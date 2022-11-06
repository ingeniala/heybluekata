# Infrastructure

## Summary

In the beginning of a project it's necessary take many decisions one of them is related to where will be host the backend application.

### Alternatives

- Cloud
- On-premises

## Decision 

Alternative selected: *Cloud*


Folowing table contains all reasons that drive us to make previos decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Regulamentary restrictons| Scenario of startup without legal restrictions.                                                       |
| Cost                     | Scenario of startup with small budget to have own infrastructure.									   | 
| Capacity 				   | In general, a startup begins with few people, so small team can't manage all infrastructure.          |
| Time to market           | Cloud provides features and service which give quickness in the delivery process. Cloud is a booster for startups.|
| Scalability              | Cloud allows starting small with the ability to easily grow up.                                       |
| Costs                    | Pay as you go, reserved plans (in case of upfront needs)improving                                     |

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | Cloud is a less expensive solution, not only in infrasture and licences, but also in cost of maintenance |
| CONS.05 | We decided the technology without restrictions except those defined here |
| CONS.04 | A cloud solution should improve the confidence of the police with the solution |
| CONS.06 | Cloud solutions enable the evolution of the applications as needed |
| CONS.07 | Cloud providers are often compliance with GDPR and other policies |


## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.STA.01 and AC.STA.02 | Stability in cloud is cheaper and easier than in on premises |
| AC.SCA.01 | Scalability is one of the bigger advantages of cloud solutions |