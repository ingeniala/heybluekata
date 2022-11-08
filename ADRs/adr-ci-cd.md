# CI CD

## Summary

One relevant aspect of an IT solution is how to manage the build and deployment of the solutions. So it's necessary to select a robust CI CD solution. 

### Alternatives

- AWS Code Pipeline
- AWS Code Build
- GitHub
- GitLab

## Decision 

Alternative selected: *AWS Code Build and AWS Code Pipeline*

AWS Code Build and Code Pipeline were selected due to the following reasons:

- They're AWS services (selected cloud provider for infrasture [ADR Cloud Provider](./adr-cloud.md)). 
- They're adopted for severals organizations (high maturity & adoption).

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | A cloud solution could start with little-to-no cost and increase per usage. |
| CONS.03 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.06 | The solution will evolve as needed |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.STA.01 and AC.STA.02 | Inherited from [Cloud Technology](./adr-cloud.md) |
| AC.PER.01 and AC.PER.02 | AWS SNS will enable the compliment of this characteristic |
| AC.MOD.01 | CI CD Pipelines will enable the coverage of this Architecture Characteristic |