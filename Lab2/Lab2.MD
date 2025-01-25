Lab 2 Report
Q-1 Describe how this application can be deployed in the cloud using IaaS infrastructure
Ans: The app will be set up on virtual computers (like AWS EC2) that include an encrypted VPC of networking, a load balancer storing traffic distribution, and permanent storage storing the database. The OS, runtime circumstances, and services are entirely manually handled.
Here are the following steps include:
 1.	setting up virtual machines for the database, UI front end, and web server.
 2.	Configuring load balancers to provide high reliability and scaling.
 3.	setting up a safe virtual private cloud, or VPC, for private communication.
 4.	manually maintaining running environments, and updates to software and OS.

Cloud Components:

Compute:-  virtual machine (VM) (like AWS EC2) are used to host react frontend,flask server,and postgres database.
Networking:- A load balancers ( such as Azure load balancers) are used for distributing traffic.
Storage:- This can be used for the long term stroage (like AWS EBS).
Security:- VPC (virtual private network) is perform major role in security which can help to make secure netwrok and it work as a private network in the server ( such as Google cloud VPC, AWS VPC).

Q-2: Describe how this application can be deployed in the cloud using PaaS infrastructure.
Ans:- The backend and frontend are hosted by managed cloud services like Elastic Beanstalk on AWS or Azure App Services, whereas AWS RDS or comparable platforms manage the Postgres database. The deployment process has been simplified with integrated load balancing, development, and lower cost.

Cloud Components:

Web server and Frontend(react)
- It offers combined observing, logging, and scaling and also reduces administrative expenses. Using PaaS services such as Google app engine, and AWS elastic beanstalk.
Database: There are many examples of managed databases such as  RDS, Azure databases for PostgreSQL, or Google Cloud SQL.
Networking: In order to ensure high availability and efficiency, PaaS platforms come with included load balancers that split incoming traffic among several application servers. It can allow for secure communications by supporting HTTPS ending. 
Scaling:- The PaaS platform provides automatic scaling to set up the storage, and compute capacity based on the traffic instances. 

Q-3 For each case, draw a diagram that represents the target architecture and describe each of the chosen cloud components.
Ans:- This is a diagram for IaaS Infrastractures.
![Alt text ](file:///C:/Users/Meet%20Prajapati/Downloads/IMG_7823.jpg)
