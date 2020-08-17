## What is AWS Global Infrastructure:

### Introduction and Map Overview

**Where does all this Cloud Computing run?**

**69 Availability Zones within 22 Geographic Regions**

**Many more Edge Locations than AZs**

AWS serves - more than a million customers in more than 190 countries. 

Expanding global infrastructure to help customers **achieve lower latency and higher throughput**.

**Regions** (22) - Physical location in the world with multiple Availability Zones. 

**Availability Zones** - One or more discrete data centres owned by AWS. 

**Edge Location** - Datacentre owned by a trusted partner of AWS. 

**Regions:**

- A geographically distinct location which has multiple datacentres (AZs).

- Every region is physically isolated and independent of every other region in terms of location, power, water supply. 

- Each region has atleast two AZs (Data-centres). 

- AWS largest region is **US-EAST, North Virginia**

- New services almost always become available first in **US-EAST**.

- Not all services are available in all regions - usually new features of AWS, it's recommended to switch to **US-EAST** region.

- **US-EAST-1** is the region where you see all your billing information.

- North Virginia, Ireland and Singapore consist with the most AWS services available according to each region.

**Availability Zones:**

- An AZ is a datacentre owned and operated by AWS in which AWS services run. 

- Each region has at least two AZs.

- AZs are represented by a Region Code, followed by a letter identifier, eg: **US-EAST-1a** 

North Virginia has six data centres so it would be **US-EAST-1a/b/c** etc.

- Multi-AZ - Distributing your instances across multiple AZs allows failover configuration for handling requests when one AZ goes down.

- There is < 10ms latency between AZs.  

**Edge Locations:**

Get data fast or upload data fast to AWS.

- An Edge location is a datacentre owned by a trusted partner of AWS which has a direct connection to the AWS network. 

These locations serve requests for **CloudFront** and **Route 53**. Requests going to either of these services will be routed to the nearest edge location automatically. 

![CloudFront Image](https://www.marco.zone/assets/aws-cloudfront.png)

![Route 53 Image](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/core-aws-services/connect-resources-with-aws-networking/images/4a78924d4547d2980a6ca59b3ccc0f8a_b-13-d-93-be-a-08-b-4-d-27-ad-65-d-354-a-564-d-04-a.png)

<img src="https://www.marco.zone/assets/aws-cloudfront.png" width="100" height="100">
