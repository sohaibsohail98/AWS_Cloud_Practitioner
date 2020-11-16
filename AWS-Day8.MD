## Technology Overview:

### AWS Organisations and Accounts:

- The first initial sign up account for AWS is known as the Root account, another name for the master account. 

- Under the master account, the user is able to create multiple accounts. These can be useful because in case you want to isolate different departments, and decide what each account has access to within AWS. 

- **Organisations** - centrally manage billing, control access, compliance, security and share resources across your AWS accounts. 

- **Root Account User** - single sign-in identity that has complete access to all AWS services and resources in an account. Each account has a Root Account user. 

- **Organisation Units** - group of AWS accounts within an organisation which can also contain other organisational units - creating a hierarchy. 

- **Service Control Policies** - give central control over the allowed permissions for all accounts in your organisation, helping to ensure user's accounts stay within the organisation's guidelines.  **These will apply rules to specific accounts about what services they can or cannot use.**

Below is a screenshot of how each functions works:

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSOrganisationsandAccounts.png" height="400" width="400"/>

### AWS Networking:

- Region - the geographical location of the user's network: For example: US-East1 or Canada

- AZ - the data centre of the user's AWS resources

- VPC - Virtual Private Cloud - logically isolated section of the AWS Cloud where the user can launch AWS resources.

- Internet Gateway - Enable access to the Internet

- Route Tables - determine where network traffic from your subnets are directed.

- NACLs - Acts as firewalls at the subnet level.

- Security Groups - Acts as firewall at the instance level

- Subnets - a logical partition of an IP network into multiple, smaller network segments. These are defined in an Availability Zone. The data centre within the AZ is located within a particular region.

- Public Subnet - accessible to the internet.

- Private Subnet - not accessible to everyone, limited access. 

Below is the screenshot of AWS Networking demonstrated visually:

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSNetworking.png" height="400" width="400"/>

- As seen from the screenshot, the EC2 Instance would use Internet Gateway. The subnet needs to know how to reach the internet gateway to access the internet, this is where Route Tables come in. The specific route within the **Route Table** is directed to make sure the **Public Subnet** access the **Internet Gateway**.

- The Security groups access firewalls at the instance level. In the screenshot, it shows that the security group is protecting the two instances.

- NACLs is another form of security - controls the Subnet levels of internet traffic.

### Database Services:

<img src="https://ccweb.imgix.net/https%3A%2F%2Fccweb.imgix.net%2Fhttps%253A%252F%252Fd3f1iyfxxz8i1e.cloudfront.net%252Fcourses%252Fcourse_image%252Fc777c0e091a7.jpg%3Fauto%3Dformat%26cs%3Dstrip%26fit%3D%26h%3D710%26ixlib%3Dphp-3.3.0%26w%3D400%26s%3D47c860fd5c0791cb256f0ce30ea35375?auto=format&ixlib=php-3.3.0&s=646d12671b17c41c7096bb8f638af9f5" width="100"/>

DynamoDB - NoSQL key/value database

<img src="https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/core-aws-services/manage-databases-on-aws/images/a5b15f3f330bed3cc5c6efb961c39c78_ce-457896-63-ab-423-a-ba-80-1153-aff-22-b-55.png" width="100"/>

DocumentDB - NoSQL Document database that is MongoDB compatible.

<img src="https://adityasdemos.com/en/Amazon-RDS_light-bg@4x.png" width="100"/>

RDS - Relational Database Service that supports multiple engines; such as MySQL, Postgres, Maria DB, Oracle, Microsoft SQL Server, Aurora
  
  - Aurora: MySQL (5x faster) and PSQL (3x faster) database fully managed.
  - Aurora Serverless - only runs when its needed, like AWS Lambda. 
  
  <img src="https://dbdb.io/media/logos/amazon-neptune.png" width="100"/>
  
  Neptune - Managed Graph database
  
   <img src="https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/core-aws-services/manage-databases-on-aws/images/d123b0f1fc502ce368484a93e76f6546_d-1-b-30237-d-3-cb-48-f-7-a-831-0520-f-9-bdfa-6-a.png" width="100"/>
  
  Redshift - Columnar database, petabyte warehouse (1000 TB - 1PB)
  
  <img src="https://42vnof42im1n3ecs8l2w7ez1-wpengine.netdna-ssl.com/wp-content/uploads/2020/07/Amazon-ElastiCache@4x-190x190.png" width="100"/>
  
  ElastiCache - Redis or, Memcached Database. 