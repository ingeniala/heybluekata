# Onboarding

## Runtime

This component will live as a **long-live running container** inside the distributed microservice architecture, inside the EKS (Kubernetes Service) data planes. It will be built by using [FastAPI](https://fastapi.tiangolo.com/) and python language.
In this case, as the performance of this component will depend on several internal/external integrations conforming a whole flow that could delayed more than expected, the team considered it suitable to put this logic on an active running container instead of a running-to-completion workload (like a serverless function or job).