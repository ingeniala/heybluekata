# ADR Observability Platform

## Summary
The observability platform is a set of tools that allows to monitor the health of our systems and applications. It is a critical component of our infrastructure and is used by all teams to ensure that our systems are running smoothly.

### Alternatives
* [New Relic](https://newrelic.com/)
* [Datadog](https://www.datadoghq.com/)
* [OpenTelemetry](https://opentelemetry.io/)
* [Dynatrace](https://www.dynatrace.com/)
* [AWS CloudWatch](https://aws.amazon.com/cloudwatch/)

## Decision
Based on the preview [ADR: Cloud Provider](./adr-cloud.md) and costs, AWS CloudWatch is the best integrated solution to monitoring and observability tool

Easy to use and to visualize through dashboards

| Criteria | Description |
| -------- | ----------- |
| Pricing | Starting with the free tier, the price is the most economical and ties to the consumption as pay as you go. |
| Collect | Near real-time logs and metrics from resources, applications and services |
| Monitor | Provide dashboards and the possibility to create reusable graphs, alarming with configurable thresholds on metrics and triggering action based on it, correlate logs and metrics, integrated with EKS and k8s, monitor application endpoints and client side performance to enhance end users experience. |
| Act | Based on the monitored metrics and logs, it is possible to automate actions like autoscaling and executing actions via lambda functions or alarming through SNS topics. |
| Analyze | CloudWatch can manage custom operations on metrics, log analysis including container and lambda metrics logs and traces, external custom metrics such us on-premise apps. |

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
