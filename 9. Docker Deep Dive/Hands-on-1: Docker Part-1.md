# Step 1: Containerizing a Java App with Docker

1) Install Ubuntu in an AWS VM.
2) Install Maven in it after updating it.
3) Now let's grab an app:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/279576ee-3f06-446f-a589-c3ba5d0376f3)
4) To clone it, paste the link in the terminal and go inside the directory.
5) Now type `docker` in the terminal and it will show how to install docker. Install Docker.
6) Extra info:
   These are the main components:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/0b110713-bf3e-4749-b94e-19051a138643)
   Docker Socket manages the communication between Docker Deamon and the Client. Deamon is the engine and the Client is a command line interface.
7) We need to change the permission:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a2f5c257-cc2c-4a95-aae6-bc89bfe8b41e)
8) Log out and log in now with this command: `newgrp docker`
9) We can now download any image (good to notice that the image will be downloaded to the default directory dedicated for Docker):
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a3c6d2a2-7892-418e-ab60-aee5b9360858)
10) Now create a Dockerfile in the directory where we are now:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3d89fb90-1ac6-469f-ac74-38b943f7ea93)
    Here in the 4th line, Docker is going to copy all jar files from the **target** folder of the current directory to the Docker's $APP_HOME/app.jar (app.jar is the new name of that application) which is inside a container.
11) Let's build the Docker image using the Dockerfile that we have created:
    Here the . at the end of the command means where the Dockerfile is located. 
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/340601e0-e895-40a0-ab28-4e9b90ea4d19)
12) Let's check the images we have:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/374c5cf3-9c36-41cf-a2eb-7a0f7c8cd797)
13) 

   
