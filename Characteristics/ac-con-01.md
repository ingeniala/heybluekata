# AC.CON.01 - Limited ammount of connections

## Description

Members of the community can only have one connection per officer per 24 hours period.

## Detailed definition

| *Source* | Civilian |
| *Stimulus* | Trying to connect with a police officer |
| *Environment* | Production, normal conditions |
| *Impacted Artifacts* | Rules engine |
| *Respond* | Enable only the first connection each day (begining at 0:00) |