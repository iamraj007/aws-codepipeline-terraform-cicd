# AWS Codepipeline using terraform with CICD pipeline(AWS)

## Terraform Create ECS with CodePipeline

You can change variables in `variables.tfvars` , 

For example: I want to create a VPC with CIDR ( 10.0.0.0/16 ), two public subnet and two private subnet. Update as per your need

```
vpc_cidr = "10.0.0.0/16"
environment = "dev"
public_subnet_cidrs = ["10.0.0.0/24", "10.0.1.0/24"]
private_subnet_cidrs = ["10.0.50.0/24", "10.0.51.0/24"]
availibility_zones = ["us-west-2a", "us-west-2b"]
region = "us-west-2"
ami_image = "ami-09568291a9d6c804c"
ecs_key = "mycicd"
instance_type = "t2.medium"
repo_owner = "iamraj007"
repo_name = "aws-codepipeline-terraform-cicd"
github_oauth_token = "github_oauth_token"

```

How to run: 

```
terraform init
terraform plan -var-file=variables.tfvars
terraform apply -var-file=variables.tfvars
```
