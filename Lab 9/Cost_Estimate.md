# Cost Estimate for 2-Tier Application Deployment

Using the Azure Pricing Calculator, this report offers an estimated cost for establishing a basic two-tier application on **Microsoft Azure**. All prices in the estimate were in **United States Dollar (USD)**, and it had been generated on **March 15, 2025, at 10:56 PM UTC**. **Canada Central** being the region that has been chosen for all resources.

## **Application Configuration**
### **Frontend VM**
- **Service Type:** Virtual Machines
- **Instance Type:** **B2s (2 Cores, 4 GB RAM)**
- **Billing:** **730 Hours (Pay as you go)**
- **Operating System:** Windows (License included)
- **OS Type:** OS Only
- **Managed Disk:** **S6 (64GB)**
- **Networking:** 5 GB outbound data transfer (Inter Region - Canada Central to East Asia)

### **Backend VM**
- **Service Type:** Virtual Machines
- **Instance Type:** **D2s v3 (2 vCPUs, 8 GB RAM)**
- **Billing:** **730 Hours (Pay as you go)**
- **Operating System:** Windows (License included)
- **OS Type:** OS Only
- **Managed Disk:** **S10 (128GB)**
- **Networking:** 5 GB outbound data transfer (Inter Region - Canada Central to East Asia)

### **Networking**
- **Service Type:** Bandwidth
- **Description:** **Internet egress, 200 GB outbound data transfer**
- **Routed via:** **Microsoft Global Network**

### **Database**
- **Service Type:** Azure SQL Database
- **Purchase Model:** **DTU-based**
- **Service Tier:** **Standard (S0)**
- **DTUs:** **10 DTUs**
- **Storage:** **250 GB included per database**
- **Backup Storage Type:** **LRS Backup Storage Redundancy**
- **Long-Term Retention:** **0 GB**

---

## **Cost Breakdown**
| Service Category | Service Type         | Estimated Monthly Cost (USD) |
|-----------------|----------------------|------------------------------|
| Compute        | Frontend VM (B2s)     | **$43.02**                   |
| Compute        | Backend VM (D2s v3)   | **$154.67**                   |
| Networking     | Bandwidth (200 GB)    | **$8.70**                     |
| Databases      | Azure SQL Database    | **$16.18**                    |
| Support       | Basic Support (Included) | **$0.00**                    |
| **Total Estimated Monthly Cost** |  | **$222.57**                   |

## **Additional Details**
- **Licensing Program:** Microsoft Customer Agreement (MCA)
- **Billing Account/Profile:** Not specified
- **Estimated Upfront Cost:** **$0.00**
- **Total Estimated Monthly Cost:** **$222.57**

---

## **Disclaimer**
**Not a quote** All prices are in **USD** and represent a brief estimate. 
See the **[Azure Pricing Calculator](https://azure.microsoft.com/pricing/calculator/)** for the most recent prices. 
The prices shown below are as of **March 15, 2025**.

## **Summary**
Deploying this two-tier application in **Canada Central** is expected to cost a total of **$222.57** per month..

