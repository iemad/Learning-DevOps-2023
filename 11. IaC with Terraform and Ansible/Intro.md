1) Terraform is better to use when: Provisioning and configuring the resources and also managing them.
2) Ansible is better to use when: Deploying applications and setting up different kinds of tool.


## Terraform
![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/633eb0cd-f7ce-4d77-b084-c63c077b546d)
- Config (file): Says about the resources we want to create.
- TF-State: It says what is the current state of our infrastructure, and what kind of resources are available, created, and exist.
  - It always changes from the current state to the desired state.
  - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3664af40-4d5c-4bfa-ab91-8f4ffaf9f88d)
- Terraform core: It creates all the resources. It talks to the **Provider** which means the what cloud provider we are using. Then it will start creating **Resources**


## Playing with Terraform in EC2:
- Launch an EC2, update it.
- Now install Terraform:
  - Get the commands from hashicorp.com and run them.
  - Check if the Terraform is installed or not: `terraform -v`
- Now we need some files:
  - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/64fbe941-dc82-4498-b699-1dc560e7555c)
- Connect TF to our cloud provider which is AWS in our case.
  - Go to IAM and create a user and add the user to the Group -> Admin and the Attached policies is AdministratorAccess.
  - Create an access key from IAM:
    - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/ed91cf95-b996-4d36-b18b-9ad789492d6c)
    - Choose CLI option.

Start from 22:23 
 


































