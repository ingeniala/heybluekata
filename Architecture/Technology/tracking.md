# Tracking

## Runtime

Runtime layer consists in 2 layers:

- AWS Location Services which will handle all the stuff related to proximity calculation, geofences, geolocation, etc.
- A lambda function in charge of notifying the end user about people around him/her; and keep track of recent locations corresponding to the list of devices connected to the platform. 

## Storage  

This module will store information about the list of devices submitting GPS localization and how it changes in time. Once again, this unstructured data will live in DynamoDB. 