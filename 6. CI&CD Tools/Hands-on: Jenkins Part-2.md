1) Install these plugins: Eclipse Temurin Installer, SonarQube
2) X (Not needed for this session): if someone likes to install an external plugin:
   -![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/48e46884-c005-4aba-90c7-e244a5e137c9)
   - Go to advanced settings and upload that file.
   - Make sure that the plugin is compatible.
3) Go to Tools and configure:
   - Fix JDK, get jdk11.
   - Fix Maven, get Maven 3.6.0 maybe.
4) The 'System' is the place where we configure different servers.
5) The 'Node and Clouds' is the place where we add Jenkins agents.
6) Create a new user in Jenkins for testing purposes.
7) Adding a Jenkins agent:
   - Create a new VM in AWS.
     - Update the Ubuntu and then install java
     - Make folder 'agent', change the permission to 755
     - Generate SSH key when in the /home/ubuntu location and the key is created in /root/.ssh directory.
     - 

