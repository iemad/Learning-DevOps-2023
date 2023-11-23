1) Install these plugins: Eclipse Temurin Installer, SonarQube
2) X (Not needed for this session): if someone likes to install an external plugin:
   -![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/48e46884-c005-4aba-90c7-e244a5e137c9)
   - Go to advanced settings and upload that file.
   - Make sure that the plugin is compatible.
3) Go to Tools and configure:
   - Fix JDK, get jdk11.
   - Fix Maven, get Maven 3.6.0 maybe.
4) The 'System' is the place where we configure different servers.
5) The 'Node and Clouds' is the place where we add Jenkins agents.
6) Create a new user in Jenkins for testing purposes.
7) Adding a Jenkins agent:
   - Create a new VM in AWS.
     - Update the Ubuntu and then install java
     - Make folder 'agent', change the permission to 755
     - Generate SSH key when in the /home/ubuntu location and the key is created in /root/.ssh directory.
     - Add public key to authorised key:
       ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/7a859532-ada4-4bfa-9ee6-c5bc70d39d43)
     - Go to Node and Clouds and click 'New Node'
     - Add /home/ubuntu/agent to the Remote root directory, builds will be in this folder.
       ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/cde9affe-d849-4db0-bbba-314d7cc79f43)
       ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/e09510c9-2ff3-4ac9-9db6-175d9b4eae02)
       ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/d164588a-c882-4e91-801c-7f0024ec7bf9)
       ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/712b36b6-c353-40a3-83a7-bf42d3a5f55f)
       ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/df0ddf69-26f1-4fe0-9669-d8549e1252ad)
       ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/d1d995a3-4560-4a78-b3b2-41268b678398)
       and click on Save.
     - Agent is now online, named as 'slave' here:
       ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/18b573ca-e5e1-4c38-985a-a894f3b29ef7)
8) Add a Docker container as a Jenkins agent:
   - This is how Docker needs to be mentioned in the Jenkins file.
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3184d450-c14e-4fc4-a6d4-35bf26110b63)
   - Install plugins: Docker Pipeline and Docker plugin.
   - Go to the configuration of the pipeline
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/c378d242-38dd-447a-a5dc-845d8b23dcc4)
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/14bdf49b-58c0-4f39-9b33-0c8d2a6661d5)
   - Edit the pipeline script:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/886347d5-82a1-4bb4-80d2-c73e2d4a9011)
9) Exploring webhooks:
   - For instance, if someone pushes to a specific branch only then the pipeline will be triggered.
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/5eb5ef1a-b747-4fe7-8818-76bff1fc5684)
   - Install a plugin named 'Generic Webhook Trigger'
   - Create a pipeline
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/9f2a72e7-9cb9-4176-9337-d9a855f24592)
   - In the 'Build Triggers' of the pipeline configuration section, click 'Generic Webhook Trigger'.
   - For 'Post content parameters':
     - Generate a token from GitHub:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/b20796a8-3873-42f1-98d3-9f2e3b215970)
     - Do it like this:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/e208452f-0799-4d5a-9b2d-1df68b7501b9)
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/ca947752-c9b2-4447-9768-7d26bd146b89)
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/8481aeac-0730-4f1a-9f00-57d5009d7284)
   - Prepare a link:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/8087e8cc-ee93-44b8-bf96-57d188b8b626)
   - Copy this link somewhere:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/c3cc0b31-b19b-4174-8fd7-e5e8f7f51f9d)
   - Then the pipeline script:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/956a298e-31ac-494b-97c7-abdba9811e22)
     - Generate it:
       ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/d11b2a9c-3d5d-446c-a0f5-0fe93cb1dd37)
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/39144205-fc0c-4aba-8649-4fd018a062c7)
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/395a991a-1f7b-4027-88a1-d267c3590985)
     Add this tools section too:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/661e9a3c-e871-46f0-bc2f-59f087c24831)
   - Go to the repo:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a5d49886-4fdd-42ce-a51f-4e624b81743d)
     Create a new webhook:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/e685c54c-79cb-4d59-9aa9-5d94b4de8e65)
   - Run the job:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/891d8e3e-6c8c-49f4-ab70-63b354a9702d)
   - Test: Make a small change in that targeted branch and see if there is any job triggered or not.
10) Email Notification in Jenkins:
    - Install the plugin: 'Email Extension Template'.
    - Keep SMTPS open:
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/c8f13a9a-a9a1-4a50-8e90-1bb86e939d5f)
    - Fix settings in Jenkins:
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/af0c9509-28dd-46f1-a40e-c860670997b7)
    - Go to Gmail and fix this, go for 'other option' and give it a name:
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/9b7c3f8e-3309-46c3-b9fa-bc242acb2244)
    - Come back to Jenkins and this:
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/6297b73b-676b-4d13-8143-750a92c5756f)
    - Test the configuration:
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/5e037793-db7d-4c3b-9bec-52ed1eb472d7)
    - Fix some other options:
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3b84a396-efcf-47ab-be7e-8751c58aa27d)

    





    







   

   


     



   
   

     

   


    
     

     


     
