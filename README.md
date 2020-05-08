

Hello everyone, after forking this Hashicorp_vault repository in order to run on your own device you need follow next steps


## In backend.tf file

     terraform {
        backend "s3" {
        bucket = "project-emil".                                    # give your own bucket name
        key    = "path/to/my/key"
        region = "us-east-1"                                        # give region that you want
  }
}

## dev.tfvars
In this file you can do changes on each line
## Provide a region for VPC

     region      =   "us-east-1"                                # give region that you want
     region_name  =   "Virginia"
     instance_type = "t2.large"                                 # choose prefered type
     key_name = "vault"                                         # give prefered keyname
     ami = "ami-02eac2c0129f6376b"                              # you can give ami image, here used Centos 7 global AMI
     user = "centos"
     zone_id = "Z00791621PH414P2JJEA9"  #Hosted DNS Zone        # give your own hostname ID
     domain  = "emilbek.com"                                    # replace domain name



## Avaliable Zone 

     az1 = "a"
     az2 = "b"
     az3 = "c"


## This is used for VPC CIDR BLOCK 

     cidr_block = "192.168.0.0/16"


## This is used for public subnets 

     cidr_block1_public = "192.168.1.0/24"
     cidr_block2_public = "192.168.2.0/24"
     cidr_block3_public = "192.168.3.0/24"


## This is used for private subnets 

     cidr_block1_private = "192.168.11.0/24"
     cidr_block2_private = "192.168.12.0/24"
     cidr_block3_private = "192.168.13.0/24"

## Tags

     tags = {
         Name = "Team-6"
         Environment= "Dev"
         Department = "IT"
         Team       = "DevOps"
         Created_by = "Team_6"
     }
