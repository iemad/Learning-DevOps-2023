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
