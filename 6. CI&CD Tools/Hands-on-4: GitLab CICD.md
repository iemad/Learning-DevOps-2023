1) Import a project:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/73abce5b-0bd7-4f30-94d2-5a1516cdcf5a)
2) Copy and paste the application's GitHub URL (For instance, BoardgameListingWebApp for this case):
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/15020035-39a4-4885-9fd4-bddb19b2a45b)
3) Edit the pipeline, code is given (here:)[https://github.com/iemad/Learning-DevOps-2023/blob/main/6.%20CI%26CD%20Tools/Notes%3A%204)%20Intro%20to%20GitLab%20CICD.md]
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/528cf799-9a48-4280-ba4c-b3d2f45bdabd)
4) Click on 'View Pipeline' and click on 'Compile job'. Given pipeline code will give us an error as Maven is not created.
5) To solve this, add a docker image:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/fd4f949b-520d-434e-835e-761f57a19231)
6) Go to Pipelines from Build (left sidebar). Wait a bit and the job is succeeded.
7) An artifact is generated too but we can not access it:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/f2660fc3-ca3d-4cfc-a30e-e30c17c12f65)
8) Add this piece of code to get the artifact:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/df984172-eafe-45bb-a433-1d1e1ee1a655)
9) **Start from 11:48 in the video.**

    

