# Rule Engine

## Summary

A lot of functionality in Hey Blue solution depends on business rules. A core decision of the architecture is how to manage the rules in a sustainable way.


### Alternatives

- [Python Business Rule Engine](https://pypi.org/project/business-rule-engine/) (related with [adr-backend-technology](./adr-backend-technology.md))
- Hardcoding

## Decision 

Alternative selected: *Python Business Rule Engine*

The team chooses Python Business Rule Engine over Hardcoding due mainly to cost constraint (code is hard to maintain than markup language in maintainance mode), extensibility and usability of the solution for developers.

Due to the startup nature of Hey Blue, and trying to minimize the need of code development to a minimum (see restrictions) there are several benefits in usinge some business DSL (Domain Specific Language):

- Avoid to code and deploy every new business logic change: something expected to happen very often in the first iterations of the Hey Blue solution and product development.
- DSLs provide a more natural language and a steep learning curve, decreasing the time to market.
- "Commoditization" of software improves the archicture operation and mantainability.
- Architecture complexity is reduced.
- Python DSL is a well known and mature open source software that can be used at no additional cost.

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | Python Business Rule Engine is an open source and free solution |
| CONS.03 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.06 | A rule engine is a good option to evolve in complexity as needed, starting with something simple |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.CON.03 | Python Business Rules engine is an open source solution, so the police officer can access and audit the code |
