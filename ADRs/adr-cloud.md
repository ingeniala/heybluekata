# Cloud Provider

## Summary

In previous [ADR for Infrastructure](./adr-infrastructure.md) was defined Cloud like the option where will be hosted backend application, but it's necessary also decide which one, because the market gives many options.

### Alternatives

- AWS
- GCP
- Azure

## Decision 

Alternative selected: *AWS*


Folowing table contains all reasons that drive us to make previos decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Maturity                 | It's the most mature cloud services solution on the market, comparing with GCP and Azure                                             																				   |
| Market                   | AWS is a leader in the market with around 32%, unlike Azure with 19% and GCP with 7%, approximately.  | 
| Capacity 				         | Due to more control over the market, we have more devops with knowledge about it.                     |
| Cost                     | Dedicated plan for startups with 100.000 AWS credits.	Also, AWS has plans for [Non-profit organizations](https://aws.amazon.com/government-education/nonprofits/?wwps-cards.sort-by=item.additionalFields.sortDate&wwps-cards.sort-order=desc)											   |
| Cost                     | Free tier for testing.                                      										   |
| Costs                    | Pay as you go, reserved plans (in case of upfront needs)improving                                     |
| Features                 | A widely range of services and features, it’s the cloud with more features in: Computing services, storage service, AI/ML. In the case of Databases Services it’s barely surpassed by Azure, but it's a leader in the rest of relevant services.                                 																						   |
| Presence around the world| More presence a wide the world, with many locations comparing with Azure and GCP.                                 																								 |
| Growth                   | It's the best option to grow up, because offer better pricing for largest instances comparing with Azure and GCP. 																													   |
|GDPR 					           | GDPR compliance. [Link](https://aws.amazon.com/es/blogs/security/all-aws-services-gdpr-ready/)        |


## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | Dedicated plan for startups with 100.000 AWS credits.	Also, AWS has plans for [Non-profit organizations](https://aws.amazon.com/government-education/nonprofits/?wwps-cards.sort-by=item.additionalFields.sortDate&wwps-cards.sort-order=desc) |
| CONS.05 | We decided the technology without restrictions except those defined here |
| CONS.06 | Cloud solution is a simple way to support the implementation |
| CONS.07 | AWS is a [GDPR compliant solution](https://aws.amazon.com/compliance/gdpr-center/) |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.STA.01 and AC.STA.02 | The AWS [SLA](https://aws.amazon.com/compute/sla/) defines a minimum uptime of 99.99% with penalties |
| AC.SCA.01 | Cloud solution enables to start as little as possible |

