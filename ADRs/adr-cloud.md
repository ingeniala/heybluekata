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
| Capacity 				   | Due to more control over the market, we have more devops with knowledge about it.                     |
| Cost                     | Dedicated plan for startups with 100.000 AWS credits.												   |
| Cost                     | Free tier for testing.                                      										   |
| Costs                    | Pay as you go, reserved plans (in case of upfront needs)improving                                     |
| Features                 | A widely range of services and features, it’s the cloud with more features in: Computing services, storage service, AI/ML. In the case of Databases Services it’s barely surpassed by Azure, but it's a leader in the rest of relevant services.                                 																						   |
| Presence around the world| More presence a wide the world, with many locations comparing with Azure and GCP.                                 																								 |
| Growth                   | It's the best option to grow up, because offer better pricing for largest instances comparing with Azure and GCP. 																													   |
|GDPR 					   | GDPR compliance. [Link](https://aws.amazon.com/es/blogs/security/all-aws-services-gdpr-ready/)        |