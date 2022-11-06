# Web Technology

## Summary

The project has an relevant component: web application, so it's necessary define the technology to develop it.

### Alternatives

- React
- Angular
- Vue
- Backbone

## Decision 

Alternative selected: *React*


Folowing table contains all reasons that drive us to make previos decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Control of the market    | Widely used in IT world, comparing with the other options: https://npmtrends.com/angular-vs-backbone-vs-react-vs-vue.              												                                 |
| Adoption                 | Widely adopted by the community. 																	   | 
| Reutilization 		   | Share components with React Native ([ADR Mobile Technology](./adr-mobile-technology.md)). Due to react native having a base on React we could have reutilization code also with the mobile module.      									|
| Usability          	   | Easy to learn and use: a developer with a background in javascript can easily learn and start with React.				  																											   |
| Reutilization            | Components reutilization: An React App is based on components which could be reused in the whole app, also these components could be reused by mobile app [ADR Mobile Technology](./adr-mobile-technology.md).                              |
| Usability                | Easy to test.                                   |
| Guarranty                | Created and maintained by Facebook.                             									   |
| Maturity				   | Used by gigants like: Netflix, Airbnb, Asana, Pinterest and more. 									   |
| Cost					   | Save money: due is widely used. It's easy to find developers who want develop on React 		       |

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | Save money: due is widely used. It's easy to find developers who want develop on React |
| CONS.02 | With this decision the solution will be web |
| CONS.05 | We decided the technology without restrictions except those defined here |
| CONS.06 | The web solution can start little and grow in complexity when nedded |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.USA.01 | React supports Material Design using [MDB](https://mdbootstrap.com/docs/react/) |
