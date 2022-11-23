# Cloud Provider

## Summary

Previous [ADR for Infrastructure](./adr-infrastructure.md) defined cloud as the layer where the solution will reside. Nevertheless, it's also necessary to decide which cloud-based provider to use because the market provides many options as of today.

### Alternatives

- AWS
- GCP
- Azure

## Decision 

Alternative selected: *AWS*

Region picked: us-east-2 (Ohio)

Following table contains all the reasons that drives the decision:

| Criteria                 | Description
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Maturity                 | It's the most mature cloud services provider on the market, compared with GCP and Azure. |
| Market                   | AWS is a leader in the market with around 32%, unlike Azure with 19% and GCP with 7%, approximately.  |
| Capacity | Being a leader on the market translates into a bunch of IT professionals with knowledge about it. |
| Cost                     | Dedicated plan for startups with 100.000 AWS credits.
Also, AWS has plans for [Non-profit organizations](https://aws.amazon.com/government-education/nonprofits/?wwps-cards.sort-by=item.additionalFields.sortDate&wwps-cards.sort-order=desc) |
| Cost                     | Free tier for testing. |
| Cost Models              | Pay as you go, reserved plans (in case of upfront needs) |
| Features                 | A widely range of services and features, it’s the cloud with more features in: Computing services, storage service, AI/ML. Regarding databases services it’s barely surpassed by Azure, but remains as a leader in the rest of relevant services. |
| Global Expansion         | More presence around the globe, with many more locations compared to Azure and GCP. |
| Growth                   | It's the best option to grow up, because offers better pricing for largest instances compared to Azure and GCP. |
| GDPR | GDPR fully-compliant. [Link](https://aws.amazon.com/es/blogs/security/all-aws-services-gdpr-ready/) |
| Region | Based on a low pricing tier and a low rate of popularity, Ohio is the best AWS region to go with as it's as cheap as North Virginia, but not that heavily used (lots of people hire services in us-east-1 by default, which makes sense because it was created first and it provides more AZs). Ohio, on the other hand, provides only 3 AZs (availability zones) which the team considered enough for the architecture designed. [Link1](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/) / [Link2](https://openupthecloud.com/which-aws-region-cheapest/) |

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | Dedicated plan for startups with 100.000 AWS credits. Also, AWS has plans for [Non-profit organizations](https://aws.amazon.com/government-education/nonprofits/?wwps-cards.sort-by=item.additionalFields.sortDate&wwps-cards.sort-order=desc) |
| CONS.03 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.06 | Cloud solution is a simple way to support the implementation |
| CONS.07 | AWS is a [GDPR compliant solution](https://aws.amazon.com/compliance/gdpr-center/) |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.STA.01 and AC.STA.02 | The AWS [SLA](https://aws.amazon.com/compute/sla/) defines a minimum uptime of 99.99% with penalties |
| AC.SCA.01 | Cloud solution enables to start with the few resources as possible |

