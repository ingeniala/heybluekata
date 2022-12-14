# Document Management

## Summary

A lot of functionality in a startup depends on business document management. A core decision of the architecture is how to manage this documents in a good way.

### Alternatives

- GSuite
- Office 365

## Decision 

Alternative selected: GSuite

The team chooses GSuite over Office 365 due to easy of deploy, manage and use. And due to its community support to solve issues and to manage startups issues with templates in an easy way.

## Constraints mapping

| Constraint ID | Explanation |
| ------------- | ----------- |
| CONS.01 | GSuite has plans for [non-profit organizations](https://www.google.com/nonprofits/) |
| CONS.03 | There were no restrictions, except for those defined here, about technology related decisions |
| CONS.06 | GSuite is a good option to evolve in complexity as needed, starting with something simple and evolve to an enterprise solution when it would be needed |
| CONS.07 | Gsuite is compliant with [GDPR](https://cloud.google.com/privacy/gdpr) |

## Architecture Characteristics Mapping

| Characteristic ID | Explanation |
| ------------- | ----------- |
| AC.STA.01 and AC.STA.02 | Google defines a minimum uptime of 99.99% with penalties |
| AC.SCA.01 | Google, as a cloud solution enables to start with the few resources as possible |