# Lab 6 - Refactoring a Legacy Customer Order Management System for Cloud-Native Deployment on Azure
## Objective
This laboratory The purpose of this lab is to update a **Customer Order Management System** that is currently operating in the form of monolithic online application on a Windows Server 2019 virtual machine. The goal intends to boost cost-effectiveness, scalability, and robustness by refactoring it toward a cloud-native design utilizing Microsoft Azure services.

## Scenario
A business uses a **Customer Order Management System** to manage inventory, process orders, and manage customer orders. Currently, the application functions as a monolith web application on a single Windows Server 2019 virtual machine around Azure. To improve scalability, efficiency, and accessibility, the company is considering transitioning to a cloud-native solution.

## Refactored Architecture
### **Challenges with the Existing Setup:**
-The capacity to expand components separately is limited by the monolithic framework.
-Maintenance issues arise since the application depended on a single Windows Server virtual machine.
-Order management, inventory control, and payment processing have a close connection, which causes performance bottlenecks.
-High operating expenses for maintenance and manually scaling.

### **Proposed Cloud-Native Solution:**
- **Azure App Service** to host the front side of the website.
- **Azure SQL Database** to take the place of the SQL Server on-premise.
- **Azure Functions** for order announcements and handling payments in the background.
- **Azure Blob Storage** for maintaining track of customer documentation, reports, and invoicing.
- **Azure Monitor & Application Insights** for keeping track of and recording.

## **Refactoring Strategy**
### **Step 1: Assessing the Existing Architecture**
-Identify the components that are in fact monolithic, such as order processing, management of inventory, and support for clients.
-Learn how the parts relate and rely on each other.

### **Step 2: Breaking Down the Monolith into Microservices**
Divide the program among separate services:
  **Order Service**: Manages the placing, monitoring, and updating of orders.
  **Inventory Service** (Controls product availability and stock levels).
  **Payment Service** (manages refunds and payments for customers).
Create Azure Functions utilizing background processes.
Keep client logs, reports, and invoices using Azure Blob Storage.

### **Step 3: Implementing the New Architecture**
#### **1. Deploying the Web Frontend to Azure App Service**
-Establish an instance of Azure App Service.
-Use GitHub Actions to deploy the frontend to feed CI/CD automation.
#### **2. Migrating the Database to Azure SQL Database**
-Set up a **Azure SQL Database** for holding product, order, and customer information.
-Transfer data and schema into the current SQL Server.
-Modify the application's settings to make a connection with the new database.
#### **3. Implementing Azure Functions for Background Processing**
-Transfer alerts and order processing to **Azure Functions**.
-Configure event-driven triggered so that payments get processed instantly.
-You can manage order and payment processing events by using **Azure Queue Storage**.
#### **4. Storing Invoices and Reports in Azure Blob Storage**
- Transfer reports, order invoices, including customer bills to **Azure Blob Storage**.
- To display documents straight using Blob Storage, update the application.

### **Step 4: Optimization and Testing**
#### **1. Auto-Scaling Implementation**
Set up Azure App Service to expand automatically in response to traffic.
Use the horizontal scaling method to effectively manage peak loads.

#### **2. Configuring Monitoring and Logging**
To track effectiveness, turn on **Azure Monitor** and **Application Insights**.
Set up warnings to monitor system condition and identify errors.

#### **3. Load and Performance Testing**
To verify the stability of the system, run stress tests with **Azure Load Testing**.
Improve the speed of response by reducing database queries and storage systems.

## **Deployment & Automation** - A **GitHub Repository** houses the system configuration and code for the deployment.
Azure service provisioning can be performed with Terraform/Bicep scripts.
Deployment procedures have been simplified by CI/CD pipelines which utilize GitHub Actions.

## **Architecture Diagrams**
### **Before Refactoring:**
---
![Image](https://github.com/user-attachments/assets/be0a784a-653f-42d0-b9e7-01dc0c85cced)
---
### **After Refactoring:**
---
![Image](https://github.com/user-attachments/assets/00a43e85-2017-4f04-85a7-9eed00e19ae9)
---
## **Difficulties & Takeaways** 
#### **Difficulties:** 
- Ensuring a smooth databases transfer alongside no downtime.
- Overseeing microservices' API connectivity.
- Using **Azure AD** for setting up security and authentication.

### **Takeaways:** 
- **Cloud-native architecture enhances flexibility and performance.** 
- **Cloud-native architecture lowers operational complexity.** 
- **CI/CD automation speeds up installations and lowers personal error.**

## **Deliverables**
-Terraform/Bicep arrangements and the source code.
-Diagrams of the building before and after.
-A thorough record concerning the migrating procedure.
## **Bonus Challenge: Infrastructure as Code (IaC) Implementation** 
- Azure service deployment is done automatically by Terraform/Bicep scripts.
-It decreases human mistaken configurations and improves repeatability.

--- 
### **Conclusion** 
The business benefits from **better scalability, cost efficiency, and operational resilience** from reworking the **Customer Order Management System** to become a cloud-native solution. Better automation, security, and application performance are rendered possible by utilizing Azure services.











  
