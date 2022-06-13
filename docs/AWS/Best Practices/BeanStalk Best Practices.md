---
sidebar_position: 8
---
**Security**

- Implement least previlege access - only giving access to resources it needs - policy using Identity Access Management(IAM). Create IAM users for each person who uses Elastic Beanstalk to avoid using your root account or sharing credentials.
- Use proper Tags for each resource you create in order to provide better clarity. 
- Enable AWS Config on your BeanStalk to define rules that evaluate resource configurations for data compliance. AWS Config rules represent the ideal configuration settings for your Elastic Beanstalk resources. If a resource violates a rule and is flagged as noncompliant, AWS Config can alert you using an Amazon Simple Notification Service (Amazon SNS) topic.
- Monitor your Elastic Beanstalk solutions using:
    - <u>Amazon CloudWatch</u> metrics for Elastic Beanstalk – Set alarms for key Elastic Beanstalk metrics and for your application's custom metrics
    - <u>AWS CloudTrail</u> entries – Track actions that might impact availability, like `UpdateEnvironment` or `TerminateEnvironment`.
- To protect information flowing between your application and clients, configure SSL. When you configure an SSL certificate for your environment, data is encrypted between the client and your environment's Elastic Load Balancing load balancer.
- Enforce IMDSv2 on environment instances. IMDSv2 uses session-oriented requests and mitigates several types of vulnerabilities that could be used to try to access the IMDS, and is thus more secure.
