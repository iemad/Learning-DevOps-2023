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


