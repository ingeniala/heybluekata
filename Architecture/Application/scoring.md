# Scoring

## Description

Scoring module will be in charge of receiving all transactions between entities, that means:

- interactions between civilians and police officers
- donations to a charity or family in need
- giveaways between police officers
- exchanges (points-to-goods)

Therefore this component has an exposed API to receive that information.

Every kind of transaction relies on certain rules to be applied, rules that exist in another module so it will be an integration between them (synchronous API call).
Those rules (and its conditions) are applied to the supplied information so the platform can do the math and check how many points are assigned to each transaction party.

Then both results are stored on a per-user balance store, which will hold the points balance for every user in the system. 

Finally, every transaction needs to be informed and archived so it is published to the topic within the broker.

## Technology
More info about technology concerns in [Technology](/Architecture/Technology/scoring.md)