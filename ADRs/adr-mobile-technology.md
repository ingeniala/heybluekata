# Mobile Technology

## Summary

The frontend layer, in this case the mobile module, helps to expose the business capabilities of the solution in an easy, user-friendly way so the users can have a nice experience, creating an unbreakable user-application bind. Defining the technology to build that layer is definitely essential.

### Alternatives

- React Native
- IOS and Android native
- Flutter

## Decision 

Alternative selected: *React Native*


Following table contains all the reasons that drives the decision:

| Criteria                 | Description
| --------------------     | ----------------------------------------------------------------------------------------------------- |
| Portability | Write once, run on both Android and IOS. With React native is possible to only have a single codebase for every mobile device, reutilizing the code and avoiding the situation of particular codebases (Android and IOS) like when using native development suite |
| Cost                     | It's not necessary to have 2 teams with different knowledges in charge of the mobile app development. Not to mention that developers for both native IOS Android are scarce in the market, and they are more expensive than react native ones. |
| Reutilization | Shared components with React ([ADR Web Technology](./adr-web-technology.md)). Due to react native relying on React features, there could be reutilization code also with the web module. |
| Time to market           | Due to having only a single codebase, Time-to-market turns to be the same in both platforms. |
| Loyalty                  | It was created by Facebook. |
| Costs                    | Save money: React Native is widely used, so it's quite easy to find developers within the community |
| Community                |  Wide acceptance by the community, with a high collaboration in the development of libraries. |
| Maturity | Used by gigants on the market like: Skype, Walmart, Instagram, Tesla and more, unlike others like flutter who are not that adopted. |

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | Save money: React Native is widely used, so it's quite easy to find developers within the community |
| CONS.02 | With this decision the solution will be mobile |
| CONS.03 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.06 | The mobile solution can start with little effort and grow in complexity when nedded |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.USA.01 | React supports Material Design using [MDB](https://mdbootstrap.com/docs/react/) |