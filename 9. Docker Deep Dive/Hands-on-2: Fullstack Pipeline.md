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
            
           
         
