# AC.SEC.01 - Secure Information

## Description

The application must protect user data, considering what data is stored and what data is transient, including:

* Data at rest must be encripted using AES 256
* All data on transit will be encripted using at least TLS 1.3
* All secrets must be stored and managed using only key managers

## Detailed definition

| Aspect   | Value           |
| -------- | --------------- |
| *Source* | New piece of data |
| *Stimulus* | New information is generated |
| *Environment* | Production, normal conditions |
| *Impacted Artifacts* | All components |
| *Respond* | Only store the information not marked as transient. |