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
8) Go to Jenkin's Credentials section and 
