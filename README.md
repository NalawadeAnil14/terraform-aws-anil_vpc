#AWS VPC Terraform module
#Terraform module which creates VPC resources on AWS.

## Features

- Creates VPC
- Creates public/private subnets
- Creates Internet Gateway
- Create Route table

## Usage 
```hcl
module "anil_vpc" {
  source  = "NalawadeAnil14/anil_vpc/aws"
  cidr_block = "10.0.0.0/16"
  private_subnet_cidr = ["10.0.1.0/24", "10.0.2.0/24", "10.0.3.0/24"]
  public_subnet_cidr  =  ["10.0.101.0/24", "10.0.102.0/24", "10.0.103.0/24"]
  availability_zone    = ["us-east-1a", "us-east-1b", "us-east-1c"]
}
```