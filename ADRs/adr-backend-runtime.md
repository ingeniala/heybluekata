# Backend runtime

## Summary

In the las years dockers containers become in a de facto strategy to build applications, because they are lightweight, allow fast delivery code, transfer the code easly, and save money doing better use of resources. Although they have many advantages their manage and orchestration could turn a big challenge. In order to mitigate this problem have emerged some platforms to help in this matter.

### Alternatives

- ECS
- EKS

## Decision 

Alternative selected: *EKS*


Folowing table contains all reasons that drive us to make previos decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Portability              | Due to EKS is based on k8s is easly portable to other cloud.				   						   |
| No vendor lockin         | No vender lock-in because is based on an open source k8s, unlike ECS what is a proprietary AWS product.  																														   | 
| Community 			   | Community support because is based on an open source product, unlike ECS what is a proprietary AWS product.                  																										   |
| Capacity                 | Someone of HeyBlue should be in charge of infrastructure, it will be easier found Devops with knowledge in k8s (EKS) than ECS.  										   																    |
| Integration              | K8s allows integrations / enhacements with many tools, for example the templating deployment tool helm, envoy, istio, a vast array of tracing, monitoring, and metrics reporting solutions (Prometheus, Grafana, Jaeger, and more), unlike ECS.																															   |
