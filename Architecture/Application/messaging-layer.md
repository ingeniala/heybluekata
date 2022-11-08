# Messaging Layer

## Description
Backing up the [ADR Messaging](/ADRs/adr-messaging-mechanism.md) decision of designing decoupled components to guarantee async flows, thus no extra waiting time for users (a better experience), this section describes how the information is being exchanged through an event broker, in this case Kinesis stack (using Kinesis Data Streams + Data Firehose). 

_Why using both of them?_ Although any of them provides real-time / near real-time stream processing and the ability to scale and handle a bunch of data, there are a few differences to consider and that's why they are usually combined when defining a streaming data pipeline. 

- Kinesis Data Streams provides the data storage needed in case of data loss or corruption on the consumer side, and also nice features like replay capabilities.
- Kinesis Data Firehose makes it easy to load that streaming data into other AWS services, like ElasticSearch, S3 buckets or Redshift. It's like the glue needed to bind all the data not only to suscribed consumers, but also a datastore which can grow exponentially through time (such as a lake or a telemetry tool).

The figure below (figure 10.13.1) shows what it is said previously:

![Figure 10.13.1 - Kinesis Streams](/Assets/kinesis-streams.png "Figure 10.13.1 - Kinesis Streams")

## Stream distribution

In this solution, there are two streams clearly defined: one for user related events and another one for transaction recording.

The first one is filled by the `onboarding component` and notifies an event every time a new user is created and assigned credentials in the platform, therefore that event should reach the `user domain` datastore and also S3 archives, to keep track of every activity.

The second one is basically for every transaction registered by the platform (donations, interactions, redemptions) so the `scoring service` will push every one of them into the proper stream and once again, every suscriber can fetch the data (for archiving/analytics, structured storage in the `user domain` component).

As a resume, to logically separate sets of data, there are separate stream for each dataset.