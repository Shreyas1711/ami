# ami


Create a VPC with 3 subnets , routing table , internet gateway and create a public route in the public route table created above with destination CIDR block 0.0.0.0/0 and internet gateway created above as the target

# Steps to install and setup Terraform on Mac
     
# - Run the following commands to install 
        
         1.   brew install terraform

# - Enable tab complettion
         2.   terraform -install-autocomplete
# - Build the infrastructure 
         3. Configure aws CLI 
         4. Create the directory for your terraform files
         5. create a terraform file for eaxample "test_vpc.tf"
         6. create a var_def.tf file , it contains variable definition for all the input variables
         7. create variables.tfvars , assign values to the variables defined in this file
         8. Initialize the terraform directory , run following command
             - terraform init
         9. Format and validate the configuration
             - terraform fmt
         10. terraform validate to chekc any syntax errors
             - terraform validate -var-file="variables.tfvars"
         11. Build infrastructure 
             - terraform apply -var-file="variables.tfvars"
         12. Create another VPC 
             - switch to new terraform workspace
                 - terraform workspace new workspace_name
                 - terraform apply -var-file="variables.tfvars"
         13. Destroy the created infrastructure
                 - terraform destroy -var-file="variables.tfvars"
# - Create an AMI 
	14. Run the ami file using packer build command with vars file
	15. Use ssh -I to connect to the instance
	16. Run SCP -I command to connect to instance and push the web app
	17. Then unzip the web app and run the initial rpm I and run then application and test it using postman
	18. Delete the Instances and Infrastructure
             