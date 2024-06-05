- Check this: [https://github.com/jaiswaladi2468/Multistage-Dockerfile]
- 2-stages Dockerfile: [https://github.com/jaiswaladi2468/Multistage-Dockerfile/blob/main/Dockerfile]. Now we can do things easily.
- The main idea is to build things with stage 1 and then run the outcome of stage 1 in the stage 2 container. 



- Make a VM and also a clone of the given repo.
- Go inside of that.
- Run the multistage Dockerfile: ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/4bfa6f49-d885-4b09-b18d-c361e719f148)
- Here we can see how small the multi-stage container is: ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/0a01e5b1-22aa-458f-af2e-46c8b011f6fc)
- Now run the app: ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/5c5ce3f0-bd9a-466b-98db-2fc74eaba831)
- Here is a NodeJS based app:![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/1e02c22b-b87b-4116-ba4a-1a96dd09b429)
  - In 1, we are building the image
  - In 2, we are taking the output of the building stage and running it in a separate container.
  - Everything is almost same but map it like this -> 3000:3000




