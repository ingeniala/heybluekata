# Cloud Provider

## Summary


### Alternatives

- Amazon API Gateway
- Kong 


## Decision 

Alternative selected: *Amazon API Gateway*.


Following table contains all the reasons that drive us to make the decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Operation                | Amazon API Gateway is a managed service, no extra effort is necessary to manage it, unlike Kong.displayed in a k8s cluster.|
| Integration              | Because is part of AWS Suite has better integration with the rest of architecture components.	       |
| Team                     | Because is a service managed it's not necessary have many devops to maintain infrastructure, unlike Kong displayed in a k8s cluster.|


