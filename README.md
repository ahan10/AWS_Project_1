# Deploying a Multi-Tier Website Using AWS EC2

## Description
This project demonstrates the deployment of a multi-tier website using Amazon Web Services (AWS) Elastic Compute Cloud (EC2) instances and Amazon Relational Database Service (RDS). The website consists of a PHP front-end and a MySQL database, with an emphasis on scalability and high availability by leveraging AWS Auto Scaling.

## Problem Statement
A fictional company, ABC, wants to migrate its product to AWS to take advantage of its scalability and availability. The company’s current setup includes:
1. MySQL database
2. PHP-based website

The primary goal is to implement high availability for the website by enabling Auto Scaling on the EC2 instances.

## Objectives
The following objectives were addressed in this project:
1. **Launch EC2 Instances**: Deploy multiple EC2 instances to host the PHP website.
2. **Enable Auto Scaling**: Configure Auto Scaling to maintain at least 2 running instances at all times to ensure high availability.
3. **Create an RDS Instance**: Deploy an RDS instance to host the MySQL database.
4. **Database Setup**: Create the database and a table with password-protected access.
5. **Configure Networking**:
    - Change the website’s hostname to point to the RDS instance.
    - Allow traffic from EC2 instances to the RDS instance.
    - Enable all-traffic rules for EC2 instances.

## Technologies Used
- **Amazon EC2**: For launching and managing virtual servers to host the website.
- **Amazon RDS**: For creating and managing the MySQL database in the cloud.
- **Elastic Load Balancer**: To balance the load on the websites so that auto scaling can be used.
- **Auto Scaling**: To maintain application availability by automatically adjusting the number of EC2 instances.
- **MySQL**: To manage the database layer of the application.

## Steps Performed
1. **Launch EC2 Instances**:
    - Created one EC2 instances to serve the PHP website.
    - Installed relevant packages such as apache2 (the web server) and MySQL.
    - Created custom images out of this instance (used in Auto Scaling).
2. **Networking Configuration**:
    - Created two security groups to server the following purpose:
      - Allow EC2 instances to communicate with the RDS instance.
      - Allow all-traffic rules for EC2 instances.
3. **Create and Configure RDS**:
    - Launch an RDS instance.
    - Create a database with the requirements specified.
4. **Configure Website**:
    - Update the PHP website to use the RDS hostname.
5. **Set Up Auto Scaling**:
    - Enable Auto Scaling to ensure a minimum of 2 instances are running at all times.
6. **Set up Elastic Load Balancer**
    - Configure an ELB to balance traffic across the EC2 instances.


## Screenshots


## Conclusion
This project successfully demonstrates the deployment of a multi-tier web application using AWS services, ensuring high availability and scalability using EC2, Auto Scaling, and RDS.
