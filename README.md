# O'Reilly Architectural Katas - Fall 2022 - HeyBlue

## Table of Contents

* [About Los Ingenials](#about-los-ingenials)
* [Glossary](#glossary)
* [Prelude](#prelude)
* [Functional requirements](#functional-requirements)
* [Constraints](#constraints)
* [Quality Attributes](#quality-attributes-aka-architecture-characteristics)
* [Assumptions](#assumptions)
* [Architecture](#architecture)
    * [Reference Architecture](#reference-architecture)
    * [Bussiness Collaboration View](#business-collaboration-view)
    * [Application Component Collaboration Views](#application-component-collaboration-views)
    * [Technology & Deployment View](#technology--deployment-view)
* [Evolution Roadmap](#evolution-roadmap)
* [Adoption Practices](#adption-practices)
* [Team Organization](#team-organization)
* [Resources](#resources)
* [ADRs](#architecture-decision-records)


## About Los Ingenials

We are a tribe of guys who are enthusiastic about solving complex problems with technology applied vith criteria in a sustainable way. 

Our name is Ingenials, becouse we work together for Ingenia, a consulting firm focused on allowing our customers to strategically and tactically leverage their business with technology. 

### Members

* [Silvia Fresno](https://www.linkedin.com/in/silvia-fresno/)
* [Paula Ferreyra](https://www.linkedin.com/in/paula-ferreyra-4506a018/)
* [Fernando Sclavo](https://www.linkedin.com/in/fernando-sclavo-738252b9/)
* [Federico Catinello](https://www.linkedin.com/in/fcatinello/)
* [Andres Kitaura](https://www.linkedin.com/in/andreskitaura/)
* [Santiago Blanco](https://www.linkedin.com/in/santiagomblanco/)

## Glossary

* API: Application Program Interface.
* Charity: Organizations aimed to improve the world each day. In general, non profit organizations. e.g. Greenpeace, WWF, Operation Smile, UNICEF.
* Civilian: Member of the community that wants to connect to police officers, get points and redem them for products and services, or donate them to a charity organization or a family in needs.
* Constraint: Represents a factor that limits the realization of goals.
* Driver: Represents an external or internal condition that motivates an organization to define its goals and implement the changes necessary to achieve them
* Family in needs: Members of a community able to receive points as a donation, to after redem them for products and services.
* Goal: Represents a high-level statement of intent, direction, or desired end state for an organization and its stakeholders.
* IRS: Internal Revenue Service.
* Police Officer: Member of a community that can accept connection with a civilian, obtain points and donate them to a charity organization.
* Retail: Members of a community providing product and services that can be redem for hey blue points.

## Prelude

The Hey, Blue! initiative facilitates moments of meaningful connection between police officers
and members of their community by offering intentional opportunities for individuals to meet and
share positive experiences.

Inspired by the extraordinary acts of heroism displayed by both individual community members
and first responders during 9/11, EcoSchool co-founder, John Verdi, wanted to build a platform
that could bring police officers and communities together with a shared purpose.
Connection-driven projects like Preschool Storytime and Selfies For Change are just the start of
a larger movement designed to create an awareness of our shared humanity.

You can find additional information about HeyBlue and Verdie School in [heyBlue](https://heyblue.app/)
and [Verdie School Nonprofit](https://www.verdiecoschool.org/heyblue)

## Functional requirements

The figure 1.1 - Motivation shows the vision of HeyBlue, its functional requirements and how them relate or influence each other.

![Figure 1.1 - Motivation](/Assets/1.1.Motivation.png "Figure 1.1. - Motivation")

Bellow, we will describe each of them.

### Drivers

* DR01. Hey Blue is motivated for the reinforcement of a shared pourpouse between community and police officers.
* DR02. Hey Blue want to create a common awareness of our shared community.

### Goals

* GO01. Enforce positive relationship between police officers and civilians
* GO02. Actively support to non-profit organizations
* GO03. Reinforce a stronger community interaction

### High level use Cases

The table bellow describe the High level use cases, and the relationship with the goals described above.

| UC ID | Description | Related Goals |
| ----- | ----------- | ------------- |
| UC01  | As hey blue administrator I want to get reports and analytics of the application activity | GO01, GO03 |
| UC02 | As hey blue administrator I want to share aggregated tracking data with local media outlets, automatically | GO01, GO02, GO03 |
| UC03 | As a local media outlet I want to subscribe to get access to aggregated data | GO03 |
| UC04 | As a User I want to connect to another users | GO03 |
| UC05 | As a user I want to share information about my profile in social media | GO01, GO03 |
| UC06 | As HeyBlue Admin I want the app to track the location of the users | GO03 |
| UC07 | As a user I want to connect to my social media profile | GO03 |
| UC08 | As a user i want to opt-in and out of push notifications | GO01 |
| UC09 | As a civilian I want to find retail stablishments to redeem my points | GO03 |
| UC10 | As an officer I want to find charities where I can gift the points | GO02 |
| UC11 | As a business/charitie I want to create a storefront to encourage users to redeem or donate their points | GO01, GO02 |
| UC12 | As a Business I want to manage the catalog of products and the point value assigned to them | GO03 |
| UC13 | As a municipality I want to allow civilians to redeem the points to pay fines or fees | GO03 |
| UC14 | As a user I want to receive positive reinforcement through intrinsec reward system based on my activity | GO01, GO03 |
| UC15 | As heyblue admin I want to track how the points were used for each user | GO01, GO03 |
| UC16 | As an officer or community member I want to connect with each other using QR Codes | GO03 |
| UC17 | As a community member I want to see how many connections each participating officer has made | GO01, GO03 |
| UC18 | As heyBlue Admin I want to know the users zip codes to share revenues with community in the user area | GO03 |
| UC19 | As a civilian I want to say hi to a police officer to gain points | GO01 |
| UC20 | As a HeyBlue Admin I want to ensure the employee experience, including recruiting, upskilling and lifecycle | |
| UC21 | As an investor I want to get information about the numbers of the company | |
| UC22 | As HeyBlue Admin I want to control the financial performance | |
| UC23 | As IT responsible of HeyBlue I want best practices, tools to ensure an efficient IT Value delivery | |
| UC24 | As HeyBlue Admin I want to control and manage the risks, mainly the fraud related risks | |

## Constraints

The figure 1.2 shows the Constraints detected for Hey Blue.

![Constraints](/Assets/1.2.Constraints.png)

Below, we will describe each one of them.

* CONS.01 - The cost should be as little as possible. HeyBlue is a non-profit company. The use of resources should be wisely defined. Choose the cheapest alternative if it is possible.
* CONS.02 - Application should be mobile and web
* CONS.03 - There is no restriction about technology
* CONS.04 - The solution should be limited to USA cities (by Zip Codes)
* CONS.05 - The officer location feature must be implemented in a way that ensure the officer confidence on it.
* CONS.06 -  Define a solution that evolve with a team
* CONS.07 - Compliance with GDPR


## Quality Attributes (AKA Architecture Characteristics)

The figure 1.3. shows the Quality Attributes (A.K.A. Architecture Characteristics) identified for Hey Blue.

![Architecture Characteristics](/Assets/1.3.Architecture%20Characteristics.png).

In the following sections we describe each architecture characteristics:

* Usability Characteristics
    * [AC.USA.01 - Web App Usability](/Characteristics/ac-usa-01.md)
    * [AC.USA.02 - Mobile App Usability](/Characteristics/ac-usa-02.md)
* Security Characteristics
    * [AC.SEC.01 - Secure Information](/Characteristics/ac-sec-01.md)
    * [AC.SEC.02 - End User AAA](/Characteristics/ac-sec-02.md)
    * [AC.SEC.03 - Device Linking](/Characteristics/ac-sec-03.md)
    * [AC.SEC.04 - Direction of searching](/Characteristics/ac-sec-04.md)
* Confidence Characteristics
    * [AC.CON.01 - Limited ammount of connections](/Characteristics/ac-con-01.md)
    * [AC.CON.02 - Connection in a limited ratio](/Characteristics/ac-con-02.md)
    * [AC.CON.03 - Officer location automatic turn of](/Characteristics/ac-con-03.md)
* Stability Characteristics
    * [AC.STA.01 - Weekdays uptime](/Characteristics/ac-sta-01.md)
    * [AC.STA.02 - Weekends uptime](/Characteristics/ac-sta-02.md)
* Modifiability Characteristics
    * [AC.MOD.01 - Add new social media](/Characteristics/ac-mod-01.md)
* Scalability Characteristics
    * [AC.SCA.01 - Increase capacity as usage](/Characteristics/ac-sca-01.md)
* Performance Characteristics
    * [AC.PER.01 - Speed of connection](/Characteristics/ac-per-01.md)
    * [AC.PER.02 - Speed of change](/Characteristics/ac-per-02.md)

## Assumptions

* IRS give information through API or file sharing. that let know when an organization is a charity organization. 
* A state department inform, through API or file sharing, what are the family in needs.
* A family in need can redeem their points but can't donate them.
* Due to its user characteristics, retails can only use Web channel.
* Hey Blue will hire employees or contractors to support its operation.
* If Hey Blue obtain financing from investors, they want to know the performance of the organization.
* Hey Blue will have a minimal IT team to maintain the application, supported by automated tools.
* Hey Blue need to avoid risks associated with the business operation.
* In a future, will be needed to integrate with additional social networks.
* Mentor and mentee feature will be out of scope of the first version of Hey Blue, and must be implemented in future iterations.
* There is no restriction about technology
* We must define a solution that evolve with a team, starting with a simple but useful solution with a small team supporting it.


## Architecture

### Reference architecture

An architecture's main objective is the clear communication of the roles and responsibilities of a system, whether it is made up of software applications or other components, which will then guide decision-making to meet the requirements of an organization. The objective of the reference architecture is to define the business responsibilities that cover the needs raised by an organization or part of it, which will then serve to define the solutions (or applications) that will instantiate it. At the same time, it establishes a common language to talk about the applications that are part of solution's architecture to support the processes associated in this case with Hey Blue. The benefits of having a reference architecture are many, among which are:

* Common language.
* Standard and clear application requirements.
* Enable automation.
* Facilitate the selection of COTS (Commercial off the Shelf) solutions.

In the case of Hey Blue, we defined a reference architecture based on the work of the [W3 consortium](https://www.w3.org/2013/socialweb/presentations/krebs1.pdf), with a few extensions of our part to cover specific requirements about produc, storefront and enterprise needs.

The figure 1.4. shows the reference architecture for social network, which define the business responsibilities associated with the Hey Blue case.

![Social Network Reference Architecture](/Assets/1.4.Social-Network-Reference-Architecture.png)

In the following sections we will describe each one of the business responsibilities, with views exported from the Archimate and detail the following topics:

- How the Reference Architecture components support the Functional Requirements
- How the Reference Architecture components support the Architecture Characteristics
- How the defined Constraints influence the Reference Architecture Components

Follow each link to get more information about each Reference Architecture meta-functions:

* [Interaction](/Architecture/Business/interaction.md)
* [User](/Architecture/Business/user.md)
* [Ubiquity](/Architecture/Business/ubiquity.md)
* [Gamification](/Architecture/Business/gamification.md)
* [Foundation](/Architecture/Business/foundation.md)
* [Commerce](/Architecture/Business/commerce.md)
* [Enterprise](/Architecture/Business/enterprise.md)

### Business Collaboration View

In the sections below, we will describe the business flows identified for Hey Blue, the supporting relationship of conceptual components (defined in the seccion [Application Components Collaboration Views](#application-component-collaboration-views)), and how the business entities are impacted or support the business processes.

This set of views are extracted from the Archimate model and detail the:
- Main business flows of the architecture
- Main business events derived from the flow and how they connect the different business flows
- Relations between the components
- Conceptual Applications components of the architecture and how they support the business processes
- Main business entities of the architecture
- Access operations on those business entities, to show what process create, update or read them

#### Onboarding flows

* [Charity Onboarding](/Business/Flows/charity-onboarding.md)
* [Civilian Onboarding](/Business/Flows/civilian-onboarding.md)
* [Family in need Onboarding](/Business/Flows/family-in-need-onboarding.md)
* [Municipality Onboarding](/Business/Flows/municipality-onboarding.md)
* [Police Officer Onboarding](/Business/Flows/police-officer-onboarding.md)
* [Retail Onboarding](/Business/Flows/retail-onboarding.md)

#### Interaction and scoring flows

* [Charity points redemption](/Business/Flows/charity-points-redemption.md)
* [Civilian / Police Officer Interaction](/Business/Flows/civilian-police-officer-interaction.md)
* [Civilian points redemption / Donation](/Business/Flows/civilian-points-redemption-donation.md)
* [Family in needs points redemption](/Business/Flows/family-in-need-points-redemption.md)
* [Police Officer points transfer / donation](/Business/Flows/police-points-transfer-donation.md)

#### Support flows

* [Device relinking](/Business/Flows/device-relinking.md)
* [Storefront Management](/Business/Flows/storefront-management.md)

### Application Component Collaboration Views

This set of views are also extracted from the Archimate model and detail the:
- Main business flows of the architecture
- Main business events derived from the flow and how they connect the different business flows
- Relations between the components
- Main business actors interacting with Hey Blue architecture
- Application coverage that supports the business processes and have direct interaction with them

### Technology & Deployment View

[Component Responsibilities](./conceptual-architecture/component-responsibility.md)

## Evolution Roadmap

## Adoption Practices

### Agile practices

Derived from the constraint [CONS.01](#constraints) and [CONS.06](#constraints), we highly recommend the adoption of agile practices (Like SCRUM or KANBAN) to manage the development, evolution and support of the solution. It will enable Hey Blue to gain speed of delivery value, cost control and increase the quality of the product delivered.

### DevSecOps 

Based on the constraint [CONS.02](#constraints) and the architecture characteristics [AC.STA.01](./Characteristics/ac-sta-01.md), [AC.STA.02](./Characteristics/ac-sta-02.md) and [AC.MOD.01](./Characteristics/ac-mod-01.md) we recommend the adoption of DevSecOps practices, in particular the application of [Teams Topologies](#team-organization) and adopt the [Type 2 DevOps Topology](https://web.devopstopologies.com/#type-two) at least at the beginning of the project, and transitate to [Type 1 DevOps Topology](https://web.devopstopologies.com/#type-one) as needed. 

### Incident Management

The incident management process is a set of activities that are performed to identify, report, and resolve incidents. The process is designed to minimize the impact of incidents on the business and to restore normal operations as quickly as possible. The process is also designed to identify the root cause of incidents and to prevent recurrence. Recommended to be integrated and automatized with the monitoring and alerting capabilities, in our case, the AWS CloudWatch, tool defined in the [ADR: Observability Platform](./ADRs/adr-observability-platform.md) section.


## Team organization

Following the requirements defined by [CONS.06](#constraints), we strongly recommend to addopt Team Topologies philosophy to define the responsibilities associated with Hey Blue. 

In the very beginning, just one Stream Aligned team will be enough to cover the responsibilities needed to deploy the first versions of Hey Blue in an agile way. The image below describe this initial situation:

![Team Topologies  v1.0](/Assets/TeamTopologies-V1.0.png "Initial Team Topology")

In this initial team deployment, we recommend to have the following roles:

* Web Developer, responsible for the development, evolution and support of the web components.
* Mobile Developer, responsible for the development, evolution and support of the web components.
* Backend Developer, responsible for the development, evolution and support of the backend services.
* Product Owner, responsible for the definition and guidance of the business definitions and backlog priorization.
* Architect, responsible of ensure that the development activities are compliants with the architecture definition, enabling a feedback loop as needed.
* Agile Coach, who is in charge of the agile ceremonies that enable team collaboration.
* OPS, in charge of the opperation of the infrastructure, enabling of the developer platform and support for the deployment of changes.
* Quality engineer, responsible for quality assurance. 

When the business and platform requirements increase in complexity, it will be possible to add a platform team to support the application lifecycle, or divide the single Strem-aligned team into several, with the following division, for example one Stream-aligned team for Civilian-oriented features, and another Stream-aligned team for non-civilian-oriented features, as shown below.

![Team Topologies v2.0](/Assets/TeamTopologies-V2.0.png "Evolutionary Team Topology")

As we can see, the roles are the same as in the version 1.0 (but for sure we need more people energizing them!). This type of organization enable a team evolve as the platform increase the complexity.

## Resources

### Archimate

This architecture and the related decisions was based on [Archimate](https://www.opengroup.org/archimate-forum/archimate-overview), the Open Group Architecture Modelling Language, using the open source tool [Archi](https://www.archimatetool.com/download/). 

The model was versioned in this repo (folder /model). To connect Archi with this repo and pull the [model](/model), you can use the [Collaboration plugin](https://www.archimatetool.com/plugins/#coArchi) for Archi.

Additionally, we provided an HTML view of the model, in the folder [htmlModel](htmlModel).

## Architecture Decision Records

* [ADR Infrastructure](./ADRs/adr-infrastructure.md)
* [ADR Cloud](./ADRs/adr-cloud.md)
* [ADR Mobile Technology](./ADRs/adr-mobile-technology.md)
* [ADR Web Technology](./ADRs/adr-web-technology.md)
* [ADR Backend Runtime](./ADRs/adr-containers-runtime-service.md)
* [ADR Backend Architecture Model](./ADRs/adr-backend-runtime-model.md)
* [ADR Backend Technology](./ADRs/adr-backend-technology.md)
* [ADR Messaging mechanism](./ADRs/adr-messaging-mechanism.md)
* [ADR IDP Platform](./ADRs/adr-idp-platform.md)
* [ADR Notification mechanism](./ADRs/adr-notification-mechanism.md)
* [ADR Observability platform](./ADRs/adr-observability-platform.md)
* [ADR Analytics](./ADRs/adr-analytics.md)
* [ADR Rule Engine](./ADRs/adr-rule-engine.md)
* [ADR Finance and Treasury](./ADRs/adr-finance-treasury.md)
* [ADR HR](./ADRs/adr-hr.md)
* [ADR Code Repository](./ADRs/adr-code-repository.md)
* [ADR Document Management](./ADRs/adr-document-management.md)
* [ADR Mailing](./ADRs/adr-mailing.md)