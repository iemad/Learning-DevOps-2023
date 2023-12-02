## A) Built-in Process:
1) Import a project:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/73abce5b-0bd7-4f30-94d2-5a1516cdcf5a)
2) Copy and paste the application's GitHub URL (For instance, BoardgameListingWebApp for this case):
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/15020035-39a4-4885-9fd4-bddb19b2a45b)
3) Edit the pipeline, code is given (here:)[https://github.com/iemad/Learning-DevOps-2023/blob/main/6.%20CI%26CD%20Tools/Notes%3A%204)%20Intro%20to%20GitLab%20CICD.md]
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/528cf799-9a48-4280-ba4c-b3d2f45bdabd)
4) Click 'View Pipeline' and 'Compile job'. Given pipeline code will give us an error as Maven is not created.
5) To solve this, add a docker image:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/fd4f949b-520d-434e-835e-761f57a19231)
6) Go to Pipelines from Build (left sidebar). Wait a bit and the job is succeeded.
7) An artifact is generated too but we can not access it:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/f2660fc3-ca3d-4cfc-a30e-e30c17c12f65)
8) Add this piece of code to get the artifact. Now click 'commit changes' and a new pipeline job will be started:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/df984172-eafe-45bb-a433-1d1e1ee1a655)
9) Go to the most recent pipeline that we run and go to the build section:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/31da1606-cdae-4d27-8b6b-6b47b9ee20eb)
10) Now we see the option for downloading the artifacts:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/571b03c7-0d6e-4675-8f32-47461b1e463d)


## B) Taking the Process to Our Own VM Agent:
1) Make a VM in AWS. Update it, install Maven.
2) Go to GitLab and add a project runner from the left sidebar's CI/CD option.
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/6699b827-c400-40c5-b577-cd72bce232dd)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a83229e3-681a-447c-8fd7-f8d89750ad38)
3) Go to the VM and copy the Step 1 code.
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/5754118c-72cd-4ec6-b32f-c164b9db930b)
4) Create a new folder, move to that, and run the command after installing gitlab-runner:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/4d21d046-50b9-41fb-9531-72f9f75b3765)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/bfcdff04-298d-47da-8a99-875e7216fe89)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/7f16c657-f007-4b61-8aaa-74d058595162)
5) The runner is attached to the GitLab, refresh the page:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/ff39e90c-980c-47e9-988e-17f2728efdb2)
6) 





