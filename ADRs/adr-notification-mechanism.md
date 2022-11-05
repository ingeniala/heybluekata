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