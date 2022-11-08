# Tracking

## Description

One of the core capabilities of the solution, to keep track of the whole list of users and notify them based on proximity so they can interact with each other (civilians with police officers).

There are two main use cases to contemplate:

- every user sending their location frequently, so the system can track everyone’s location and figure out who is near who
- the system notifying a certain person (let’s say civilian) every time a police officer is nearby (it can be defined based on business conditions: radius, range, movement speed, etc), so they can meet and earn some rewards (points).

Main driver of this scenario is to be able to build it fast, which means no need to reinvent the wheel in terms of proximity algorithms, and try to be accurate according to precision.
Integrating with external location platforms and calculating based on GIS parameters does not seem to be the best approach to take.

Of course, mobile integration is quite a driver as well, as this feature is basically mobile-based.

This being said, and in order to delegate to the underlying cloud as much of the effort as possible to make this happen, the team decided to stick with AWS stack which is highly compatible with mobile devices (and the toolkit used to build them in the cloud) and it can also handle notifications based on proximity, which was a must-have in the solution.

## Technology
More info about technology concerns in [Technology](/Architecture/Technology/tracking.md)