Lab 2 Report
Q-1 Describe how this application can be deployed in the cloud using IaaS infrastructure
Ans: 
The app will be set up on virtual computers (like AWS EC2) that include an encrypted VPC of networking, a load balancer storing traffic distribution, and permanent storage storing the database. The OS, runtime circumstances, and services are entirely manually handled.
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
