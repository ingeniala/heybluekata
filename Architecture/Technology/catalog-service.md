# Catalog Service

## Runtime

This one will live as a **long-live running container** inside the distributed microservice architecture, inside the EKS (Kubernetes Service) data planes, because workloads will have a high frequent of use. 
Like the rest of the cluster containers, it will be built using [FastAPI](https://fastapi.tiangolo.com/) framework over python interpreted language.

## Storage

Catalogs for _merchants_ and municipalities will not have necessary the same data structure, so the proposal is to use a noSQL DB, like Dynamo DB from AWS, to stick to the guidelines defined for the whole architecture (based on AWS services).
