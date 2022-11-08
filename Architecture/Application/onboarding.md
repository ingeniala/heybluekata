# Onboarding

## Description

This service will handle the business logic related to the onboarding process, no matter the entity. This means that not only a police officer or civilian will be able to use it but also the merchants, charitable organizations or families in need. Some of the entities will use the web client to signup and create a user account, and others (police officer,civilian) could use the mobile client.

This being said, this component will expose an API to receive the needed information to sign an user up, and of course interact with several components:

- First of all, a component in charge of validating the identity supplied by the user to be created. This is what’s been called an “ID validator” within the conceptual architecture diagram. Depending on the user kind (police officer or civilian, etc), this external provider will definitely vary.    
- Then, an identity provider where the user and its credentials are created after the conditions are met.

Eventually, when the user is finally created and credentials associated, the service will push an event to a broker (Kinesis DataStreams), so every component subscribed can be notified.

## Technology
More info about technology concerns in [Technology](/Architecture/Technology/onboarding.md)