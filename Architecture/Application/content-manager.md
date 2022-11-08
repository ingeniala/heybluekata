# Content Manager

## Description

As was described previously, the architecture has a Content Manager which main responsibility is manage static content of StoreFronts (for Marchants and Municipalities) and it has integraton with [Store Service](./store-service.md). The flow is described as follows:

- A webhook is triggered in Prismic every time a content is created/updated.
- That webhook arrives at the AWS API Gateway (HTTP API), which will then awake a lambda function.
- The lambda function will trigger a GitHub Action pipeline, which will build the Gatsby site and upload the generated static files (html) to S3 buckets.
- CloudFront distribution will allow exposition of the content in a distributed fashion, what is called a _CDN_.

## Technology
More info about technology concerns in [Technology](/Architecture/Technology/content-manager.md)