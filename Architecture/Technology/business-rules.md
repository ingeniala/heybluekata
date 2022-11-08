# Business Rules

## Runtime

Similar to the user catalogs component, this one will live as a **long-live running container** inside the distributed microservice architecture, inside the EKS (Kubernetes Service) data planes. As it provides an internal API for supplying information, the team considered to have this logic “alive” and not to put it in a Lambda model because of the lack of triggering mechanism (not an external API gateway call, no need to handle an EventBridge trigger, nor a time-based execution).
Like the rest of the cluster containers, it will be built using [FastAPI](https://fastapi.tiangolo.com/) framework over python interpreted language.

Particularly in this scenario, the team decided to use a special python library to handle the definition and update of business rules, lying on what's called a BRE (business rule engine). See [ADR BRE](../../ADRs/adr-rule-engine.md).

Library reference: [Python Business Rule Engine](https://pypi.org/project/business-rule-engine/)

## Storage

Business rules will be held in a durable datastore so it can be retrieved anytime needed. For this purpose, and based on the nature of the data involved (unstructured, every rule can have different config or conditions to be met), the team picked a non-structural approach, in this case a noSQL document-based store. To stick with the rest of the decisions in terms of infrastructure and scalability, DynamoDB is the chosen repository. 