# Business Rules

## Description

Reference Architecture describes that not only redemptions but also encounters between users may have rules defined by the business in order to establish the amount of points to give to every party in the transaction.

All those rules are handled by a single component, as shown in the technical architecture, and can be changed/adjusted by using a web client. 

Technically speaking, this component will expose basically three APIs:

- creating rules, which can be done by using a web client
- editing/patching rules, same as before
- fetching existing rules and their config, which will be required specially by other components on the solution (CMS & Scoring) so they can operate as expected. 

## Technology
More info about technology concerns in [Technology](/Architecture/Technology/business-rules.md)