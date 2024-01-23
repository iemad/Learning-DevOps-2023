1) Create an EC2 in aws.
2) 3 kinds of Docker volumes:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/1e131bad-a3b0-44bf-a1b9-f894a35592ed)
3) Fetch the image adijaiswal/boardgame:1.0, make a container out of that, map that to 80808->8080, give the container a name, make a docker-compose YML file.
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/c7cccfb9-1224-4f58-9f57-8fd8c4ef11ff)
4) Paste this:
```yaml
version: "3.5"
services:
  mongodb:
    image: mongo
    container_name: mongodb
    volumes:
      - db_data:/data/db
    ports:
      - 27017:27017
    environment:
      - MONGO_INITDB_ROOT_USERNAME=rootuser
      - MONGO_INITDB_ROOT_PASSWORD=rootpass
    networks:
      - network
  mongo-express:
    image: mongo-express
    container_name: mongo-express
    ports:
      - 8081:8081
    environment:
      - ME_CONFIG_MONGODB_ADMINUSERNAME=rootuser
      - ME_CONFIG_MONGODB_ADMINPASSWORD=rootpass
      - ME_CONFIG_MONGODB_SERVER=mongodb
    restart: unless-stopped
    depends_on:
      - mongodb
    networks:
      - network
networks:
  network:
    name: mongo-network
volumes:
  db_data:
```
5) 1 is the created volume and 2 is the part of the application that is mapped.
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3d50ac1b-ffa9-40b6-8043-32c765db5973)
6) Run this: `docker-compose up -d`
7) Docker is creating this:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/c28cac6b-50c5-4029-9c6a-debe9da50e26)
8) Two new containers are created as expected:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/618cd82e-c1b8-49a6-98ce-77ffed7884e3)
9) Go to the Ec2 IP:8081, we now find Mongo Express and add 2 more dummy databases.
10) Now remove both the containers:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/c2d7fc59-b241-46a8-8454-95b263bc77bd)
    And of course, we can not check the Mongo Express now.
12) And then make them again:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/be037e35-c6ae-42b9-b741-2f1e4f8cd2ee)
    This time we find the newly added databases too if we go to the Mongo Express via browser.






























