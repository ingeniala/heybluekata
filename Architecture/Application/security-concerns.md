## Description

This topic involves handling the security aspects of the whole solution.

Based on the [ADR Cloud Provider](/ADRs/adr-cloud.md), the team decided to stick to the AWS Well Architected Framework, following the [AWS Security Pillar](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/security.html).

The design principles include:

- **Implementing a strong identity foundation**: Well defined privileges for each kind of duty and appropriate authorization on each interaction with the AWS resources, centralizing the identity management. This is implemented on AWS IAM.
- **Enabling traceability**: This principle talks about the observability layer, monitoring, auditing, alerting. Metrics and logs are automatically investigated and derived into actions, many times automatically (e.g.: autoscaling). Following the [ADR observability platform](/ADRs/adr-observability-platform.md), this part will be implemented using [AWS CloudWatch](https://aws.amazon.com/cloudwatch/).  
- **Applying security at all layers**: Following this principle, our team defines a layer between the external requests and the internal application components, and between internal components as well. Technically speaking, security groups and network ACLs.
- **Automate security best practices**: Define a secured architecture and include versioned IaC templates to automate infrastructure allowing to scale faster and manage cost effectively.
- **Protect data in transit and at rest**: Define the data sensibility levels and apply the mechanisms to ensure the information when it’s needed.  
- **Keep people away from data**: Minimize the needs of accessing the data, automatize the data processing to avoid manual intervention procedures.
- **Prepare for security events**: Be prepared for an incident, use an incident management tool and processes aligned with the organization model.

As part of this pillar (figure 10.14.1), AWS will be responsible for the security **of** the cloud, while the customers will be responsible for the security **in** the cloud.

![Figure 10.14.1 - Security Pillar](/Assets/security-pillar.png "Figure 10.14.1 - Security Pillar")
