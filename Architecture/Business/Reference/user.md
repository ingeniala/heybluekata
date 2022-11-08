# User

Business responsibilities associated with the user and its lifecycle, from the onboarding to the deletion of the platform.

Includes the following business functions:

## Identity

Identity of each users, including:

* Given and family name (for persons)
* Company name (for organizations)
* User name
* Identity information (ID number, taxes ID, etc)

**As showing in the seccion [User - Motivation mapping](#user---motivation-mapping), in this case the focus of the defined architecture will be on the management of the identity information about the different actors.**

## Addressing

Addressing characteristics of the users, including:

* Snail mail address
* Email address
* Social URIs

**As showing in the seccion [User - Motivation mapping](#user---motivation-mapping), in this case the focus of the defined architecture will be on the management of the email address, social URIs and Postal Code.**

## Social Graph

Management of the social graph, showing the relationship of a user with the universe of users in the platform. Includes:

* Contacts
* Groups
* Brands
* Access control

**As showing in the seccion [User - Motivation mapping](#user---motivation-mapping), in this case the focus of the defined architecture will be on the management of the interactions graph that represents the relationships between actors.**

## Profile

Profile management of the user in the social network, including:

* Profile page
* Profile Data
* Presence
* Location
* Skills / habilities

**As showing in the seccion [User - Motivation mapping](#user---motivation-mapping), in this case the focus of the defined architecture will be on the management of the basic information of the profile, like number of interactions, points redemptions history (relation with gamification).**

## User - Motivation mapping

The figure 8.2.1. shows how the *user* business function support the functional requirements and how they are influenced by the architecture characteristics and constraints.

![Figure 8.2.1 - User - Motivation matrix](/Assets/1.6-Motivation-User-mapping.png "Figure 8.2.1 - User - Motivation matrix")

As we can see in the previous diagram, all the busines functions will participate in some way covering the Hey Blue architecture.

## User - Conceptual Architecture mapping

The figure below (Figure 8.2.2) shows how the components of the conceptual architecture (more info in [Application Components Collaboration Views](/README.md#application-component-collaboration-views)) realize the Reference Architecture.

![Figure 8.2.2 - User Conceptual Architecture Mapping](/Assets/User-Conceptual-Architecture-Mapping.png "Figure 8.2.2 - User Conceptual Architecture Mapping")