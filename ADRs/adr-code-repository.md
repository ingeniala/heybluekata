# Code Repository

## Summary

One relevant aspect of an IT solution is how to manage the code and related artifacts. So it's necessary to select a robust code management solution. 

### Alternatives

- AWS Code Commit
- GitHub
- GitLab

## Decision 

Alternative selected: *AWS Code Commit*

AWS Code Commit was selected due to the following reasons:

- It's a service of AWS (selected cloud provider for infrasture [ADR Cloud Provider](./adr-cloud.md)). 
- The core of AWS Code Commit is GIT, so no reasons to no choose AWS Code Commit.
- It's adopted for severals organizations.

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | A cloud solution could start with little cost and increase per usage. |
| CONS.05 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.06 | The solution will evolve as needed |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.STA.01 and AC.STA.02 | Inherited from [Cloud Technology](./adr-cloud.md) |
| AC.PER.01 and AC.PER.02 | AWS SNS will enable the compliment of this characteristic |