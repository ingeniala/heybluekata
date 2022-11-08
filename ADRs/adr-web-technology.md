# Web Technology

## Summary

The frontend layer, in this case the web module, helps to expose the business capabilities of the solution in an easy, user-friendly way so the users can have a nice experience, creating an unbreakable user-application bind. Defining the technology to build that layer is definitely essential.

### Alternatives

- React
- Angular
- Vue
- Backbone

## Decision 

Alternative selected: *React*

Following table contains all the reasons that drive us to make the decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Control of the market    | Widely used in the IT industry compared with the other options: https://npmtrends.com/angular-vs-backbone-vs-react-vs-vue. |
| Adoption                 | Widely adopted by the community. | 
| Reutilization 		   | Shared components with React Native ([ADR Mobile Technology](./adr-mobile-technology.md)). Due to react native relying on React features, there could be reutilization code also with the mobile module.      									|
| Usability          	   | Easy to learn and use: a developer with a background in javascript can easily learn and start with React. |
| Reutilization            | Components reutilization: An React App is based on components which could be reused in the whole app, also these components could be reused by mobile app [ADR Mobile Technology](./adr-mobile-technology.md). |
| Usability                | Easy to test. |
| Loyalty                  | Created and maintained by Facebook. |
| Maturity				   | Used by gigants on the market like: Netflix, Airbnb, Asana, Pinterest and more. |
| Cost					   | Save money: React is widely used, so it's quite easy to find developers within the community |

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | Save money: React is widely used, so it's quite easy to find developers within the community |
| CONS.02 | With this decision the solution will be web |
| CONS.03 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.06 | The web solution can start with little effort and grow in complexity when nedded |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.USA.01 | React supports Material Design using [MDB](https://mdbootstrap.com/docs/react/) |
