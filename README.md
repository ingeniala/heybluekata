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


## Quality Attributes (AKA Architecture Characteristics)

## Restrictions

## Assumptions

* IRS give information through API or file sharing. that let know when an organization is a charity organization. 
* A state department inform, through API or file sharing, what are the family in needs.
* A family in need can redeem their points but can't donate it.
* Retail can only use Web channel.


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
