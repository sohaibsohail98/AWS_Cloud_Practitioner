## Continuing Billing and Pricing 

### AWS Budgets:

- Plan your service usage, service costs and instance reservations. 

- The first two budgets are free, each budget is $0.02 per day, less than $0.60 a month, 20,000 budgets limit. 

- AWS budgets - ability to setup alerts if the user exceed or are approaching your defined budget.

- Create **cost**, **usage**, **reservation** budgets (reserved instances)

- Tracked at monthly, quarterly or yearly levels with customisable start and end dates.

- Alerts support EC2, RDS, Redshift and ElastiCache reservations.

- Budgets are based on a fixed cost - upfront can be planned based on the user's chosen level. For the next 6 months, plan how much cost the user wants to allocate for each month.

- Easily managed by AWS Budgets dashboard or via the Budgets API.

- **Get notified** via email or Chatbot, how close to the current or forecasted budget.

### TCO Calculator

- The total cost of ownership - estimate how much a user would save when moving to AWS from on-premise.

- Provides you with - detailed set of reports, it would be used in executive presentations

- Built on underlying calculation models - this generates fair assessments of value that you can achieve given the data provided. 

- This TCO helps by reducing the need to invest in large capital expenditures. 

- Tool is for approximation purposes only.

Launching the TCO calculator:

1. Describe the user's environment.
2. View 3 year summary of cost comparisons.
3. Download a full detailed report.

### AWS Landing Zone:

- Helps enterprises quickly set-up a secure, AWS multi-account. Mainly for big businesses. 

- Provides user with a baseline environment to get started with a multi-account architecture - AWS recommends to these companies to run a multi-account but the company does not know how to approach this option the best way. Landing zone assists companies to setup multi-account architecture. 

- Ths is done through the AVM. 

- AWS Account Vending Machine (AVM) - automatically provisions and configure new accounts via Service Catalog Template.

- The accounts are accessed using single sign-on (SSO) for managing and accessing accounts. 

- Customisable environment, it allows customers to implement their account baselines through a Landing Zone configuration and update pipeline.

- Landing zone gives the user a baseline environment, allowing to adding additional accounts and security options.

### AWS Resource Groups and Tagging:

- **Tags** are words or phrases that act as metadata for organising user's AWS resources. 

- **Resource Groups** - collection of resources that share one or more tags. 

- Helps the user organise and consolidate information based on your project and the resources that you use. 

- Example: A database, a server and a EC2 Bucket, **to group them all together**, you would use the same tag and put them in a resource group.

- Resource groups - display details about a group of resource based on: Metrics, Alarms and Configuration Settings. 

- Resource group settings can be modified at any time, to change what resources appear. 

- To create a tag and link it to AWS Resource Groups is straightforward. 

- When launching a new instance, towards the end, it will provide the user option to add tags, this would be a key and value. Once this is listed. The AWS Resource groups page needs to be accessed, while creating a group, it would ask for the tags from the instance to be inserted. This will create a link between the two, and allocate the instances to the resource group.

- The tag editor allows the removal or addition of additional tags to the instances if needed. 

### AWS QuickStart:

- Prebuilt templates by AWS and AWS partners to help users deploy popular stacks on AWS. 

- Reduce hundreds of manual procedures into just a few steps. (In other words, automation)

Quick start is in 3 parts:

1. Reference architecture for the deployment - architectural diagrams and descriptions. 

2. **AWS CloudFormation** templates that automate and configure the deployment. These templates are used to provisioning AWS resources.

3.  A deployment guide explaining the architecture and implementation in detail. 

- Quick Start reference deployments, usually, allow spin up a full functional architecture in less than an hour!

- Each Quick-Start template has its own features, it may be able to offer different values, for example, a unique VPC, or offering more AZs. 

### AWS Cost and Usage Report:

- Generate a detailed spreadsheet, enabling the user to better analyse and understand AWS costs.

- Places the reports into **Amazon S3 Bucket**

- Use **Athena** to turn the report into a queryable database

- Use **QuickSight** to visualise user's billing data as graphics.

In the top right under the username, it would say Billing Dashboard, click on this. Under Cost and Usage reports, create a new report. 

- Using **Athena and QuickSight** to analyse this cost and usage report can be useful within AWS.



