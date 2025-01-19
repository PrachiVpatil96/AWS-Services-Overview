
# Elastic IP and EC2 Instance Setup

This project demonstrates how to create an Elastic IP in AWS, attach it to an EC2 instance, and ensure that the public IP address remains constant even when the EC2 instance is stopped and started.

## Prerequisites

Before you begin, ensure you have:

1. An AWS account.
2. AWS CLI installed and configured.
3. Necessary permissions to create and manage EC2 instances and Elastic IPs.

## Steps to Implement

### Step 1: Launch an EC2 Instance

1. Log in to the [AWS Management Console](https://aws.amazon.com/console/).
2. Navigate to the **EC2 Dashboard**.
3. Click **Launch Instances** and provide the required details:
   - Select an AMI (e.g., Amazon Linux 2).
   - Choose an instance type (e.g., t2.micro).
   - Configure instance details and ensure you have a key pair for SSH access.
   - Configure Instance Network
4. Click **Launch** to create the instance.

![Preview](Images/img6.PNG)

### Step 2: Allocate an Elastic IP

1. Navigate to the **Elastic IPs** section under the EC2 Dashboard.
2. Click **Allocate Elastic IP address**.
3. Choose **Amazon’s pool of IPv4 addresses** and click **Allocate**.
4. Note down the Elastic IP address allocated.

![Preview](Images/img4.PNG)

### Step 3: Associate the Elastic IP with the EC2 Instance

1. Select the newly created Elastic IP address.
2. Click **Actions** → **Associate Elastic IP address**.
3. Choose the instance you launched earlier from the list.
4. Click **Associate** to attach the Elastic IP to the instance.

![Preview](Images/img5.PNG)


### Step 4: Verify the Elastic IP

1. Go back to the EC2 Dashboard and select your instance.
2. Verify that the **Public IPv4 address** matches the allocated Elastic IP.

![Preview](Images/img3.PNG)

  
Elastic IP addresses in AWS allow you to have a static public IP address for your EC2 instance. This ensures that the IP remains consistent, even if the instance is stopped and restarted. This is especially useful for applications where a constant IP is required, such as hosting web applications or connecting to external systems.


## Notes

- Ensure that your Elastic IP is released when not in use to avoid unnecessary charges.
 #### Step
 ![Preview](Images/img11.PNG)
- before releasing make sure that Elastic ip is diassociated from EC2
- Instance automatically gets a Dynamic Public IP after diassociating the Elastic ip from EC2

 ![Preview](Images/img12.PNG)

- Elastic IPs are region-specific, so ensure you are in the correct region when managing them.


## Conclusion

By following the steps above, you have successfully created and attached an Elastic IP to an EC2 instance. This ensures a stable public IP address for your application.
