# WebAppEcrDemo
Web Application  demo with ECR and ECS services used

This is normal web applicatiomn using HTMl and CSS which looks like this
![image](https://github.com/user-attachments/assets/2cd1ed53-69a9-4cd4-8f07-594d5b0504d9)


We need to creat ECR i.e AWS Elastic Container Respository 
Login to AWS and search ECR and click on create respository
![image](https://github.com/user-attachments/assets/c82e400b-0a97-4fc4-bfe8-2d75b5003a96)


After that we need to push the image to the ECR, you can click on push command that AWS provide you
![image](https://github.com/user-attachments/assets/27721469-f2dc-450b-bb40-cb3ba77ae917)


Now we need to create the ECS to use this image and host to a container
![image](https://github.com/user-attachments/assets/24661057-a8f3-48b0-9f97-4b9b21fd8b3e)


NOw click on the create ECS and enter the detail like Cluster name where to host i.e fargate or EC2 
![image](https://github.com/user-attachments/assets/b71b06bd-d9ee-4d0e-9180-f7526409a429)


Once you click on create go to task definition tab and creat task which we need to do for docker container like given secruity group access , networking ,scaling etc
![image](https://github.com/user-attachments/assets/f983c788-d104-4fbb-a3f9-1d0261e35a30)


After this we need to create service in Cluster so go to cluster and create new services
![image](https://github.com/user-attachments/assets/203760a7-7964-49e6-b6fa-150089bdcd93)


So we are using Github Action which trigger ECR and ECS service in AWS if any changes done in the code
We need to set up the environment  variable so that Github able to push the image in the ECR, so to add the credential we need to go to repository and there we need to add secret and variable tab in the setting section.
![image](https://github.com/user-attachments/assets/834a13d3-eed8-4160-91ef-95bce384db8c)


Now click on the secret and variable and after that click on Action and add the secret 
![image](https://github.com/user-attachments/assets/5776263b-edcd-4c88-baec-1c103b183ade)


I had upload the git hub action folder in the githubaction folder where i had used this variable to login to ecr to build and push the image.


Result: HTML page is able to see using AWS ECR and ECS service 
![image](https://github.com/user-attachments/assets/d6365390-baca-4562-8e29-98206cf66032)

