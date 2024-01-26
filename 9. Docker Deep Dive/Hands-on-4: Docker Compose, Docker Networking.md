- Remove all docker containers:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/f97101ae-099e-40a0-b8ef-465c30464bb3)
- Remove all docker images:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/527e4125-820d-4764-8360-f1f645d36931)

  # Docker Network:

- The most used network type is bridge:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/b87c5096-55bc-4d64-bd7a-83951e9ee04d)
- We can add our network too:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/9617e304-d0a9-432e-8a52-b0001345ae73)
- Inspecting a network:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/67cd0d93-63b2-48ba-af2c-c2f9e2ccef3f)
- Now, we are going to create 2 containers for them and connect them:
  - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/ada3b63d-1500-4848-8e17-5fabdfe6e69b)
  - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/01d73b69-54ef-4ab5-81b9-b1741b46c3d4)
  - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/fd3524e9-d166-45a7-8371-7fb4541d9889)
  - Now access the Mongo Express via browser -> IP:8081
- To avoid writing these commands separately in the terminal, we have Docker compose.

### Docker Compose
- First, stop and remove the containers.
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/8fae9c69-df12-4d04-93e6-e50a9f6a85b0)
- Create a new file named `docker-compose.yml` and add these after validating the indentation/validator from online:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/051d12a7-f414-4328-9eb5-000ef723c91b)
- Run: `docker-compose up -d`
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/94384bb5-ba42-4198-9a74-1844eda9d3ca)
- Both the containers are now running as a multi-container application.
