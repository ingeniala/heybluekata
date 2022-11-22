# Omnichannel - Backend for Frontend

## Summary

Given the uprising of new tech such as smartphones, tablets, IoT, and others; new needs came up to the ecuation regarding creating application user interfaces. So, organizations faced the new challenge of extending the web client to others, such as mobile (like in this scenario).

Although every channel that interacts with the same data provider (backend, APIs) has different needs, it must bring the user the idea of a unified experience no matter the mean used (omnichannel).

That being said, core business capabilities are the same in every channel, but it's its responsibility to create the best way to interact with end users.

### Alternatives

- BFF (backend for frontend architectural pattern)
- None (both mobile and web client accessing same business APIs)

## Decision

Alternative selected: *BFF*

Some benefits of implementing BFFs:

- Multiple frontend application interfaces can call their respective BFF backends in parallel, and dedicated backend services can respond faster.   
- Following BFF architecture reduces the time to make modifications and enhancements in backend systems with dedicated teams working on the upgrades.   
- The BFF layer in the overall system architecture can benefit from hiding sensitive or unnecessary data before transferring it to the frontend application interface, which helps simplify the system. 
- BFF backend systems can use any protocol like FTP, SOAP, REST or GraphQL to request data from microservices, but still use a single protocol when interacting with the frontend application interface.    
- BFF can cache or maintain active sessions, which could vary depending on the channel being used.  
- BFF can help orquestrate several API calls in order to fullfil a business requirement requested by a specific channel.    
- BFF hides from the channel the token management (expiration, renewal), in case of authentication/authorization flows (Oauth2.0/OIDC).


## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.03 | There were no restrictions, except for those defined here, about technology related decisions |

### Internal Constraints

There are some drawbacks using BFF:

| Drawbacks ID | Explanation |
| ------------- | ----------- |
| DRA.6 | BFF now becomes a SPOF (single point of failure), because any downtime affects directly to the channel. To remediate the situation, the BFF will be deployed in the AWS cloud, in a environment where high availabilty and scalability are key pillars for applications. |