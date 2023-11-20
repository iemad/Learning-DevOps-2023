## Installation section:
1) Install Maven (Java will be installed automatically): `sudo apt install maven -y`
2) Install Jenkins:
```bash
# Update package list
sudo apt update

# Install Java (required for Jenkins)
sudo apt install openjdk-11-jdk

# Add Jenkins repository key and source list
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'

# Install Jenkins
sudo apt update
sudo apt install jenkins

# Start Jenkins service
sudo systemctl start jenkins

# Enable Jenkins to start on boot
sudo systemctl enable jenkins

# Check Jenkins service status
sudo systemctl status jenkins
```
3) Go to the URL: IP:8080 and provide the administrator password, change to sudo to read the file.


## Installing and Configuring Plugins:
5) Install suggested plugins and proceed ahead.
6) From the GUI, install **Eclipse Temurin installer** and also **SonarQube**.
7) Go to **Tools** section and find 'JDK installations', click on 'Add JDK', give it a name like 'jdk17', click on 'Install automatically' and select 'Install from adoptium.net', select 'jdk-17.0.9+9.1'; Finally, click on 'Apply'.
8) Add another JDK: JDK 11.
9) Now Find 'SonarQube Scanner installations' and add a scanner, and select the latest one.

