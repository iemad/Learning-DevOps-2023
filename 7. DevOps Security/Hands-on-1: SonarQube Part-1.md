1) Install Jenkins in a VM.
2) Then install Docker, get the proper image for that, and run it in the backend:![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a3581023-6be6-4b0d-86fc-96fbbb4673e0)
3) Install two plugins in the Jenkins: Eclipse Temurin installer, and SonarQube Scanner.
4) Get the SonarQube here: IP:9000/. User ID and Password are: 'admin'. 
5) Create a pipeline in Jenkins, here is a [pipeline](https://github.com/iemad/Learning-DevOps-2023/blob/main/7.%20DevOps%20Security/Notes%3A%201\)%20SonarQube.md)
6) Now configure the SonarQube Scanner plugin from the Tools section in Jenkins:
   First, JDK:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/f75a07cf-3db8-4438-8c57-45d52c302e4b)
   Then, SonarQube:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/72cce662-4e01-483a-b4f4-234f774b341c)
   Then, Maven:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/5a82a07e-3d9a-4a6e-9fd1-e51114d5c5bd)
7) Get credentials (generate token) from SonarQube:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/ff3cf558-4f9a-4939-8b40-a8ca222bce67)
8) Go to Jenkin's Credentials section and add it as a secret text.
9) Go to Jenkin's System section and set up the SonarQube part:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/4a3c17ff-f8d2-4d1f-bc7a-9811e0dbd025)
10) Now it is time to complete the pipeline.
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/81222ca0-b279-43c3-b03d-8268fe7ddd38)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/eb4e7f52-d69b-4459-b3c0-b23f0bc286c1)
    - Now fix the SonarQube part:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/fc5d74ae-5685-47ef-94f5-42bc29dbf9d8)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/ee336be2-5361-4d93-acab-f9bb106d02d1)
    - Calling SonarQube Scanner tool:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3c003e61-bcbe-49a8-b283-1162a8b0d3fc)
    - Add arguments: It tells the project name in SonarQube, where the Java binary files are, and what the project key will be.
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/b137bb85-59f1-4b76-b902-1d6938231b6d)
    - Make sure that pom.xml file has this part (properties):
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/4c9dd74c-863a-4c6a-a197-bd9b8faaf074)
    - Add this plugin section too:
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/4c94bc1e-6b7e-4f43-88ef-8af8130d5a9d)
    - And also the dependency section:
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/7c521249-5c79-4238-98c1-130b20ed6499)
    - In case we would like to run it in another branch:
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/9bbb0d9a-a154-4836-8563-6dde88bafcbe)
    - Now if we run the pipeline, we can see a result in the SonarQube portal.
11) Installing external SonarQube Plugins by going inside the Docker container and then restart it:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/03578f16-609f-4434-a286-3eb11d823fd2) 




    
    

    


    




