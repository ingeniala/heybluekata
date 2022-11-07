# Infrastructure

## Summary

One of the first of many decisions to make at the beginning of a project is basically where the solution should exist, where the components should live taking account of the key drivers and mandatory constraints given by the business (e.g. time matters, no extra costs allowed, easy-to-setup-and-scale solution). 

### Alternatives

- Cloud (fully-managed infrastructure by a cloud provider)
- On-premise (self-hosted or not, but living on a specific locatable datacenter)

## Decision 

Alternative selected: *Cloud*


Following table contains all the reasons that drive us to make the decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Regulamentary restrictons| Scenario of startup without legal restrictions. |
| Cost                     | Scenario of startup with small budget to have its own infrastructure. | 
| Capacity 				   | In general, a startup begins with few people, so a small team can't manage all infrastructure on their own. |
| Uncertainty 			   | In general, a startup does not know or even care about the amount of servers needed to cover the solution demands, which can be uncertain at first. A great fit for choosing a pay-as-you-go cloud suscription |
| Time to market           | Cloud provides features and services which speeds the delivery process up. Cloud is a booster for startups. |
| Scalability              | Cloud allows starting quick-and-easy with the ability to grow up as needed. |
| Costs                    | Pay as you go, reserved plans (in case of upfront needs) |

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | Cloud is a less expensive solution, not only in infrasture and licences, but also in cost of maintenance |
| CONS.05 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.04 | A cloud based architecture should improve the confidence of the police officers as part of the solution |
| CONS.06 | Cloud solutions enable the evolution of the applications as needed |
| CONS.07 | Cloud providers are often compliance with GDPR and other policies |


## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.STA.01 and AC.STA.02 | Stability in cloud is cheaper and easier than in on premises |
| AC.SCA.01 | Scalability is one of the bigger advantages of cloud solutions |