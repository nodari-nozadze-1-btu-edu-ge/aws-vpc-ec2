AWS EC2 Deployment Script
This script automates the deployment of an AWS EC2 instance along with associated resources such as VPC, subnets, security groups, and key pair. It utilizes the Boto3 Python library to interact with the AWS API.

Prerequisites
Python 3.x
Boto3 library
AWS CLI configured with appropriate access keys
Setup
Clone the repository or download the script file.
Install the required dependencies using pip install -r requirements.txt.
Set up your AWS credentials by either configuring the AWS CLI or using environment variables.
Modify the .env file to include your AWS access key ID, secret access key, session token, and region name.
Usage
Run the script with the desired command-line arguments to perform different operations. Available arguments include:

-npu: Number of public subnets to create.
-npr: Number of private subnets to create.
--create_vpc_with_subnets: Create a VPC with the specified number of subnets.
--create_vpc: Create a VPC.
--tag_vpc: Provide a name for the VPC.
--vpc_id: Specify the VPC ID.
--subnet_id: Specify the subnet ID.
--key_pair_name: Specify the name of the key pair.
--create_IGW: Create an internet gateway.
--attach_IGW: Attach the internet gateway to the VPC.
Example usages:

bash
Copy code
python deployment_script.py --create_vpc --tag_vpc "MyVPC"
python deployment_script.py --create_vpc_with_subnets -npu 2 -npr 2
python deployment_script.py --vpc_id "VPC-ID" --subnet_id "SUBNET-ID" --key_pair_name "MyKeyPair" --create_ec2_with_VPC

License
This project is licensed under the MIT License.

Feel free to customize this template according to your specific needs.