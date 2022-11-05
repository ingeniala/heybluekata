# Mobile Technology

## Summary

The project has an relevant component: mobile application, so it's necessary define the technology to develop it.

### Alternatives

- React Native
- IOS and Android native
- Flutter

## Decision 

Alternative selected: *React Native*


Folowing table contains all reasons that drive us to make previos decision:

| Criteria                 | Description                                                    
| --------------------     | ----------------------------------------------------------------------------------------------------- | 
| Portability 			   | Write once, run on Android and IOS, with React native is possible only have one base code for mobile, in this way we have a maximum reutilization code, because avoid the situation of base code for Android and base code for IOS, unlike with IOS and Android native              												                                           |
| Cost                     | It's not necessary 2 different teams in charge of development of mobile app. Also developers for native IOS and native Android are scarce in the market, and they are more expensive than react native ones.								| 
| Reutilization 		   | Share components with React ([ADR Web Technology](./adr-web-technology.md)). Due to react native having a base on React we could have reutilization code also with the web module.      													   |
| Time to market           | Due we have only one base code we have the same time to market in both platforms.					   |
| Guarranty                | It was created by Facebook.                                    									   |
| Costs                    | Pay as you go, reserved plans (in case of upfront needs)improving                                     |
| Community                |  Wide acceptance by the community, with a high collaboration of the community in the development of libraries.                             																							|
| Maturity				   | Used by gigants like: Skype, Walmart, Instagram, Tesla and more, unlike flutter who isn't widely adoption.  				   															   								             | 
