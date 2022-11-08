# QR Generation

## Runtime

This component in charge of creating a distributable QR will need profile information (supplied by the mobile app) and then will return a base64 string conforming the QR image. 

So, it will expose an API and basically compute the QR, which will later return, a great fit for a **lambda function**.

It does not need to be running the whole time, actually. The trigger can be a request received and passed through the gateway, which will wake the lambda and order to execute. 

Because of costs, the team preferred to **develop this in-house** than integrating an external provider, which will add complexity in terms of establishing an egress connection, security, latency, parsing data, etc. On the other side, developing this feature by using a python module can be done easily in no more than 10-15 lines (https://towardsdatascience.com/generating-qr-codes-with-python-in-less-than-10-lines-f6e398df6c8b). 

## Storage  

N/A

## Technology Views

For simplicity, it is provided two kinds of views. A simplified view generated using draw.io view that tells the story in a easier way, and the archimate view, useful for analytics purposes.

### Simplified view

![Drawio QR](/Assets/drawio-tech-qr.png "QR in draw.io")

### Archimate View

![Archi QR](/Assets/HeyBlue-QR-Interaction-Technology.png "QR in Archi")