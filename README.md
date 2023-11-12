# Ansible-vpc
This is an ansible playbook to create a configuration on AWS. Below the list of resource that will be created with the vpc:  
- 3 Privates subnet (PriSub1Cidr, PriSub2Cidr, PriSub3Cidr)  
- 3 Publics subnet (PubSub1Cidr, PubSub2Cidr, PubSub3Cidr)  
- 1 Internet Gateway for public network  
- 1 NAT gateway for private network
- 1 Elastic IP
- 1 Route table for private network  
- 1 Route table for public network  
- 1 Key pair to be use for ssh  
- 1 Ec2 host instance

# Requirements
- AWS credentials to create resources.  
- AWS Configured in console
- Ansible and Boto3 installed

# Installation
Clone this repository to your local machine.  
Navigate to the project directory.  
Run the command **ansible-playbook vpc_setup.yaml** to install the network  
Run the command **ansible-playbook host_setup.yaml** to provisioning a host instance  
Run the command **ssh -i ansible-key.pem ec2-user@Your-Public-IP** to ssh into your instance  

After running both the command a file is generated **output_vars** that contains the IDs of your network resources.

