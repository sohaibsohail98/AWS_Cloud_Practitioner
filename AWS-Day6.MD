## EC2 Pricing Models:

### Introduction:

Four ways to pay EC2 - **On-Demand, Spot, Reserved and Dedicated**:

**On Demand** - used by default, no up-front payment and no long-term commitment - charged by minute or hour. Mostly used for workload which is short-term, spikey, or unpredictable. A new app for development, or running an experiment.
 
**Reserved Instances:** Best long term savings, applications that steady-state, predictable usage or require reserved capacity. When you commit to a specific time to AWS, they provide you with savings. It is based on three variables: Term, Class Offering and Payment Option. 
 
 For payment options: 
 - Standard - Up to 75% reduced pricing compared to on-demand. Cannot change RI attributes (Instance type).
 - Convertible - Up to 54% reduced pricing compare to on-demand. Can change RI Attributes if greater or equal in value (change the instance size to a larger size).
 - Scheduled - You reserve instances for specific time periods eg: once a week for a few hours (very predictable). Savings can vary.
 
 Term: 
 - How long you are willing to commit? The greater the term, the greater the savings - Commit to 1 or 3 year contracts. 
 
 Payment options: Upfront, partial upfront and no upfront. Greater upfront, greater savings.
 
- Reserved Instances can be shared between multiple accounts within an organisation.
 
- Unused RIs can be sold in the Reserved Instance Marketplace


**Spot Instances**:

 - Biggest savings - 90% compared to on-demand pricing. 
 
 - Unused compute capacity - want to maximise the utility of their idle servers. For example, a hotel runs a sale to utilise their vacant suites. 
 
 - However, there is a tradeoff. These servers can be terminated at any time, if the computing capacity is needed by on-demand customers. Will not charge for the partial hour it was used.
 
 - It is designed for applications that have a **flexible start and end times** or applications that only feasible at **very low compute costs**.
 
 - If the user terminates an instance, he/she will be still charged for any hour it was running.
 
 Note: AWS Batch is an easy and convenient way to use Spot Pricing.
 
 <img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSSpotDefinitions.png" height="200" width="550"/>
 
 
**Dedicated**: 
 
 - Dedicated Host Instances - designed to meet regulatory requirements, have struct server-bound licencing that won't support multi-tenancy or cloud deployments. 
 
 **Multi-Tenant vs Single Tenant:** 
 
 **Multi-Tenant:**
 
 - Sharing the same hardware as other AWS customers. Running workloads on the same hardware. Virtual Isolation is what separates customers - software.
 
 **Single Tenant:** 
 
 - Single customer has dedicated hardware - Physical Isolation is what separates customers. 
 
 - Enterprises and Large organisations may have **security concerns or obligations** against sharing the same hardware with other AWS Customers.
 
 - Dedicated Host Instances - offered in both On-Demand and Reserved (70% off on-demand pricing)
 
 ### EC2 Pricing Cheatsheet:
 
 EC2's 4 pricing models: On-Demand, Spot, Reserved Instances (RI) and Dedicated.
 
 **On-Demand (least commitment)** - 
 
 - low cost, flexible, pay only by hour, 
 - Use case: short term, spiky, unpredictable workloads, first time apps
 - Ideal for when workloads cannot be interrupted
 
 
**Reserved Instances** - up to 75% off (Best long-term value)

- Use case: steady state or predictable usage
- Can resell unused reserved instances (Reserved Instance Marketplace)
- Reduced Pricing is based on Term, Class Offering, Payment Option

- Terms: 1 or 3 year
- Payment Options: All or partial upfront, or no upfront
- Class Offerings: 
Standard - 75% reduced pricing compared to on-demand - Cannot change RI Attributes.
Convertible - Up to 54% reduced pricing compare to on-demand. **You can** change RI attributes are greater or equal in value. 
Scheduled - Instance reserved for specific time periods. Once a week for a few hours. Savings may vary.

**Spot Pricing** - Up to 90% off biggest savings

- Request spare computing capacity, flexible start and end times.
- Use case: It can handle interruptions - server randomly stopping and starting.
- Use case: For non-critical background jobs.
- Instances can be terminated by AWS at anytime. 
- If your instance is terminated by AWS, you don't get charged for a partial hour of usage. 
- If you terminate an instance, that hour will still be charged while it was used.

**Dedicated Hosting** (Most Expensive):

- Dedicated servers, can be on-demand or reserved (up to 70% off)
- Use case: Need a guarantee of isolate hardware (enterprise requirements)

## Billing and Pricing:

