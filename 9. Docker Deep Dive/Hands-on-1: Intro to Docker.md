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
9) We can now download any image (good to notice that the image will be downloaded to the default directory dedicated to Docker):
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a3c6d2a2-7892-418e-ab60-aee5b9360858)
10) Now create a Dockerfile in the directory where we are now:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3d89fb90-1ac6-469f-ac74-38b943f7ea93)
    Here in the 4th line, Docker is going to copy all jar files from the **target** folder of the current directory to the Docker's $APP_HOME/app.jar (app.jar is the new name of that application) which is inside a container.
11) Let's build the Docker image using the Dockerfile that we have created:
    Here the. at the end of the command means where the Dockerfile is located. 
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/340601e0-e895-40a0-ab28-4e9b90ea4d19)
12) Let's check the images we have:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/374c5cf3-9c36-41cf-a2eb-7a0f7c8cd797)
13) Now let's run a container from our newly created image:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/0aaaf432-097c-4832-ab4c-bbacbef46bc7)
    The first port is the host port and the second one is the host port.
14) Now we can check the running container, run the command" `docker ps`
15) To see all the containers (where they are being run or stopped): `docker ps -a`
16) No let's check the application in the browser: IP:8080
17) Now let's push our image to the DockerHub:
    - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/017e9f1e-dfcc-4ee7-be03-0437b49b3762)
    - Log in:
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/f8836674-acaf-4aee-b57d-9cf95d845325)
    - Push it:
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/4fb6b7e9-7c03-4ec6-857e-6f493404fd55)


# Step 2: Pulling a Docker image and testing it in another VM
1) Just install Docker first after updating the Ubuntu and then change the permission group: `sudo apt install docker.io -y` and then `sudo usermod -aG docker ubuntu`
2) Log out and log in now with this command: `newgrp docker`
3) Now pull the image:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/ee0d0430-067f-4c25-b729-65e4dfd4222a)
4) Run a container from it:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a8c9a477-290c-4c10-b12b-44d7e4131658)


# Step 3: Some extra things:
1) How to go inside an active container:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/b54f0175-864b-4ec6-96fa-00aa70832d02)
