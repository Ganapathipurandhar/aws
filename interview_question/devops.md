Here’s a list of AWS and DevOps interview questions along with concise, interview-ready answers:

1. **What is the role of IAM roles and policies?**

Answer:
IAM (Identity and Access Management) roles and policies define permissions for AWS resources.

Roles: Temporary credentials for AWS services or users to access resources.

Policies: JSON documents that specify what actions are allowed or denied on which resources.
Example: Assigning an EC2 instance a role to access an S3 bucket.

2. **Can you explain the Terraform plan and its purpose?**

Answer:
terraform plan is a command that creates an execution plan. It shows what changes Terraform will make to the infrastructure (e.g., create, update, or delete resources) without actually applying them. It helps in reviewing changes before deployment.

3. **What is AWS Lambda, and how does it work?**

Answer:
AWS Lambda is a serverless compute service that runs code in response to events (e.g., S3 uploads, API Gateway requests). It automatically scales and manages the infrastructure. You only pay for the compute time consumed.

4. **How do you invoke a Lambda function, and where do you configure it?**
Answer:
Lambda functions can be invoked:

Manually: Using the AWS CLI (aws lambda invoke).

Automatically: Via triggers like S3, DynamoDB, or API Gateway.
Configuration is done in the AWS Management Console, CLI, or SDKs.

5. **How does Lambda handle scaling and event-based invocations?**
Answer:
Lambda automatically scales by running multiple instances of the function in response to incoming events. Each event triggers a separate invocation, and Lambda handles concurrency limits.

6. **What is Amazon CloudWatch, and have you configured any custom metrics?**

Answer:
CloudWatch is a monitoring service for AWS resources and applications.

Custom Metrics: Yes, I’ve configured custom metrics (e.g., application-specific logs or performance data) using the PutMetricData API.

7. **What metrics are available on your CloudWatch dashboard?**
Answer:
Common metrics include:

EC2: CPU utilization, network in/out.

Lambda: Invocation count, error rate, duration.

RDS: Database connections, read/write latency.

8. **How do you configure CPU utilization on your CloudWatch dashboard?**
Answer:

Go to CloudWatch > Metrics.

Select the EC2 namespace.

Choose the instance and add the CPUUtilization metric to the dashboard.

9. **How do you attach an SSL certificate to an S3 bucket?**

Answer:
S3 itself doesn’t support SSL directly. To enable HTTPS:

Use CloudFront as a CDN in front of the S3 bucket.

Attach the SSL certificate to the CloudFront distribution.

10. **What type of encryption have you implemented in your project?**

Answer:

At Rest: S3 server-side encryption (SSE-S3 or SSE-KMS).

In Transit: SSL/TLS for data transfer.

Client-Side: Encrypting data before uploading to S3.

11. **If an S3 bucket has a read-only policy, can you modify objects in the bucket?**

Answer:
No, a read-only policy (s3:GetObject) only allows viewing/downloading objects. Modifying objects requires write permissions (s3:PutObject).

12. **Why did you choose Terraform over Boto3 for infrastructure provisioning?**

Answer:
Terraform is declarative and platform-agnostic, making it ideal for infrastructure as code (IaC). Boto3 is more suited for scripting and automation tasks in Python.

13. **What is a Content Delivery Network (CDN), and how does it work?**

Answer:
A CDN (e.g., Amazon CloudFront) distributes content to edge locations closer to users, reducing latency and improving load times. It caches static and dynamic content.

14. **Have you created a Jenkins pipeline for your project?**

Answer:
Yes, I’ve created Jenkins pipelines to automate CI/CD workflows. The pipeline includes stages like build, test, and deploy, defined in a Jenkinsfile.

15. **How do you attach policies to IAM users, either individually or by group?**

Answer:

Individually: Attach policies directly to the IAM user.

By Group: Add the user to an IAM group with the desired policies attached.

16. **What type of deployment strategies are you using in your project?**

Answer:

Blue/Green Deployment: Using AWS CodeDeploy to switch traffic between two environments.

Canary Deployment: Gradually rolling out changes to a small subset of users.

17. **Have you used any tools to create customized Amazon Machine Images (AMIs)?**

