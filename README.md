# terraform-ecs-fargate
deploying nginx:latest to ecs cluster using terrraform

**What is the Objective ?**
To launch a nginx server through ecs cluster served by load balancer and all the resources managed by terraform. 


**What does the script do ?**
The scipt deploys following 
- Application Load Balancer
- ECS cluster 
- VPC 
- Public and private subnet
- Nat and Internet Gateway 
- Security groups

User --> ALB -> ECS (VPC) nginx server


**How to run the script ?**

1. Clone the terraform-ecs-fargate github repository.

>git clone https://github.com/AjeetK/terraform-ecs-fargate.git
>cd terraform-ecs-fargate


2. Initialize the terraform to get required modules for deploying the resources

>terraform init


3. Checkout what resources will deployed/updated and generate a plan

>terraform plan


4. Once you are okay with the output of “terraform plan” command, you can go ahead creating the stack using “terraform apply” command.
It will ask you to give confirmation to go ahead and create the stack. Type “yes” and hit enter to keep it going.

>terraform apply


This will create the whole setup. At the end it will also out DNS name of a loadbalancer through which we can access nginx homepage.
If you are able to access this endpoint in browser to see the nginx home page that means our deployment is successful.

