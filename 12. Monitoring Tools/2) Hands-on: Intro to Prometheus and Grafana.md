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
    Here is where it is stated:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/32444039-02f1-4dd5-bebc-49efbdcdef29)
14) Access the Grafana, ID, and Password are 'admin', 'admin'.
15) Now let's connect Grafana and Prometheus:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3ddf4e6d-3ce4-42f8-a805-c6792204f94a)
    Choose 'Prometheus' as the source and proceed ahead.
    Give the URL of the Prometheus server:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/66a7a111-a3b4-475c-8f1d-ee26a5cce344)
    HTTP method should be this:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/364cdb7a-7e9e-472a-b26f-2af1ded18884)
    And then save.
16) Let's make a dashboard now and we can use this file:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/0b1a0824-6984-4ea7-96b1-16fd238084cd)
17) Now it is time for the Alert Notification part:
    First, we need to edit this file:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/de52eff2-4ae8-4744-9450-f61627e9a07b)
    The password should be generated from Gmail in this case:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/17a8a885-4bfc-4188-bd9a-78470f99c128)
    Grafana should be restarted:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/edd5812b-32ec-448e-8f78-d73f14d05018)
18) Set contact point, test, and save:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/71e2c12c-377d-4b92-9f08-d1646009a57f)
19) Let's configure the condition:
    Go here:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/554180a8-46d1-40cf-bc31-59f24ffcf6b6)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/c1e94dd0-6879-401b-8cfb-69de3f7bffae)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/d234abde-7ee2-4c4f-861c-17b7edb02c28)
    Here Google will show an error but GitHub will not:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/8608f6a1-f7e4-4469-82a6-378533420c15)
    Let's proceed:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/d6a6e71e-23c1-4747-995f-bb913dc3d63a)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/892feab9-fea9-4505-a4b9-8338f46557ae)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/e27d9786-ad82-493c-b7fe-e8459c4acedb)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/62cb239f-10a4-407b-96b4-b08ec86b893c)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/b493618a-d57b-4d78-b881-dbd63a4aa4fb)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/06a8fd2a-212c-41af-b661-0ee9401cd9b0)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/dd9b00ba-b95c-4931-b673-ac81e6259db2)
20) Configure Alert for SSL Certificate:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/21fa1e41-9771-4d18-b9a4-a03335581daf)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/7eaf22e1-b427-4489-82b1-eba1e4633c31)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/c43a7a80-e124-4f76-8c51-d76713b498c8)
    Delete these:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/54613dd3-6641-48e0-a01f-fe5d7c3eaa0d)
    Then:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/d7d4a6de-d49a-45da-b255-88d404476138)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/6e65554f-c514-4849-ab49-bcd7c11ed7f4)
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/77aa6879-7c13-468a-83a2-0e46b0f64410)
    Well, click on 'Save rule and exit'. Done for this tutorial. :) 
