 if you are using multiple var files for ex: terraform.tfvarrs and prod.tfvars.so you have keep two state files,otherwise it will go override the already exsited infrastructure.
    
    to solve this problem we will use workspaces.
    
    terraform workspace---------it will show all the aruguments.
    terraform workspace list---it will show all workspaces
    terraform workspace new prod---------to create a new workspace
    terraform workspace new dev
    terraform workspace select <name of the workspace>---------------to go to particular workspace.
    terraform workspace delete <name of the workspace>
    
    if you want identcal environment
    
   what is an workspace?
   
   if we are planning to deploy the multipleenvironments from the same code state file would get over written.inorder to differtiate the satatefile we will use workspaces.
   it is a good choice if you want create identical environments.
   
   go to that particular workspace.then do thsi
   
   terraform workspace select <name of the workspace
   
   terraform apply --var-file <name of the varfile>-------dev.tfvars,test.tfvars
   
   adding userdata to ec2 machine while creating:
   ----------------------------------------------------
   
   https://www.bogotobogo.com/DevOps/Terraform/Terraform-terraform-userdata.php
   
   
   importing:
   ---------------
   
   you deployed an infrastrcture using terraform.but later you created any ec2 or any resource manuvally.the terraform doesnot about that .so if you try to destroy infastrucure 
   it wont delete the infrastructure because the resource is there inside that infrastructure that you have created manually.
   
  
   
   so you have to import that resource to terraform
   
   terraform state list
   
   terraform import
   
   terraform import <aws_instances.web-2> <instancesid>---manuval created id 
   
   
   terraform lifecycle:
   ----------------------------
   https://www.terraform.io/docs/language/meta-arguments/lifecycle.html
   
    1.create_before_destroy
    2.prevent_destroy 
    3.ignore_changes 
    
    
  terraform apply on specific resource:
  -------------------------------------
  
  https://learn.hashicorp.com/tutorials/terraform/resource-targeting
    
    
   
   
   
    
    
