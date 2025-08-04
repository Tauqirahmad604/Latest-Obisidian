1. Variables
2. Variable types ( string, number, bool, List)
3. Functions (join, upper, lower, lookup)
4. Map Variable
5. TFVARs Files
6. Read Variables from your system(export TF_VAR_username=tauqir)
7. Terraform Core and Plugin
8. .tfstate file and lock .tfstate file
9. destroy command
10. Terraform validate
11. Terraform refresh (when you change some thing manually by console and want to update that in terraform file also)
12. Terraform Output
13. Terraform console ( to see variables values)
14. Terraform fmt (correct format of data in files )
15. Dynamic Block (bar bar repeat hony waly blocks ko manage krny k liye)
16. Terraform Taint (When we want to recreate a new specific resource may be security group or any thing)
17. File Provisioner (file, local-exec, remote-exec)--------> to send file from local to remote
18. Terraform workspace (when need to setup multiple env)
19. Terraform datasource (AMI id can be changed in aws that's why we use it )
20.  Terraform Modules and its types (root module, child module, published module)
21. Terraform Backends 
22. Sentinal In Terraform
23. Our pipeline wants to deploy to private ec2 using aws roles how to achieve this?
24. Life cycle in terraform or nested block
25. You need to update an EC2 instance's AMI ID without downtime. Terrafrom wants to destroy and recreate the instance. How do you avoid downtime?
26. I want to store secrets in aws secret manager through terraform how can I achieve this?
27. If I am going to create s3 bucket for remote state is it necessary to create it in public?(no make it private and allow only aws users to access it)
28. I have created an infra with terraform and now don't want to continue with terraform any more. How to achieve this?



### Terraform Workspaces

We can use one terraform file for both enviroments. We can use this variable to achieve this ${terraform.workspace}-instancename


![[Pasted image 20250514202115.png]]



![[Pasted image 20250514203316.png]]


Question: How it manage tfstate file may be anything overrides.

If we have 2 workspaces name with dev and test each workspace have different tfstate file
.terraform/
└── terraform.tfstate.d/
    ├── dev/
    │   └── terraform.tfstate
    └── test/
        └── terraform.tfstate


### Terraform Data Sources




### Sentinel In Terraform 

**Sentinel** in the context of Terraform is a **policy as code** framework developed by **HashiCorp**. It's used to enforce **fine-grained, logic-based policy decisions** on Terraform operations in the **Terraform Cloud** and **Terraform Enterprise** environments.


#### Terraform drift detection 

( if some one manually changed any settings for any resource, then detecting that change is called drift detection). 
There are 2 ways to detect it.
Scenario 1: 
Use terraform refresh using a cron job. ( terraform refresh, refershes the recents changes which was done manually to the statefile and keeps it updated. 
Scenario 2: - A) 
Use audit/activity logs to see who made changes, if its changed by user and resources is managed by TF, then send an alert using lambda/azure functions and notify.


[http://139.144.55.181:9090/](http://139.144.55.181:9090/ "http://139.144.55.181:9090/")

letskinect

pRozu5uy@CH?ke$=7bOY

abdul@139.144.55.181

54.243.23.246------> intelrad server ip

cd /home/totalscope/server_sh_files
