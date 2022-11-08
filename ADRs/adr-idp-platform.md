# IDP Platform

## Summary

In order to manage identity and access control to the application for police officers, civilians, charity and family in needs, it's necessary to define a platform to cover such needs in the architecture.

### Alternatives

- AWS Cognito
- Auth0 (OKTA)

## Decision 

Alternative selected: *AWS Cognito*.

Here are the main reasons backing up this decision:

- AWS Cognito belongs to AWS, which is the cloud provider selected for the infrastrusture [ADR Cloud Provider](./adr-cloud.md), and the main guideline used for making many other decisions.
- It's a good option to start with something simple.
- Native integration with the architecture components due to it belongs to AWS.
- It's not necessary to have specialists in other platforms rather than AWS services.

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | Could be a cheap solution if it's managed with Non-profit organization AWS offering |
| CONS.03 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.07 | AWS is a [GDPR compliant solution](https://aws.amazon.com/compliance/gdpr-center/) |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.SEC.02 | Authentication and Authorization are core features of Cognito |
| AC.SEC.03 | AWS cognito supports device linking with little effort |
| AC.STA.01 and AC.STA.02 | Inherited from [Cloud ADR](adr-cloud.md) |