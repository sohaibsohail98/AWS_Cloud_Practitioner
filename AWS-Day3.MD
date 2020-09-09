## Getting Started: Billing preferences, budgets and alarms:

### Accessing Billing preferences:

**Head over to the AWS Management Console, open the link "My Billing Dashboard", once clicked, head to the Billing preferences.**

- Select the following preferences to ensure that the free account will not exceed charges. 

```
Receive PDF Invoice by Email
Receive Free Tier Usage Alerts
Receive Billing Alerts
```

**This will make sure that the account holder is notified of any AWS excess usage service that may be charged.**
 
 
### AWS Budgets:

- The budgets allow the user to be notified if they are going over their budget and it also provides cost forecasts of what could be the upcoming expenses. 

##### **Follow these following steps to start a new budget:**

- From the main console screen of AWS, search for AWS Budgets and look for the option, create a new budget. In AWS, users are allowed to set 2 2 free budgets. 

- Once the cost budget type is selected, enter the relevant details to set your budget including the amount and alert settings. 

### CloudWatch - Setting alarms:

##### **Follow these steps to ensure that a new alarm is set to keep track of AWS billing charges:**

- In the AWS Console, search for CloudWatch. This will load up the page and on the left, click on Billing. 

- It will pop up with a message saying "Please change region".

- In order to follow this message, the user needs to make sure they are in the "US-EAST1" AZ which is located in North Virginia. To change this, in the top right corner allows the user to select a different region. 

- Once this is done, click Billing again and create a alarm. 

- Adding the budget, specifying the conditions and moving on to the next step, configuring actions.

- In the adding notification option, it is important to define the **alarm state** and **the SNS topic** which in this case, the user has to create one. 

## Getting started: Setting up IAM: 

### **Change IAM Users Sign-in link:**

- In order to make sure all the security steps of the AWS account is complete, the user has to ensure that these steps are carried out. 

##### **Tutorial:**

Creating Account Alias:

- This creates a complete new unique account name for IAM users to sign in.

- Below is a screenshot of how the account aliasing appears:

<img src="https://github.com/sohaibsohail98/AWS_Cloud_Practitioner/blob/master/Image/AWSIAMHome.png" height="350" width="470"/> 

### **Activate MFA on Root Account:**

- The reason why is because, if someone stole the email and password access related to the AWS root account, MFA can ensure that there are additional security steps in place to safely secure the root account. 

##### **Tutorial:**

- Click onto:

```
Manage MFA
```

This should bring the site of "Your Security Credentials".

Under the Multi-Factor authentication, there is an option for:

```
Activate MFA
```

This will open a pop up, providing options for the type of MFA device to assign:

- Virtual MFA Device - Using a Mobile phone device to authenticate login. 

- U2F security key - Uses YubiKey or other U2F compliant device

- Other MFA hardware devices.

For the purpose of security our account in this instance, we will be using Virtual MFA Device to multi-authenticate our root account.

In order to this, we downloaded the Google Authenticator app and scanned the QR code. The application provided us with some numbers which need to be entered twice in the MFA codes section of the AWS MFA device setup.
 
**This will successfully enable MFA onto the AWS account**