### **Free Services**:

- Some AWS services are free, however, the resources they use will cost you.

For example: Auto-scaling, CloudFormation, Elastic Beanstalk, Opsworks, Amplify, AppSync, CodeStar - these are free, they can provision AWS services which cost money. Amazon VPC, IAM - Identity Access Management, Organisations and Consolidated Billing and AWS Cost Explorer are also free to use.

### **AWS Support Plans**:

Four different support plans: Basic, Developer, Business, Enterprise

- [Free] Basic - email support only, for billing and account. - 7 advisor checks
- Developer - no third party support. $20/ month - 7 advisor checks
- Business - $100/month - All trusted advisor checks
- Enterprise - $15,000/ month - All trusted advisor checks

Features enabled to each support plan:

- **Tech support via Email, 24 hours until they reply.** - Developer, Business, Enterprise 

- **General guidance (less than 24 hours) and system impaired (less than 12 hours)** - Developer, Business and Enterprise.

- **Tech support via chat, Phone - anytime 24/7, Production System Impaired (Less than 4 hours), Production System Down! (Less than 1 hour)** - Business and Enterprise only. 

- **Exclusively for Enterprise only**: Business-critical system down (less than 15 minutes), personal concierge and TAM - Technical Account Manager. 

### Let's create support case:

- Visiting the support page within AWS and creating a case with specific details allows to log and fix issues via email (for free tier) or alternative contact methods. 

- A case with technical support - can be useful if you are having issues with a specific AWS service. 

### AWS Marketplace:

- A digital catalogue with thousands of software listings from independent software vendors. 

- Easily find, buy, test and deploy software that already runs on AWS. 

- Product can be free to use or have an associated charge. The charge becomes part of your AWS bill, and once you pay, AWS Marketplace pays the provider. 

- The sales channel for ISVs and Consulting partners allows - sell your solutions to other AWS customers.

- Products can be offered as:
AMIs (Amazon Machine Images), AWS CloudFormation templates, Software as a serviced (SaaS) offerings, Web ACL, AWS WAF rules.

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSMarketplace.png" height="200" width="550"/>

### Marketplace Subscription:

- You can use AMIs and other tools when creating a new instance from the AWS marketplace. This is useful when you want to use a service which connects with AWS instances. A screenshot is shared to show how it would look like.

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSInstancewithMarketplace.png" height="200" width="550"/>
 
- This will allow the user to select the relevant AMI and open an instance using it. Most of these AMIs will be charged at a hourly rate so it's important to keep an eye out.

### AWS Trusted Advisor:

- Advises on security, **saving money**, performance, service limits and fault tolerance. - automated checklist of best practices on AWS. 

- It's free - comes with 7 Trusted Advisor Checks

- Business and Enterprise - get all Trusted Advisor Checks.

There are several advisories however, we will be focusing on the key ones:

Cost Optimisation:

- Idle Load Balancers - Loading up a Elastic Load Balancer has a minimum cost of $15/month. If there are no EC2 instances being balanced, it will recommend to terminate this load balancer as it's not doing anything. Saving the user money.

- Unassociated Elastic IP Addresses - EC2 Instance that has a static IP, you can reserve an IP from AWS.  Get rid of it to save money.y 

Performance:

- High Utilisation Amazon EC2 Instances - Very high CPU usage on the instance. Maybe use a larger instance to increase performance.

Security:

- MFA on Root Account (Multi-Factor Authentication)

- IAM Access Key Rotation - Keys used by users are rotated.

Fault Tolerance:

- Amazon RDS Backups - This makes sure that if databases goes down, the user can recover them with backups. 

Service Limits: 

- AWS allows you to increase the limits. For example, SES allows you to send emails, normally caps at 5000 emails. If the user needed to go beyond that, a service limit would be requested. 

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSTADashboard.png" height="200" width="550"/>

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSTACostOptimisation.png" height="200" width="550"/>

These are some screenshots of how it can appear for service limits.

- Reports can be downloaded in excel. 

- Preferences can be set - weekly emails to keep up to date with AWS Trusted Advisor status, any changes with recommended cost-savings.

### Consolidated Billing:

- One bill for all of your accounts

- Consolidate - Billing and payment methods **across** multiple AWS accounts into one bill. 

- For billing - AWS treats all the accounts in an organisation - into one account.

- User can designate one **master account that pays the charges** of all the other member accounts.

- Consolidated billing is free - offered at no additional cost.

- Use Cost Explorer - to visualise usage for consolidated billing.

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSConsolidatedBilling.png" height="200" width="550"/> 

