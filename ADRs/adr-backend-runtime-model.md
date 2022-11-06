# Backend runtime model

## Summary

An important decision we have to make is define the model to follow for the backend runtime, in order to have the best strategy in the use of resources.


### Alternatives

- Containers
- Serverless

## Decision 

Alternative selected: *Containers and Serverless*

Both of them were selected because each one is good for diferent scenarios. In the project we have many different needs, we have to solve, so it's necessary have a special care in order to know when and where use them, but both are necessary for the application.

**Note: In responsibilities description of each component will be explain "why" and "which" model was selected for it.**

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.05 | We decided the technology without restrictions except those defined here |
| CONS.06 | Containers and serverles are good technologies to evolve in complxity as needed, starting little at the begining |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.SCA.01 | Containers and Serverless enables the compliment of this characteristic |
| AC.PER.01 and AC.PER.02 | Containers and Serverless enables the compliment of this characteristic |