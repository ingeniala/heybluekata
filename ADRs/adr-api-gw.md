# Cloud Provider

## Summary

In a distributed container-based architecture, where different workloads map to isolated business capabilities, there will inevitably be multiple APIs, which could have different needs, in terms of access limitation, security, resources, pricing, etc. 

There should be a way to oversee that set of APIs so that rules can be defined and applied in a performant and centralized way, making it easier to implement a governance strategy. 

This is where an API Gateway takes precedence in the architecture and becomes a key component to define.

### Alternatives

- Amazon API Gateway
- Kong (unmanaged FOSS solution)


## Decision 

Alternative selected: *Amazon API Gateway*.


Following table contains all the reasons that drive us to make the decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Operation                | Amazon API Gateway is a managed service, no extra effort is necessary to manage it, unlike Kong where an infraestructure layer is needed to make it work, and then a day-2 operation strategy, generating extra costs to the organization. |
| Integration              | Amazon API Gateway being part of the AWS Suite implies a better integration with the rest of architecture components. |
| Team                     | Because is a service managed it's not necessary have many devops to maintain infrastructure, unlike Kong which will necessary need people around to make things work. |
| Cost                     | Amazon API Gateway is not a FOSS solution, however it has a wide free-tier where it's being payed only for the API calls received. Free tier includes one million API calls received for REST APIs, one million API calls received for HTTP APIs, and one million messages and 750,000 connection minutes for WebSocket APIs per month for up to 12 months. |

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | Amazon API Gateway is not a FOSS solution, however it has a wide free-tier where it's being payed only for the API calls received. |
| CONS.03 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.07 | AWS is a [GDPR compliant solution](https://aws.amazon.com/compliance/gdpr-center/) |
