# Building-Multi-Tier-Java-Web-Application-on-AWS-Cloud-Using-EC2-Service-
This project introduces participants to deploying a multi-tier Java web application on AWS using EC2  instances. The focus is on creating and managing instances for each tier, configuring security groups, and  ensuring high availability using AWS infrastructure. 

<img width="919" height="715" alt="Screenshot 2025-09-18 233857" src="https://github.com/user-attachments/assets/56b1c0ca-18bf-4cce-b04c-6332eee7157e" />

# Project Summary
Users will access our web application by using a domain name bought from public dns provider. The domain name URL will point to the ELB endpoint.

Users browsers will use this endpoint to connect to the load balancer by using HTTP on port 80. The ELB will be in a security group that only allows HTTP traffic on port 80.

The application load balancer will then route the request to Tomcat servers (EC2) running in a security group that accepts connection only from the load balancer on port 8080.

The backend servers (MySQL, Memcache and RabbitMQ) for our application will sit in a separate security group.

# Project Implementation


