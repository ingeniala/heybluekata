# Amazon Elastic Kubernetes Service Dataplane Runtime

## Summary

Based on other decisions made by the team such as using [AWS](./adr-cloud.md) as preferred cloud provider and [AWS EKS](./adr-containers-runtime-service.md) as the default solution for managing the containers where main functionalities will reside; another third related decision came up: how to optimize the compute needs inside EKS, referring to not only saving some money but also using only what's needed by applications. 

### Alternatives

- EC2 (plain virtual machines provisioned and managed by AWS)
- Fargate (serverless compute solution provisioned and managed by AWS)

## Decision 

Alternative selected: *Fargate*

The primary aim of Fargate is to remove the necessary overhead in managing your own EC2 worker nodes. When a new application is deployed to EKS using Fargate, AWS provisions a new serverless compute environment to run your application in. Once deployed, this workload running on Kubernetes appears almost identical to its EC2 equivalent:

- it’s still run as a pod   
- you use the same kubectl commands and     
- you’re still able to retrieve logging

Following table contains all the reasons that drive us to make the decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Operation                | Fargate profiles are managed and provisioned entirely by AWS, so it has no extra effort managing virtual machines as Kubernetes worker nodes. |
| Sizing                   | AWS Fargate matches workloads requirements with a set of pre-configured CPU & Memory based price points. See [pricing](https://aws.amazon.com/fargate/pricing/). | 
| Cost 			           | Running pods in an ‘always-on’ mode (EC2) for a month could cost roughly more than fitting into a Fargate pricing category, that could result in a cheaper workload. Although using EC2 "spot" instances could be a better scenario in terms of money savings, the cost of loosing a virtual machine every now and then (see spot terms & conditions), migrating workloads and the effort needed to support the infra is worst. So that being said, Fargate turns to be "cheaper". |
| Security                 | Secure isolation by design: individual EKS pods run in their own dedicated kernel runtime environment and do not share resources with any other pod. |

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | EKS Fargate implies using only what is needed, so it could be considerably cheaper than EC2 "alive" on-demand virtual machines. |
| CONS.03 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.06 | The solution will evolve as needed. The more pods are created, the more compute Fargate will provide, always matching the resources requirements. |

### Internal constraints

There are some drawbacks using Fargate:

| Drawback ID | Explanation |
| ------------- | ----------- |
| DRA.1 | Creating Kubernetes Daemonsets objects (not necessary for now, but could be done using a separate node pool with EC2 machines). |
| DRA.2 | Privileged containers are not supported (although this is actually a best practice to follow). |
| DRA.3 | GPUs are currently not available in Fargate. (not needed). |
| DRA.4 | Only Private Subnets are supported (generally best practice). |
| DRA.5 | AWS Container Insights is currently unsupported on EKS Fargate. (not needed) |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.STA.01 and AC.STA.02 | The AWS [SLA](https://aws.amazon.com/compute/sla/) defines a minimum uptime of 99.99% with penalties |
| AC.SCA.01 | Cloud solution enables to start with the few resources as possible |