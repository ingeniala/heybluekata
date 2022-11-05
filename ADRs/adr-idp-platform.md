# IDP Platform

## Summary

In order to manage identity and control the access to application for policies, civilians, charity and family in needs, it's necessary define a platform to cover such needs in the architecture.

### Alternatives

- AWS Cognito
- Auth0

## Decision 

Alternative selected: *AWS Cognito*.

Reasons for decision:

- Because AWS Cognito belongs to AWS, which is the cloud provider selected for the infrastrusture [ADR Cloud Provider](./adr-cloud.md).
- It's simple to start with.
- Native integration with the architecture components due to it belongs to AWS.
- It's not necessary have specialists in an other platforms, we only need people with knowledge in AWS services.