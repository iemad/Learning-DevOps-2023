## Regular way:

1) Go to the Actions tab and get this YML file configured:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a899bd46-d44e-4fb3-b0f6-f69253f1ad05)
2) A build process will automatically be triggered.
3) Uploading artifact:
   - [https://github.com/actions/upload-artifact]
   - Copy this part:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/38d38349-a257-4f03-ae0a-76abca926f3e)
   - Add this to the YML file:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a8036d5c-8da5-4167-b2d7-3d289e45457e)
   - Artifact is ready now:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/670bde6d-3c9b-47ae-9d20-11d34294ce1d)
   

## Doing the job in a Runner (external VM):

1) Create a new branch named 'develop' for the repo and remove the YML file from there:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/7d1dc425-1b36-449a-bdf4-dc0ba82a60fa)
2) Go to the Runners option and create a new self-hoster runner:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/53d7e02d-d27c-4d85-b85e-491e21ec102d)
3) Prepare an EC2 instance in AWS, get into it, and update it.
4) The follow these:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/b8c12957-d6ff-4b99-88fd-c8d6ca930af5)
   - Do this part carefully:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/5b5fe245-730e-49c0-a191-bc1913f8f274)
5) Go to the repo's root, change the branch to 'develop', and go to the Actions tab.
6) In the workflow choose 'Jave with maven' and edit the YML file.
   - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a8329034-fc03-4df2-8db3-ab821e230322)

   

   




