- A request flow:
  - User: I would like to deploy an application to Kubernetes. =>
  - API Server: User's request will come to the API Server. =>
  - Scheduler: Scheduler will inform Kubelet. =>
  - Kubelet: Kubelet will create pods of the application.
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/aa63be68-c428-46c1-b869-8ffaee06d24e)


- Deplyment:
  - We are going to try out this combination:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/edb2d2ba-878f-4823-82c3-30cb5177c387)
  - In the VMs, ports 6443 and 30000-32767 should be kept open along with other necessary ones.
  - Create two Ec2 instances and update them.
  - Now we need to do these step:
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/408a3bec-0f57-4020-96c9-5a679ff50c28)
    Copy this part and run it on the worker node to add that node to the master.
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/2dc28742-7f8d-49d2-908a-c4abdcc80cff)
  - Few sets of commands we need to know:
    - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/408554d0-d7c3-4f51-bc21-3c0ee13ae36b)
    - Way to create a pod:
      - First we create deployment using a Docker image
      - That deployment create a pod
        ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/f7413e7e-8be9-4669-8c69-f48983ea9edc)
      - The way to delete a pod is the delete the deplyment. An attempt to delete a pod will terminate the existing one and along with that a new pod will be created since the deployment is there and working fine.
    - Editing a pod:
      - We can edit a deployment. There we will get a YML file where (in the 'replicas' variable) we can mention the number of the pods of an application we would like to get.
        - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/89804d33-72db-4740-9100-573f3818ba5c)
        - ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3c6d4ed5-098b-4de4-898f-f68dd8917945)
        - Here are two pods from a single deployment.
          ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/334e83ad-c149-4f52-bae8-7f9e5e471a71)
          ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/0455bb0c-7d39-4e59-abf0-6e4036d63dbd)
       
  - Let's understand YAML files.
    - Deployment yaml is responsible for creating Pods.
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/797d1bed-fd6a-4860-b369-55f6de3e3127)
    - Service yaml is responsible for communication between pods.
      ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/9e798849-f3a1-47e4-9616-2cb32e9911a7)

  - Now let's create YAML files in Master node. We are starting from the begining, deleteing the old pods by deleting old deployments.
    ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/54c68b66-1a07-4bfc-9450-39c65aa75eec)



start from 1 hr 23 mins.





