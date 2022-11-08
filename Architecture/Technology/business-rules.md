# Business Rules

## Runtime

Similar to the user catalogs component, this one will live as a **long-live running container** inside the distributed microservice architecture, inside the EKS (Kubernetes Service) data planes. As it provides an internal API for supplying information, the team considered to have this logic “alive” and not to put it in a serverless model because of the lack of triggering mechanism (not an external API gateway call, no need to handle an EventBridge trigger, nor a time-based execution).
Like the rest of the cluster containers, it will be built using [FastAPI](https://fastapi.tiangolo.com/) framework over python interpreted language.

## Storage

Business rules will be held in a durable datastore so it can be retrieved anytime needed. For this purpose, and based on the nature of the data involved (unstructured, every rule can have different config or conditions to be met), the team picked a non-structural approach, in this case a noSQL document-based store. To stick with the rest of the decisions in terms of infrastructure and scalability, DynamoDB is the chosen repository. 