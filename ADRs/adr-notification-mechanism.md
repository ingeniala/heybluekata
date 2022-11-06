# Notification Mechanism

## Summary

One relevant aspect of application are notifications, policies and civians need receive notifications in order to allow social interaction. So it's necessary select notification mechanism for the architecture. 

### Alternatives

- Firebase FCM
- AWS SNS

## Decision 

Alternative selected: *AWS SNS*

AWS SNS was selected due to following reasons:

- It's a service of AWS (selected cloud provider for infrasture [ADR Cloud Provider](./adr-cloud.md)). 
- The core of AWS SNS is based in Firebase, so no reasons to select Firebase which belongs to other cloud provider.
- It's widely adopted for severals organizations.
- It's a mature technology supported by AWS.

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | A cloud solution could start with little cost and increase per usage. |
| CONS.05 | We decided the technology without restrictions except those defined here |
| CONS.06 | The solution will evolve as needed |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.STA.01 and AC.STA.02 | Inherited from [Cloud Technology](./adr-cloud.md) |
| AC.PER.01 and AC.PER.02 | AWS SNS will enable the compliment of this characteristic |