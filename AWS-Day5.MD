## Hands On: Sessions Manager:

### Connecting to the Instance:

- Right clicking the instance and clicking connect, will bring up a pop message. This will show several ways of how to connect to the server, this includes using SSH or EC2 Instance connect services. 

- Instead of using this way to connect, AWS has recommended to use SSM to connect to instances. 

- Search for SSM (Simple Systems Manager) in the services, this will open up the AWS service. 

Under **Instances & Nodes**, click on:
```
Session Manager
```

Once this is loaded, we will start a session.

- Previously we created a IAM role for SSM, it will log anytime someone uses a session. 

- Once the session has started, it might login as the root user, to change this, enter the following in the console:

```
sudo su - ec2-user
```

### Creating an Amazon Machine Image (AMI)

**Another way of referring to AMI, is a snapshot or a copy of an server.**

- Right clicking the server in instances, or selecting actions, along with image and create image will create this AMI. Note that it's not necessary for the instance to be running for this to occur. 

Below is a screenshot of how it appears in the EC2 instances menu:

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSAMICreation.png" height="200" width="550"/>

- Once this is clicked, a pop up option will show additional settings including the image name, allocated RAM and volume options.

 - An AMI is needed when setting up Auto Scaling Groups. 

### Auto Scaling Groups:

- Under EC2, on the left, the auto-scaling groups option will appear. 

- An auto-scaling group ensures that multiple instances or servers are running. For example, to make sure atleast one instance is functioning, the group can set a rule to check if one server is running. If it's not running, it will launch a instance. 

- It can also to help meet the demand of the traffic. For example, a web application or app may start receiving a lot of traffic, and it needs more servers to keep up. Auto-scaling groups will determine this demand and use more instances to ensure it can handle the web traffic. 

- In the same way, if the traffic is reduced, the auto-scaling groups would reduce the amount of instances to meet the demand.  

**Creating an Auto-Scaling group**:

- Click on the create button and getting started. 

- Once this is selected, it will ask for the launch configuration which in this case, we will have to create a new one. This will open a new tab to create it. 

- In this launch configuration, we chose the instance type which is the AMI we previously created, along with the basic instance resources (Medium server settings). We also selected the IAM role. 

- Storage and security groups options are also needed to be selected in the launch configuration. In this case, I had to select the port as 22 and source to anywhere, to accept all incoming connections. 

- Once this launch configuration is setup, we can select it when creating the auto-scaling instance. 

- While selecting the launch configuration, we will have to implement some settings, this includes VPC and Subnets. 

- Furthermore, Auto-Scaling policies are important because its a set of rules to make adjustments according to specific instance usage. For example, high CPU load or major data transfer may need more computing power, hence the policies will ensure it keeps up with this demand. 

- Note: Load Balancer can distribute incoming traffic across multiple instances using Elastic Load Balancer. It can also monitor the health of its registered instances, and direct traffic only to healthy instances. 

- Configuring the group size, and scaling policies is an important factor when we are creating an auto-scaling group. We can set minimum or maximum capacity limits for our group size. As seen below with the screenshot, autoscaling policies can save resources, time and money:

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSAutoScalingPolicy.png" height="200" width="550"/>

- This is highly recommended because it allows the business to use as the traffic demands for new instances. 

- There is an option to add notifications to the group to allow tracking of whenever Amazon EC2 Auto Scaling launches or terminates the EC2 instances in the Auto-Scaling group. 

- Once these options are selected, we can review the creation of the auto-scaling group and create it.

Below is a screenshot of a successful Auto-Scaling group created:

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSAutoScalingCreation.png" height="200" width="550"/>


### Elastic Load Balancer:

- This tool allows traffic to be managed with instances, if one AZ is unavailable then it can look for an instance in another AZ. 

- To start up, we will launch some instances. After this, we will create a new load balancer.

- The type of load balancer we selected was ALB - Application Load Balancer - generally the one to use. 

- After selecting two availability zones, selecting internet-facing scheme, default security group, the option for configuring routing appears.

- Creating a new target group - reference to the instances which we want to route traffic to. 

- After this, we need to register the instances we just started to the load balancer and create it. 

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSLoadBalancerCreator.png" height="200" width="550"/>

### S3 Buckets:

- A place to contain files. Once we navigate to the S3, we uploaded a file just to test out the uploading function.

### CloudFront:

- CloudFront is used as a CDN (Content Distribution Network). Used to share video or static files across the world, loading them as quickly as possible, shortest route to the end user. It will take the content and copy and make it available in multiple edge locations around the world. To access the content, it will go to the nearby edge location instead of connecting to a distant location. 

- Once we create a distribution, it will locate the files in the S3 bucket and copy the content over to multiple global servers to make it quickly accessible. 

- A unique DNS name similarly like in the Elastic Load Balancer, the traffic would access the domain name, which would route the traffic to the nearest edge location. 

### Relational Database Service (RDS):

- In RDS, we will be creating a database using PostgreSQL, the template we are choosing is the Free tier. Production is used by big companies looking for the best option, Dev/Test is for small to medium sized businesses. Free tier is the best to get gaining hands on experience. 

