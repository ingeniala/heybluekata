# Containers runtime service

## Summary

Over the last years (OCI)[https://es.wikipedia.org/wiki/Open_Container_Initiative] based containers become in a _de facto_ strategy to build applications, because they are lightweight, allow fast delivery code, high portability between environments, and save money doing a better use of resources. Although they have many advantages, when architectures are designed around dozens or hundreds of them, some new challenges appear like orchestration, discovery, communication, self-healing, resilience, balanced replication at scale. Luckily, some platforms were created to mitigate these situations.

### Alternatives

- ECS
- EKS

## Decision 

Alternative selected: *EKS*


Following table contains all the reasons that drives to make the decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Portability              | Due to EKS being a custom distribution of a plain vanilla Kubernetes, it is easily portable to other cloud.				   						   |
| No vendor lock-in         | No vendor lock-in because it's based on an open source Kubernetes, unlike ECS what is a proprietary AWS product. | 
| Community 			   | Community support because it's based on an open source product, unlike ECS what is a proprietary AWS product. |
| Capacity                 | Someone of HeyBlue should be in charge of the infrastructure, it will be easier to find Devops with knowledge in k8s (EKS) than ECS. |
| Integration              | K8s allows integrations / enhacements with many tools, for example the templating deployment tool helm, envoy, istio, a vast amount of tracing, monitoring, and metrics reporting solutions (Prometheus, Grafana, Jaeger, and more), unlike ECS which is stuck to AWS observability stack. |

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | EKS avoids vendor lock-in, has a wide community support, and also could be cheaper than ECS (if the solution is well designed) |
| CONS.03 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.06 | The solution will evolve as needed |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.SCA.01 | Containers are a good fit to enable this characteristic |
| AC.STA.01 and AC.STA.02 | Containers are a good fit to enable this characteristic |