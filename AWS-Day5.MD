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

