---
title: "Architecture Deployment"
chapter: false
menuTitle: "Architecture Deployment"
weight: 80
---

The GitHub Fortinet repositories contain infrastructure as code that can be used to deploy sample Fortinet architectures for use during POCs and product demonstrations. They can be found here: [https://github.com/fortinet](https://github.com/fortinet)

Terraform is a common IaC framework used to deploy architectures to cloud environments. Fortinet's [fortigate-terraform-deploy](https://github.com/fortinet/fortigate-terraform-deploy) repository contains IaC templates that can be used in various cloud environments across different providers (AWS, Azure, GCP, etc.) to deploy Fortigates for demonstration purposes. 

To get started with Terraform, it is recommended to run it from a command line interface, such as the MacOS Terminal or the WSL command line in Windows. To get started with WSL in Windows, see [this](http://localhost:1313/getting-started/03docker.html) page from an earlier section in this document. To install Terraform in WSL once you've got WSL set up, you can follow the instructions for installing it in Ubuntu here:[https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli). Under the second 'Install Terraform' heading, click 'Linux', then click 'Ubuntu/Debian' and follow the instructions there at the WSL command line. 

## Deploying a Terraform Template in AWS

Before beginning, ensure you have an AWS user access key with permissions required to launch the desired resources. Information on access keys can be found in the official AWS documentation here: [Managing Access Keys for IAM Users](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)

First, clone the fortigate-terraform-deploy repository locally.

```shell
git clone git@github.com:fortinet/fortigate-terraform-deploy.git
cd fortigate-terraform-deploy
``` 

Then, navigate to the repo you'd like to deploy. For our purposes, we'll navigate to aws/7.4/single, which can be used to deploy a single Fortigate in AWS based on FortiOS 7.4.

Now, create a terraform.tfvars file based on terraform.tfvars.example, open the file with your preferred editor (below we're using vim), and paste in your AWS Access Key ID and Secret Access Key. 

```shell
cd aws/7.4/single
cp terraform.tfvars.example terraform.tfvars
vi terraform.tfvars
```
Then, customize the variables in variables.tf as desired.

Finally, run terraform init, plan, and apply to deploy the infrastructure.

```shell
terraform init
terraform plan
terraform apply
```

If the output is as desired, type 'yes' and press enter, and the deployment will begin.

To tear down the infrastructure, type 'terraform destroy'.

More information on this specific deployment can be found here: [Deployment of a FortiGate-VM (BYOL/PAYG) on AWS](https://github.com/fortinet/fortigate-terraform-deploy/tree/main/aws/7.4/single).
