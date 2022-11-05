# O'Reilly Architectural Katas - Fall 2022 - HeyBLue

## Table of Contents

* [About Los Ingenials](#about-los-ingenials)
* [Glossary](#glossary)
* [Prelude](#prelude)
* [Functional requirements](#functional-requirements)
* [Quality Attributes](#quality-attributes-aka-architecture-characteristics)
* [Restrictions](#restrictions)
* [Assumptions](#assumptions)
* [Architecture](#architecture)
    * [Bussiness Collaboration View](#business-collaboration-view)
    * [Application Component Collaboration View](#application-component-collaboration-view)
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
* Driver: represents an external or internal condition that motivates an organization to define its goals and implement the changes necessary to achieve them
* Goal: represents a high-level statement of intent, direction, or desired end state for an organization and its stakeholders.
* IRS: Internal Revenue Service.

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

![Figure 1.1 - Motivation](/images/1.1.Motivation.png "Figure 1.1. - Motivation")

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

## Quality Attributes (AKA Architecture Characteristics)

## Constraints

## Assumptions

* IRS give information through API or file sharing. that let know when an organization is a charity organization. 
* A state department inform, through API or file sharing, what are the family in needs.
* A family in need can redeem their points but can't donate it.
* Retail can only use Web channel.
* Hey Blue will hire employees or contractors to support its operation.
* If Hey Blue obtain financing from investors, they want to know the performance of the organization.
* Hey Blue will have a minimal IT team to maintain the application, supported by automated tools.
* Hey Blue need to avoid risks associated with the business operation.


## Architecture

### Business Collaboration View

### Application Component Collaboration View

### Technology & Deployment View

## Evolution Roadmap

## Adoption Practices

## Team organization

## Resources

### Archimate

This architecture and the related decisions was based on [Archimate](https://www.opengroup.org/archimate-forum/archimate-overview), the Open Group Architecture Modelling Language, using the open source tool [Archi](https://www.archimatetool.com/download/). 

The model was versioned in this repo (folder /model). To connect Archi with this repo and pull the [model](/model), you can use the [Collaboration plugin](https://www.archimatetool.com/plugins/#coArchi) for Archi.

Additionally, we provided an HTML view of the model, in the folder [htmlModel](htmlModel).

## Architecture Decision Records

* [ADR Infrastructure](./adr-infrastructure.md)
* [ADR Cloud](./adr-cloud.md)
* [ADR Mobile Technology](./adr-mobile-technology.md)
* [ADR Web Technology](./adr-web-technology.md)
* [ADR Backend Runtime](./adr-backend-runtime.md)
* [ADR Backend Architecture Model](./adr-backend-architecture-model.md)
* [ADR Backend Technology](./adr-backend-technology.md)
* [ADR Messaging mechanism](./adr-messaging-mechanism.md)
* [ADR IAM Tool](./adr-iam-tool.md)
* [ADR Notification mechanism](./adr-notification-mechanism.md)
* [ADR Observability platform](./adr-observability-platform.md)
