# Lab 6 - Refactoring a Legacy Customer Order Management System for Cloud-Native Deployment on Azure
## Objective
This lab aims of this lab is to update a **Customer Order Management System** that is now running on a Windows Server 2019 virtual machine as a monolithic web application. Refactoring it into a cloud-native architecture with Microsoft Azure services is the aim in order to increase cost-effectiveness, scalability, and resilience.

## Scenario
Order processing, inventory control, and customer orders are all handled by a company's **Customer Order Management System**. On a single Windows Server 2019 virtual machine in Azure, the application currently operates as a monolith web application. With the goal to increase scalability, performance, and maintainability, the organization would like to migrate to a cloud-native solution.

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
-Determine which parts are indeed monolithic, such as customer service, inventory control, and processing of orders.
-Find out how the components work together and rely on one another.

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

### **After Refactoring:**

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
- [URL of GitHub Repository](#)
-Terraform/Bicep arrangements and the source code.
-Diagrams of the building before and after.
-A thorough record concerning the migrating procedure.
## **Bonus Challenge: Infrastructure as Code (IaC) Implementation** 
- Azure service deployment is done automatically by Terraform/Bicep scripts.
-It decreases human mistaken configurations and improves repeatability.

--- ### **Conclusion** 
The business benefits from **better scalability, cost efficiency, and operational resilience** from reworking the **Customer Order Management System** to become a cloud-native solution. Better automation, security, and application performance are rendered possible by utilizing Azure services.











  
