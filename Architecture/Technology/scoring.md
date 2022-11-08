# Scoring

## Runtime

In this scenario, the team decided to do this calculation on a lambda function to take advantage of the run-to-completion model and save some money by turning it off when there are no transactions to submit.

If the component turns out to be heavily accessed, then it can be kept warm under a time-based ping so cold starts are not a pain (https://acloudguru.com/blog/engineering/how-to-keep-your-lambda-functions-warm).

The code conforming this component will be python as well, global decision unless there is an exception or any other restriction to be aware of. 

## Storage

Team chose a key-value store to hold the user list and corresponding balance (amount of points). The model is straight-forward, unstructured and easy to represent, the low cost (a valuable free tier) and the speed on the access at scale are preferred (a user able to see current balance).  Mainly for these reasons, the team went with DynamoDB instead of other options (e.g. an Elasticache). Not to mention that Dynamo is already targeted by other modules so it won’t be a new service to hire.

## Technology Views

For simplicity, it is provided two kinds of views. A simplified view generated using draw.io view that tells the story in a easier way, and the archimate view, useful for analytics purposes.

### Simplified view

![Drawio Scoring](/Assets/drawio-tech-scoring.png "Scoring in draw.io")

### Archimate View

![Archi Scoring](/Assets/HeyBlue-Scoring-Technology.png "Scoring in Archi")