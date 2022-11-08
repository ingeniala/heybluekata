# Tracking

## Runtime

Runtime layer consists in 2 layers:

- AWS Location Services which will handle all the stuff related to proximity calculation, geofences, geolocation, etc.
- A lambda function in charge of notifying the end user about people around him/her; and keep track of recent locations corresponding to the list of devices connected to the platform. 

## Storage  

This module will store information about the list of devices submitting GPS localization and how it changes in time. Once again, this unstructured data will live in DynamoDB. 

## Technology Views

For simplicity, it is provided two kinds of views. A simplified view generated using draw.io view that tells the story in a easier way, and the archimate view, useful for analytics purposes.

### Simplified view

![Drawio Tracking](/Assets/drawio-tech-tracking.png "Tracking in draw.io")

### Archimate View

![Archi Tracking](/Assets/HeyBlue-Tracking-Notification-Technology.png "Tracking in Archi")