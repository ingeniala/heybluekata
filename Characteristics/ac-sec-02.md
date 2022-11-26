# AC.SEC.02 - End User AAA

## Description

The users of the application (Police officers, civilians, charity and business) must be properly authenticated to use the applications, and can only access the functionality and information that is allowed by their predefined profile using Role Based Access Control.

Every state change triggered by a user action must be logged on an audit trail.

## Detailed definition

| Aspect   | Value           |
| -------- | --------------- |
| *Source* | User |
| *Stimulus* | Want to access the platform |
| *Environment* | Production, normal conditions |
| *Impacted Artifacts* | Security components |
| *Respond* | Only authenticated users can access the platform, and only use the functionality them are allowed to. |