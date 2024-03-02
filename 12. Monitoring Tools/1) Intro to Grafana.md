![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/7db32b03-7828-43b1-a074-2c142779c3e3)## Setting up 
- Keep these ports open in the VM:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/492c6d91-7811-4361-a100-5ae576209ae5)
- Clone a repo:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/9fc59834-f08f-41b1-b240-f04c139dfde2)
- Go inside of that and execute Docker
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/39eb733d-0aec-4edb-ab7c-42b07e9923ef)
- Let's access Grafana's backend:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/811ce686-1e63-4ec4-a714-a4f4fcd11192)
- Initial ID and Password are: admin, admin
- Let's access the app:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a19b7478-c690-4c9c-aa7e-fb72b54b0e56)
- Now we can add the Data Source:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/812b3320-2329-48ba-8cb7-142f304f484a)
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/0299bf2a-50b0-46a3-8465-6ed44042fd70)
  And now click on 'Save and Test'
- Time to check the metrics:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/023b20d5-a82e-4bee-9545-f38f1a5e0fc0)
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/b8a8f167-70d8-422a-b032-98dc0c79b11b)

  We can set a timer too:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/18a87616-ca54-4e97-bdf6-600a6dd89f9b)

- Let's try the data source Loki:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/1b2c80cc-a662-49dc-967e-8d147d5746bb)
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/f3e6fe6d-2848-4e21-a1f9-e86f7fe00118)

- Let's intentionally make an error:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/2ff0bc7b-802c-4314-ab81-883da3995c6c)
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a099d2a5-94cb-487e-a69d-aa74b309a802)
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/1cbb63c2-e862-4a1e-ad95-9f5c246d9a7c)

- Now we are going to create our own Dashboard:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/4d8fbc2d-0548-430f-81c2-8a99c7a8a2a1)
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/f228276d-c2fe-4d2b-9353-18aa5ee7b779)
  - Let's make some traffic:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/dddaaf11-fc6e-49d8-a0f8-acde81eaa8ea)
  - We can see the changes in the dashboard:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3ab5f68e-fbd9-4d40-85c2-79cf50008217)

- Creating an alert rule:
  - We need two things:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/45364926-14eb-49cf-a00e-725d0b16a7db)
  - Now we are creating a contact point:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/2e72d3a4-ceb7-481c-89d5-06cec7326f59)


    
    







 


