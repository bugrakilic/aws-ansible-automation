# Ansible Automation Practices on AWS Cloud Platform

This repository contains a collection of **Ansible playbooks** and best practices for automating various tasks and infrastructure management on the **AWS Cloud Platform**. 

## Prerequisites

Before using the playbooks in this repository, you need to ensure you have the following setup. 

- **Ansible**: Installed on your local machine or CI environment.
- **AWS CLI**: Configured with the necessary credentials and permissions.
- **boto3 and botocore**: Python libraries for AWS. 

## Installation Ansible AWS collection 
Python and required libraries are needed to be installed. 

```
pip install boto3 botocore 
```

Ansible AWS collection helps automate the management of AWS services. 

```
ansible-galaxy collection install amazon.aws
```

## Getting started 
1. Clone the repository. 

```
git clone https://github.com/your-username/ansible-aws-automation.git
cd ansible-aws-automation
```

2. Update the vars/aws_credentials.yml file with your AWS credentials:

```
aws_access_key: YOUR_ACCESS_KEY
aws_secret_key: YOUR_SECRET_KEY
aws_region: YOUR_AWS_REGION
```

3. Run the playbooks. 

An example for running an EC2 playbook:

```
ansible-playbook -i inventory/aws_dynamic_inventory.yml playbooks/create_vpc_ec2.yml
```

An example for running a Lambda playbook:

```
ansible-playbook -i inventory/aws_dynamic_inventory.yml playbooks/deploy_lambda.yml
```

## Contribution 
This is an open-source project for possible Ansible usage on AWS cloud platform. All contributions are welcome, so feel free to submit a pull request. 