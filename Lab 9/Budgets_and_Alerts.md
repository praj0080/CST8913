# Azure Budget and Alerts

## Budget Setup
- **Budget Name:** Monthly Budget - $50
- **Scope:** Azure Subscription
- **Reset Period:** Monthly
- **Budget Limit:** **$50.00 USD**
- **Created On:** YYYY-MM-DD

![Budget Summary](images/budget_summary.png)

## Alert Configuration
### **50% Usage Alert**
- **Threshold:** 50% ($25.00)
- **Notification Type:** Email
- **Recipient:** user@example.com

### **90% Usage Alert**
- **Threshold:** 90% ($45.00)
- **Notification Type:** Email
- **Recipient:** user@example.com

![Alert Thresholds](images/alert_thresholds.png)

## Notes
- Alerts will notify via email when usage reaches 50% and 90%.
- The budget resets **monthly**.

