1) Set up a VM and install Docker in it:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/199d6378-d04d-4513-bee1-72e57e92c1fb)
2) Then install Docker Compose:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/120f76e4-dcab-4513-9a86-8b6772288a00)
3) Go there: _https://github.com/iemad/Monitoring_, clone it the VM
4) Execute this in the background:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/725175ce-6b97-470b-bdbd-52fe71980a89)
5) Check the status of Blackbox Exporter if it is set up or not, run this command: `netstat -tunlp`
6) Install net-tools: `apt install net-tools`
7) Things should be good now:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/ccea1901-3c60-4c52-993f-a122bd7b5955)
8) We can not proceed further, this file needs to get permission modified:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/918a1c19-2a6d-4646-9946-d9bd0cda1f49)
9) Now we can do this again:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/71ad48f6-2158-4049-a08c-ef66214a9a8a)
   Now it is running on 9115.
10) Let's change the IP of this file:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/fd661d76-16df-4787-8e3e-addbf05ef8f8)
    This is the IP of the VM:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/74890f05-a14d-4625-a161-5f93f82cc736)
11) Now install Prometheus and Grafana:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/ba7bc942-aa26-40bf-842b-b6e6e8c4c265)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/f5d9494d-733b-476c-a9a8-66febd6ea125)
12) Let's access the applications: IP:9115 and IP:9090 and IP:3000
13) Now Blackbox and Prometheus are connected: 
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a3ba4497-ad09-4ca6-9dd3-3cc7d4231655)
14) Access the Grafana, ID, and Password are 'admin', 'admin'.
15) 



   
