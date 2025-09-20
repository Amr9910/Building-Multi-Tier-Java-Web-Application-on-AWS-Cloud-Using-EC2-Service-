# Building-Multi-Tier-Java-Web-Application-on-AWS-Cloud-Using-EC2-Service-
This project introduces participants to deploying a multi-tier Java web application on AWS using EC2  instances. The focus is on creating and managing instances for each tier, configuring security groups, and  ensuring high availability using AWS infrastructure. 

<img width="919" height="715" alt="Screenshot 2025-09-18 233857" src="https://github.com/user-attachments/assets/56b1c0ca-18bf-4cce-b04c-6332eee7157e" />

# Project Summary
Users will access our web application by using a domain name bought from public dns provider. The domain name URL will point to the ELB endpoint.

Users browsers will use this endpoint to connect to the load balancer by using HTTP on port 80. The ELB will be in a security group that only allows HTTP traffic on port 80.

The application load balancer will then route the request to Tomcat servers (EC2) running in a security group that accepts connection only from the load balancer on port 8080.

The backend servers (MySQL, Memcache and RabbitMQ) for our application will sit in a separate security group.

# Project Implementation

Step 1: Create 3 VM 
We’ll create 3 VM. one for the application server (tomcat instance),one for the backend services (mysql instances), one for the backend services(memcache instance, rabbitmq instance) and Application load balancer(nginx). 

<img width="1911" height="870" alt="Screenshot 2025-09-18 224837" src="https://github.com/user-attachments/assets/942fad9a-13c2-4376-87f6-a4570ef944af" />

step 2: chose application and os image 

<img width="1886" height="818" alt="image" src="https://github.com/user-attachments/assets/a254187a-e966-4dce-ae15-6d6be48e98a0" />

# step 3:

choose instance type 

<img width="1253" height="251" alt="image" src="https://github.com/user-attachments/assets/2ec3b8c2-679e-485a-a87c-bd433998d388" />

step 4: create key pair 

<img width="677" height="636" alt="image" src="https://github.com/user-attachments/assets/b14db209-2084-4156-87de-5272ce6f9b6a" />

step 5: create security Group 

<img width="1241" height="617" alt="image" src="https://github.com/user-attachments/assets/28b9ea24-cfb6-403b-8ade-248ff09f04e4" />


