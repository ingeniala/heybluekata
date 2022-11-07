# Messaging Mechanism

## Summary

Over the last years, messaging through queues or topics has become a great option to decouple architecture components in a distributed scenario conformed by a several applications. _HeyBlue_ is not the exception, so it's necessary to find the best platform to cover this need.

### Alternatives

- AWS Kinesis
- AWS SQS

## Decision 

Alternative selected: *AWS Kinesis*

Following table contains all the reasons that drive us to make the decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Data consuming           | AWS Kinesis allows data to be consumed many times, unlike AWS SQS. |
| Data deletion            | Data is deleted after a specific retention period, unlike AWS SQS (data is deleted only after consumption). | 
| Retention Policies 	   | Kinesis stores records for 24 hours by default and can retain streaming data for up to 365 days, unlike AWS SQS which maximum is 14 days. |
| Integrations             | Kinesis can send stream records directly to services such as Amazon S3, Amazon Redshift, Amazon ElasticSearch, Splunk, AWS Lambda, unlike AWS SQS which only allows AWS Lambda. |
| Pub/Sub                  | Kinesis allows multiple applications reading from the same stream independently, unlike AWS SQS where there is one suscriber per queue. |
| Quering data             | _"Streaming MapReduce"_ querying capability (Spark, Flink). |

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | A cloud solution may start with little-to-no cost and increase based on the usage. |
| CONS.05 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.06 | The solution will evolve as needed |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.STA.01 and AC.STA.02 | Inherited from [Cloud Technology](./adr-cloud.md) |
| AC.PER.01 and AC.PER.02 | AWS Kinesis will enable the compliment of this characteristic |