# Infrastructure with Bastion Host Using AWS CloudFormation

The objective is to build an AWS CloudFormation Stack that deploys a basic infrastructure featuring a bastion host. The bastion host will serve as a secure entry point for accessing private EC2 instances within a VPC.

The diagram illustrating the architecture with the Bastion Host is provided below.

![image](https://github.com/pablo-alex/awsInfrastructureBastion/assets/42077537/3b835fd1-fbab-4298-889f-22e36e36c615)

## Instructions:

### Infrastructure Design:

- Design the infrastructure which will consist of a Public Subnet, a Private Subnet, an EC2 instance that will act as the Bastion host, and an instance located in the Private Subnet.
- The Public Subnet will be used for the Bastion host, while the Private Subnet will house the private EC2 instance that will be accessed through the bastion host.
- Define the appropriate security configuration for the Bastion host, such as the security group that will allow SSH access (port 22) from selected IP addresses, as well as the security group for the private EC2 instance which should be accessible through the Bastion Host on port 22.

### AWS CloudFormation Template Creation:

- Prepare a YAML or JSON file representing the AWS CloudFormation Template to create the infrastructure. Use the appropriate CloudFormation structure and ensure to include all necessary resources for the Subnets, bastion host, test instance, and others as required.
- Define the necessary parameters in the Template to allow customization of the infrastructure, such as the CIDR of the Subnets, subnet names, the AMI to be used for the bastion host, etc.
- You should utilize most of the intrinsic functions explained in the course.
- You should use Mappings for the selection of EC2 instance AMIs.
- You must also use Conditions to demonstrate the use of this CloudFormation feature.

### VPC and Subnet Creation:

- Deploy the AWS CloudFormation Stack in the user's chosen region. Provide 2 options for selection (for example, us-east-1, us-east-2).
Verify that the (public and private) subnets have been created successfully. Note down the network ranges of the created subnets and add screenshots from the AWS console showing the subnets.
Bastion Host Configuration:

### Connect to the bastion host.

- Ensure that the Bastion host has internet connectivity and can access AWS services.

### Access to Private EC2 Instances:

- Deploy an EC2 instance in the previously created private subnet. Make sure this instance does not have direct internet access.
- Use the Bastion host to access the private EC2 instance using SSH.
- Confirm successful access to the private EC2 instance from the bastion host."
