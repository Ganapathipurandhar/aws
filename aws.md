### what is cloud?
* cloud computing is a on-demand delivery of computing resourses like ec2, storage and infrasturcture over the internet. by pay-as-you-go model, without any operational, management overhead

### public and private cloud?
**Public cloud** : in public , we have the complete access on the services but cloud provider manage the services
**private cloud** : were as in private cloud --> services are manage by organization itself [in aws there have concept of VPC [ it is an logical isolation, it acts as private cloud--> suitable for sensitive data like banking etc] 

### Why Public Cloud is Popular?
Reduces overhead by outsourcing infrastructure management,Pay-as-you-go pricing model.Accessibility and scalability without significant upfront investment. [reduces operational, management overhead]

**Cloud repatriation** is the process of moving workloads from public cloud environments back to on-premises or private infrastructure. Organizations choose repatriation to optimize costs, enhance data security and compliance, reduce latency, address vendor lock-in concerns, and better manage predictable workloads.

However, it comes with challenges like high initial costs, migration complexity, a potential skills gap, and limited scalability compared to the cloud. Many companies adopt hybrid cloud strategies to balance the benefits of on-premises systems and public clouds. Industries like banking, healthcare, and manufacturing often lead this trend due to security, compliance, and performance needs.
[but it very minium 1 or 2%]

# IAM(Identity and Access Management)
                          --> IAM esure the authentication and authorization of services
authentication (who you are)

authorization (what you can do)

## IAM Components

Users: Individual identities requiring access. --> authentication
Groups: Collection of users with shared permissions.[team in the company]
Policies: Define specific permissions and actions users/groups can perform.--> authorization  [Custom policies: visual , json tamplate :Effect": "Allow",Action": [], Resource": []]
Roles: Temporary permissions for AWS resources or cross-account access. 
### example:
A DevOps engineer creates an AWS account and avoids sharing root access.
IAM users are created with limited permissions based on roles (e.g., read-only access to a database or S3 bucket, access only a specfic services etc).

## Why IAM is Crucial?
Prevents unauthorized access and accidental data deletion.Simplifies management of permissions via groups and policies.
## Custom Policies and Managed Policies
AWS provides managed policies for common use cases. Custom policies can be written in JSON format for specific needs.


