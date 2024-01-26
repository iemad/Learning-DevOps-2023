## Major components of the Kubernetes

- Basic components of K8s:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/0adf151d-ee55-4a92-8bac-72596365c552)
- **Master node **and **worker nodes**:
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/4d4f46c1-13ef-4063-a06e-40d944fe0784)
- **Pod** is an abstraction of a single or multiple containers. After adding certain things to a container/(s) (for instance YAML file, etc.), it turn(s) into Pod(s). The pod is the smallest component of Kubernetes.
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/16a87903-288d-495d-92fa-1872ecf64d4a)
- **Service** is another component of Kuberneter and it has its own IP address. Pods communicate through Services and it works as a load balancer. Good to know that, if a pod is rebooted or stopped and another pod is created, it doesn't matter because the new pod will be attached to the proper service.
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/91e04811-bd79-407c-a8cc-654d34e85a16)
  When App-1 with POD gets overloaded, the service automatically transfers traffic to App-1 POD2. Copy of the pods are called **Replica**.
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/77593029-6671-4c7d-b6bc-8797fbe1fbf1)
- **Config Map** is another component of Kubernetes. It stores databases' URLs that we don't want other people to access.
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/2132813f-6197-489d-9785-1a6fb1ee5a35)
- We store the login credentials of the databases in the **Secret** which is another component of the Kubenetes.
- **Ingress** converts the IP address of the app to a meaningful URL and sends the request to the service.
  ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/d8f9555f-f87f-4295-b359-320efb5e8bec)
- **Volume** is another component of the Kubernetes. The contents of the databases are stored in the volume so that if in case a database pod is restarted, the data is not lost, data persists.

## Processes running on Master node and Worker nodes.

**start from 25:45**
  
