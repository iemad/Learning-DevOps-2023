1) Set up a VM in AWS and clone a project:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/e5442824-d79a-431b-8de8-0221331f064a)
2) Go inside that folder and run this: `mvn package`
3) Go to Jenkins's Plugin section and install a plugin named 'OWASP Dependency-Check'.
4) Go to the Tools section to configure that.
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/e2256341-9a49-4022-ae75-df64e7642cfe)
5) Now configure the pipeline.
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/abbcfe4a-92f0-4e55-b9c8-54719af859e1)
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/11b347ec-4fba-48a2-b71b-49d096b67369)
   Go to Pipeline Syntax and search for this [--scan ./** is going to scan everything]:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/3d270fb5-3f2d-491d-8b98-e1307c67eea7)
   Add this part to the pipeline (it is mentioned in the Notes of this part **7. DevOps Security**
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/a0a5d5a0-fa71-4676-aa16-a09857e6376b)
   Now run the pipeline.

---------------

## Let's try the latest version on the local machine:
1) Fetch it at first:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/5361280e-71f7-487f-ba85-21850c264349)
2) Unzip it:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/9cf1c7ea-3bf9-402d-afcc-bb03d4bb1f47)
3) Do these steps:
   ![image](https://github.com/iemad/Learning-DevOps-2023/assets/17620076/febe8b7e-167f-4447-8b6f-9c60f299e8e1)
4) The HTML page is almost not readable here. So better we do it in the Jenkins.





