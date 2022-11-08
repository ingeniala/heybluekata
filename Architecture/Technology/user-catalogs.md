# User Catalogs

## Runtime

This component will live as a **long-live running container** inside the distributed microservice architecture, inside the EKS (Kubernetes Service) data planes. As it provides an internal API for supplying information, the team considered to have this logic “alive” and not to put it in a Lambda model because of the lack of triggering mechanism (not an external API gateway call, no need to handle an EventBridge trigger, nor a time-based execution).
Like the rest of the cluster containers, it will be built using [FastAPI](https://fastapi.tiangolo.com/) framework over python interpreted language.

It will also have a Kubernetes cronjob associated responsible for polling the external providers every now and then so the catalogs are kept the most up-to-date as possible. 

## Storage

Catalogs will be held in a durable datastore so it can be retrieved anytime needed. For this purpose, and based on the nature of the data involved (which can vary among entities), the team picked a non-structural approach, therefore a noSQL engine. To stick with the rest of the decisions in terms of infrastructure and scalability, DynamoDB is the chosen repository. 

## Technology Views

For simplicity, it is provided two kinds of views. A simplified view generated using draw.io view that tells the story in a easier way, and the archimate view, useful for analytics purposes.

### Simplified view

![Drawio User catalogs](/Assets/drawio-user-catalogs.png "User catalogs in draw.io")

### Archimate View

![Archi User catalogs](/Assets/HeyBlue-User-Catalog-Technology.png "Onboarding in Archi")