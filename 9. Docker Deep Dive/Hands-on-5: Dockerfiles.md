# Java-based Application

1) Update the VM and go to the home directory: `cd home/ubuntu`
2) Clone a project: https://github.com/iemad/secretsanta-generator
3) Go inside of that: `cd secretsanta-generator` and `rm -rf Dockerfile`
4) We need java and maven: `sudo apt install maven -y`
5) Let's make a package of the app: `mvn package` and we will find a folder named 'target' is generated and our artifact is there
6) Let's find a JDK 11 based Docker image. Here is a good one:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/f8661086-2b25-4923-9d64-e151c7bbbcef)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/4dd5ad55-2fc3-4c0d-8de6-f9674dddb677)
7) Now let's create an environment. This will be created inside the container:
   - We are going to define a folder trough a variable where our jar file will be kept
   - This folder will be created at runtime
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/aca9fc95-7c2a-41dd-bc87-ae2012ec458a)
8) Now let's define the working directory inside the container:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/b61a2bf9-e33b-4b64-a46e-4633a7257aca)
   We are just using that variable $APP_HOME
9) We can use COPY/ADD here to copy the jar file from the host machine to the Docker container. ADD can extract a zipped folder automatically when the folder is being downloaded from another server. Here we prefer COPY since the jar file is in our host machine.
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/b4534eb7-4814-49ba-a358-4004d956105e)
   Here the left one is the source and the right one is the destination and in the destination, we are renaming the zipped file.
10) 
   
