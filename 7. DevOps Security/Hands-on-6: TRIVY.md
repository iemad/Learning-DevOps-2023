# Scanning File System
1) Set up an AWS VM at first.
2) Follow [this link](https://github.com/iemad/Learning-DevOps-2023/blob/main/7.%20DevOps%20Security/Notes%3A%202\)%20TRIVY.md) and install TRIVY.
3) Clone a git repo: `git clone https://github.com/iemad/Shopping-Cart.git`
4) Now run Trivy on the file system: `trivy fs /home/ubuntu/Shopping-Cart`
   We can do customization too:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a2ed70ba-76fc-48a2-b64d-ba8da0bf52df)
6) Let's generate a report:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/0a087d24-ecdf-4e8c-906e-a2535e029589)
-------------------------------------
# Scanning Docker Images
1) Install Docker on the VM at first.
2) Let's scan this image:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/adc8ebbe-f078-44f1-a4ad-2353206fafae)
   Here is the command we need to run (It will fetch the image from DockerHub and scan it):
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/6375c349-b4fd-4e9f-917a-7f6b31fc843f)
4) We can customize the command:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/6c66ce63-888b-427e-b947-bbf4e3c2479d)
-------------------------------------
# Scanning Docker Images Using Jenkins
1) Install Trivy and Jenkins on the VM (Trivy will be available in Jenkins as the host VM is the same for both).
2) Let's add a stage in the pipeline like this:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/92efeb01-b759-4c31-8348-d4fda1941595)
3) Let's find the report from the latest build:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/690838e2-23dd-47c1-8144-d71c61778370)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/12004273-01f3-4452-b1e7-9f917a5abe75)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/cfe5743c-b0b7-4605-8b4f-7b23b9b239b9)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/072cf4bc-6121-4649-99b4-7f8b523f6e19)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/6cd717d4-b910-4fd3-aa93-672e424c16d4)
5) Let's scan the Docker image now; to do that, the VM must have the Docker installed. Here is what we need to add to the pipeline:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/4dcb4d40-abca-40de-9710-0d074f792c1f)
6) A report will also be generated:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3608dc8b-9e02-4f59-aaad-47bcae615cf8)
   
