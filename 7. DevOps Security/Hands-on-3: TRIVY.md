1) Good to know that the primary use of Trivy is scanning Docker images.
2) Let's do it. Go to (this link)[https://aquasecurity.github.io/trivy/v0.18.3/installation/] and install it in an AWS VM.
3) Clone a repository: `git clone https://github.com/iemad/spring-framework-petclinic.git`
   - A folder named spring-framework-petclinic will be created.
4) We can analyze the file system like this: `trivy fs \home\ubuntu\spring-petclinic` and get a result in the terminal.
5) We can just the Critical and High only like this:  `trivy fs --severity Critical,HIGH \home\ubuntu\spring-petclinic`
6) We can do this too:  `trivy fs --security-checks vuln,config \home\ubuntu\spring-petclinic`
   
