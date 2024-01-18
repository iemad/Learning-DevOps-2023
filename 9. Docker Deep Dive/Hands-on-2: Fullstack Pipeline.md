# Stage 1: Setup

1) In the Sonar server:
   Install Maven > Jenkins in an AWS EC2 after updating the Ubuntu. Then restart it.
   - access the Jenkins via browser: IP:8080 and proceed ahead.
   - 
2) Launch 2 more EC2s.
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/ec24835f-0fca-47fa-af83-18813afd7116)
3) In the Sonar server:
   - Install Docker after updating Ubuntu.
   - Make the user eligible for the ubuntu group so that the user can run the commands: `sudo usermod -aG docker ubuntu` and then `newgrp docker`
   - Pull a Docker image: `docker pull hello-world`
   - Run a SonarQube container: `docker run -d --name sonar -p 9000:9000 sonarqube:lts-community`
   - Access sonarqube: IP:9000 and proceed ahead.
4) In the Nexus server:
   - update the Ubuntu.
   - install docker.
   - Make the user eligible for the ubuntu group so that the user can run the commands: `sudo usermod -aG docker ubuntu` and then `newgrp docker`
   - Run a Nexus container: `docker run -d -p 8081:8081 --name nexus sonatype/nexus3`
   - Wait a few seconds and then access Nexus: IP:8081 and proceed ahead.
   - For credentials:
       - User: admin
       - Pass:
         - run: `docker ps`
         - Go inside the container:
           - `docker exec -it container_id /bin/bash`
           - `ls`
           - `cd sonatype-work`
           - `cd nexus3`
           - `ls`
           - `cat admin.password`
           ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/1ee0340c-cce4-44e8-b6c0-38e9ab9823ae)


# Stage 2:
1) Jenkins:
   - Install plugins in Jenkins: Eclipse Temurin installer, SonarQube Scanner, Docker, Docker Pipeline, docker-build-step, OWASP Dependency-Check, Maven Integration, Config File Provider, Pipeline Maven Integration Plugin. Then restart.
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/8b1a2bde-bd9f-4044-8f6c-1023ad7d4691)
     Also, install **Nexus Artifact** Uploader.
   - Go to Tools:
     - JDK:
       - Name: jdk17
       - Mark Install automatically
       - Click on Add Installer and choose 'Install from adoptium.net' and then this one:
         ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/f796b983-e863-46fc-aed9-7e57a216ae26)
     - SonarQube Scanner installations:
       - Name: sonar-scanner
       - Keep the rest of things as it is:![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/cafda604-449b-42be-b72d-8d3455c72d6d)
     - Maven:
       - Name: maven3
       - Version: 3.6.3
     - Dependency-Check installations:
       - Name: DC
         ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/fe6d9d89-f8d3-405b-b80b-64d68604916d)
     - Docker:
       - Name: docker
       - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/e0321fc8-2645-4ee3-9730-ec872731a68a)
       - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/6589aa14-a9d0-403f-9ccb-740f1512f49b)
       - Alternative: [image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/d7c6b23c-ec74-4615-b12e-d629b636869d)
     - SonarQube servers:
       - Go to SonarQube in the browser:
         - Click Administration on the menu > Security > Users
         - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/139851b2-a4c2-4f51-ac09-a099bc070a9d)
         - Go to Credentials in the Jenkins:
           - Go to Global
           - Add the token:
             ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/6bd871b3-d447-467d-8a46-4ddf1a9bedeb)
           - Let's Add credentials for Nexus too:
             ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/d3a76cff-04ed-49cf-aaef-804f8e6712a2)
   - Go to System of the Jenkins (We are now going to fix where the .jar file should go:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/e4130838-1724-4894-b0c3-6e6ce81d4190)
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/9d9b07e8-2859-4781-932f-51ef51bbfb7a)
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/9a7141f0-4138-4f08-99a8-c6f0964ab01d)
   - Create the Pipeline:
     - Name: Full-stack-CICD
     - And click Pipeline
     - Then: ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/d6cd2c50-2c40-4463-82af-8faf35ff768e)
     - Replicate stages 444444444444444 times
       ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/2c37842c-82de-4dc9-b370-c20cb088a714)
     - Here is the pipeline: Give the lIIIIIIIIIIIIIIIIIIIIIIIIIIIInk here.
     - ** OWASP is better than Trivy for checking vulnerabilities in dependencies and libraries. Trivy is better than OWASP for scanning Docker images.
     - For Quality Gate stage:
       - Go to SonarQube via browser: Administration > Configuration > Webhooks > Create
         Here the URL is Jenkin's URL.
         ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/c95f6beb-d7e6-47ed-b917-e336f95377fb)
       - Now we can add this stage in the Pipeline syntax.
     - Carefully check in the Portal: 'Deploy artifacts to Nexus' part of the pipeline. But the bottom one is easier here:
       ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/20266c9e-b340-4d55-925a-5e8dde59acf2)
   - Go to Manage Jenkins and go to Managed files.
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/349810ed-9371-4907-b2fb-5e37756dd50b)
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/d947e1d2-d16c-42d3-b83b-1d26c447173e)
2) Fix POM File:
   - Grab these URLs:
     ![297521911-6b5ac7c5-1c22-4be6-a71c-a84cf7de28a7](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/c88456df-2630-42f0-9578-66aa7d107e6a)
   - Replace this part in the POM file
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/186040a3-e078-432b-8e0c-1da6e715bde7)
3) Nexus:
   - Fix this:
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/af43ac2a-3dad-4c2a-9bf2-9521e3202873)
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/99d64e93-03a6-41fa-b513-e309017d69b3)
     ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/19f70f6a-4064-4972-a375-4d4a0f51d5df)


# Unfinished, start from 01:20:20





   
        





























     
