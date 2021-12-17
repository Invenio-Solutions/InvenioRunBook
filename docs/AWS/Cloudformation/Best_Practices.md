**Designing the Stack Template**

- Leave credentials out of your templates.  Instead, use dynamic references, like AWS Secrets Manager.
- Store Non-Confidential Parameter in AWS Systems Manager Parameters Store.
- Add Comments and background Section using MetaData Tag, which can be added to every resource you create.
- Validate your template with AWS CloudFormation, before creating or updating a stack, to ensure it consists of valid JSON or YAML without syntax or semantic errors. 
- Use tools like AWS CloudFormation Guard (cfn-guard) and cfn-nag to check your template for policy compliance issues or security vulnerabilities, respectively.
- Use cross-stack references to export resources from a stack so that other stacks can use them.
- Ensure that stack can create all the required resources without hitting the AWS account limits.
- Use Modular Approach to design templates. Use nested stack, and stack replication features to make templates reusable.

**Testing the templates**

- Test your AWS CloudFormation templates periodically to ensure that they continue to work as expected. Incorporate new service functionality as it becomes available.
- Use TaskCat to test any template that you create. TaskCat automatically deploys your templates, logs the result of the deployment, and deletes any asset that were deployed.

**Resources**

- Read and install [TaskCat](https://aws-ia.github.io/taskcat/) here.

- [AWS Documentation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html)

- https://jayendrapatil.com/aws-cloudformation-best-practices-certification/

- https://aws.amazon.com/blogs/infrastructure-and-automation/best-practices-automating-deployments-with-aws-cloudformation/
