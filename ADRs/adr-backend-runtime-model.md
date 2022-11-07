# Backend runtime model

## Summary

One of the most important decisions to make consist in defining the backend runtime model, in order to take care of unnecesary costs and optimize the strategy regarding resources usage.


### Alternatives

- Containers (long-lived workloads)
- Serverless (run-to-completion/event-based workloads)

## Decision 

Alternative selected: *Containers and Serverless*

Both of them were selected because each one will fit well depending on the scenario. In this project there are several needs to solve, so it's necessary to have a special care in order to know when and where to use every alternative, however both will be necessary.

**Note: In the section describing the responsibilities of each component will be explain the "why" and the "which" of the selected model.**

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.05 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.06 | Containers and serverless are good options to evolve in complexity as needed, starting with something simple |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.SCA.01 | Containers and Serverless enable the compliment of this characteristic |
| AC.PER.01 and AC.PER.02 | Containers and Serverless enable the compliment of this characteristic |