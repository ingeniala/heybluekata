# Messaging Mechanism

## Summary

In the last years, messaging through queues or topics has become in a way to communicate architecture components in thousands of applications. HeyBlue is not the exception, so it's necessary find the best platform to cover this need.

### Alternatives

- AWS Kinesis
- AWS SQS

## Decision 

Alternative selected: *WS Kinesis*


Folowing table contains all reasons that drive us to make previos decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Data consuming           | AWS Kinesis allows data consuming by many times, unlike AWS SQS.                                      |
| Data deletion            | Data is deleted after the retention period, unlike AWS SQS (data is deleted after consumption).	   | 
| Retention Policies 	   | Stores record for 24 hours by default and can retain streaming data for up to 365 days, unlike AWS SQS which maximum is 14 days.																										   |
| Integrations             | Can send stream records directly to services such as Amazon S3, Amazon Redshift, Amazon ElasticSearch, Splunk, AWS Lambda, unlike AWS SQS which only allows AWS Lambda.																   |
| Pub/Sub                  | Build multiple applications reading from the same stream independently, unlike AWS SQS where one application one queue.																											 |
| Quering data             | “Streaming MapReduce” querying capability (Spark, Flink).											   |