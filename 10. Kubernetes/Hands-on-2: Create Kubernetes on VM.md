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
  - 

