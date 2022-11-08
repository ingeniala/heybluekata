# User Domain

## Runtime
Similar to the user catalogs component, this one will live as a **long-live running container** inside the distributed microservice architecture, inside the EKS (Kubernetes Service) data planes. As it holds important information and can be accessed a lot (to get profile data), but algo works as a topic listener, it’s important not to think of this component as a run-to-completion workload.

Like the rest of the cluster containers, it will be built using [FastAPI](https://fastapi.tiangolo.com/) framework over python interpreted language.

## Storage

The main takeout of the model involved in this component is the hard relationships between entities, that makes the team think of a graph model at a first sight.

The model could look like this (nodes and edges with base properties):

![User domain Model](/Assets/user-domain-graph-example.png)

*How can we store this?* The quick answer is a native noSQL graph-based db, like Neo4j or AWS Neptune (if we stick to AWS offering).
Actually, the team realized that it could be really hard to maintain this model through time, the regular writes make it very expensive to do so. Not to mention that it could be more expensive, and also that the main use cases covered with this model can also be fetch from a relational database with plain tables and relationships:

- get user/merchant information.
- get all the police officers a civilian has met.
- know all the donations done to a certain family in need.
- know how many goods a certain merchant has sold.

Although the graph model fits the best, the team also considered that the developers needed to integrate and feed this model will be harder to get, with the same expertise on graph modeling as relational models. 

So if the model can be represented as a plain table to hold the 5 different “user” entities and another table to hold transactions (and some utils tables as well), and guarantee they can be searched and joined easily, then there is no need to overdesign putting in there a graph native db, there are more cons than pros.
Therefore, and to follow other decisions about infrastructure, the db engine chosen is Amazon Aurora (Postgres SQL).

## Technology Views

For simplicity, it is provided two kinds of views. A simplified view generated using draw.io view that tells the story in a easier way, and the archimate view, useful for analytics purposes.

### Simplified view

![Drawio User domain](/Assets/drawio-tech-user-domain.png "User domain in draw.io")

### Archimate View

![Archi User domain](/Assets/HeyBlue-User-Service-Technology.png "Onboarding in Archi")