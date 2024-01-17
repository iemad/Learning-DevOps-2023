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
   - Install plugins in Jenkins: Eclipse Temurin installer, SonarQube Scanner, Docker, Docker Pipeline, docker-build-step, OWASP Dependency-Check, Maven Integration, Config File Provider. Then restart.
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




























     