Answer:
Yes, I’ve used Packer to create custom AMIs with pre-installed software and configurations.

18. **What is connection draining, and how does it work?**

Answer:
Connection draining ensures that an ELB stops sending new requests to a deregistering instance but allows existing requests to complete. It prevents abrupt connection termination.

19. **How does an Elastic Load Balancer (ELB) distribute traffic?**
Answer:
ELB distributes traffic across multiple targets (e.g., EC2 instances) using algorithms like round-robin or least outstanding requests.

20. **What is auto-scaling, and how does it work?**

Answer:
Auto-scaling automatically adjusts the number of EC2 instances based on demand. It uses CloudWatch metrics (e.g., CPU utilization) to trigger scaling policies.

21. **Can you describe the different types of Load Balancers and provide examples?**

Answer:

Application Load Balancer (ALB): HTTP/HTTPS traffic (e.g., web apps).

Network Load Balancer (NLB): TCP/UDP traffic (e.g., gaming, low-latency apps).

Classic Load Balancer (CLB): Legacy, supports both HTTP and TCP.

22. **What is the maximum runtime for a Lambda function?**

Answer:
15 minutes (900 seconds).

23. **What is the maximum memory size for a Lambda function?**
Answer:
10 GB.

24.**How can you increase the runtime for a Lambda function?**
Answer:
You cannot increase the runtime beyond 15 minutes. For longer tasks, consider using AWS Step Functions or ECS.

25. **What automations have you performed using Lambda in your project?**

Answer:

Automating backups (e.g., snapshotting RDS instances).

Processing S3 uploads (e.g., resizing images).

Sending notifications via SNS.

26. **Why did you choose Terraform over Boto3 for infrastructure provisioning?**

Answer:
Terraform’s declarative approach and state management make it easier to manage complex infrastructure compared to Boto3’s imperative scripting.

27. **What modules have you used in your Lambda function?**

Answer:

AWS SDK (e.g., boto3 for Python).

Custom modules for logging, error handling, and API calls.

28.**Have you created an SNS topic for your project?**

Answer:
Yes, I’ve created SNS topics to send notifications (e.g., email, SMS) for events like CloudWatch alarms or Lambda function failures.

29. **If you’ve exhausted IP addresses in your VPC, how would you provision new resources?**

Answer:

Increase the CIDR range of the VPC.

Create a new subnet with a larger CIDR block.

Use a secondary VPC and peer it with the existing one.

30. **What is Groovy, and how is it used in Jenkins?**

Answer:
Groovy is a scripting language used in Jenkins pipelines. It allows defining complex workflows in a Jenkinsfile.

31. **Why do you use Groovy in Jenkins, and where do you save Jenkins files?**

Answer:
Groovy is used for its flexibility and integration with Jenkins. Jenkinsfiles are typically saved in the root of the repository.

32. **What is Ansible, and what is its purpose?**

Answer:
Ansible is a configuration management and automation tool. It uses YAML playbooks to automate tasks like provisioning, configuration, and deployment.

33. **What language do you use in Ansible?**

Answer:
YAML for writing playbooks.

34. **Where do you run Terraform code, remotely or locally?**

Answer:
Terraform code can be run locally or remotely (e.g., in a CI/CD pipeline or using Terraform Cloud).

35. **What is the purpose of access keys and secret keys in AWS?**

Answer:
Access keys and secret keys are used for programmatic access to AWS services via APIs, CLI, or SDKs.

36. **What are Terraform modules, and have you used any in your project?**

Answer:
Terraform modules are reusable configurations for infrastructure. I’ve used modules for VPC, EC2, and RDS setups.

37. **What environments have you set up for your project?**

Answer:

Development, Staging, and Production environments.

Each environment has its own VPC, subnets, and resources.

38. **Do you use the same AWS account for all environments?**

Answer:
No, I use separate AWS accounts for each environment to ensure isolation and security.

39. **Do you have separate Jenkins servers for each environment?**

Answer:
Yes, to avoid conflicts and ensure environment-specific configurations.

40. **Where do you write and save your Lambda function code?**

Answer:
Lambda function code is written in the AWS Management Console, IDE (e.g., VS Code), or uploaded via S3. It’s saved in a version-controlled repository (e.g., GitHub).