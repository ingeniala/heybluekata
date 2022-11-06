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

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | Is a cheap solution if it is managed with Non-profit org AWS offering |
| CONS.05 | We decided the technology without restrictions except those defined here |
| CONS.07 | [AWS](https://aws.amazon.com/government-education/nonprofits/?wwps-cards.sort-by=item.additionalFields.sortDate&wwps-cards.sort-order=desc) is GDPR compliant solution |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.SEC.02 | Authentication and Authorization are core features of Cognito |
| AC.SEC.03 | AWS cognito supports device linking with little effort |
| AC.STA.01 and AC.STA.02 | Inherited from [Cloud ADR](adr-cloud.md) |