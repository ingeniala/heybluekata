#ADR observability platform - Work in progress - formating
 
##Amazon CloudWatch

Based on the preview ADR: which Cloud? AWS CloudWatch is the best integrated solution to monitoring and observability tool
Easy to use and to visualize through dashboards
Pricing: Starting with the free tier, the price is the most economical and ties to the consumption as pay as you go.  
Collect: Near real-time logs and metrics from resources, applications and services 
Monitor: Provide dashboards and the possibility to create reusable graphs, alarming with configurable thresholds on metrics and triggering action based on it, correlate logs and metrics, integrated with EKS and k8s, monitor application endpoints and client side performance to enhance end users experience. 
Act: Based on the monitored metrics and logs, it is possible to automate actions like autoscaling and executing actions via lambda functions or alarming through SNS topics.
Analyze: CloudWatch can manage custom operations on metrics, log analysis including container and lambda metrics logs and traces, external custom metrics such us on-premise apps. 
