![Capture](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/2d62722a-eed5-4746-89bb-12f975ed62cd)

1) Connect to AWS EC2.
2) Go to a location like `/home/ubuntu`.
3) Update and upgrade the OS: `apt get update`
4) Install JDK: `sudo apt install openjdk-11-jre-headless`.
5) Install Maven: `apt install maven`.
6) Create a maven project following this link: **https://github.com/iemad/Learning-DevOps-2023/blob/main/5.%20Build%20Tool%20(Maven)/Basics%20of%20Maven.md**.
7) Move to the directory `my-project`, we will see `pom.xml` and `src` folder; this pom file contains everything we need for the project.
8) Clone the project: `https://github.com/iemad/Devops-CICD`.
9) Move to `DevOps-CICD` directory.
10) Run the command `mvn compile` and then `ls` and find there is a directory named `target`.
11) Go to `DevOps-CICD` folder and run `mvn test`.
12) Try `mvn clean test` [This will clean the output folder and then rerun the test cases]
13) The try this command: `mvn clean package`. [Package is created and we can see the `target` folder here; this folder contains all the outcomes of the run commands]
14) If we go inside that folder, we will find a .jar file which is the real application where all the dependencies are already there
15) Go back to `DevOps-CICD` directory and run `mvn clean install`
16) Go to the root folder and run `ls -la` and find a `.m2` folder
17) Come back to `Devops-CICD/target` and run that application: `java -jar jar_file_inside_target_folder`
18) Finally, get the IP of EC2 and try like this: `http://54.82.231.43:8080/`
