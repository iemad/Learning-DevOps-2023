# Setting Up the Nexus:
1) Installing Nexus in Ubuntu:
   Go to /opt directory" `cd /opt`
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/2500b849-4d5a-4a35-937c-2c513917ca4a)
2) Unzip it:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/98493688-7364-437d-8100-b6c4ce3bb90c)
3) Here is the outcome:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/859d1d74-8efe-49ae-9f81-d42d34107340)
   Well, remove that .tar.gz file as we don't need that.
4) Now change the ownership of the remaining files but add a new user before that.
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/901a47ab-693e-40ad-9721-15dade0c6ab5)
5) We need to edit a file:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/5e3c4e2a-8d0b-4365-b11a-29bccb66007c)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/203ed522-e7f1-44d0-b6b9-36bfe292fcaf)
6) Let's start the application but install JDK 8 first.
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/5108a355-b9ca-4b76-9a39-8f6453c0e17f)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/61501998-fb34-4ad9-a9ba-96b4bde9f4e1)
7) Go to the URL: IP.address:8081
8) Find the password here:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/96eb7749-24aa-4421-a489-6a84db1c8b50)

# Building Artifact and Pushing It to Nexus:
1) Edit the POM file in the Repo:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/75a4c1ca-f5fa-4ead-8491-07d640c5f355)
2) Install these plugins in Jenkins:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/bfca062e-c9dc-4bf5-be16-2bda1a5e9419)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/5df477f5-fd72-43d2-b1bf-ba1bfcc37753)
3) Now go to this place:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/979bc26c-8b8a-426a-9355-f117b625c12f)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/4e0d55f4-619d-4282-a86f-b534c049665f)
   And click on 'Next'.
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/86f7847d-113c-49d7-8fca-bb942fc9ce5e)
4) Add a stage in the pipeline:
   Go to pipeline syntax and do like this:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/0a34672f-5a8b-4280-9ef3-604eee1ec9e5)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/01ca0c04-9ca6-468d-9073-180d0d368032)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/5a0ab0dd-31da-4bd7-be8e-e6b480406a0e)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/8c154103-400e-4ad0-8366-696408d1edcf)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/0f898d6d-a8a3-498e-8439-27aa202d91d7)




