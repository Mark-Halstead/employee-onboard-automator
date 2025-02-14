# Azure Logic App - Automated User Onboarding

🚀 **Automated employee onboarding system using Azure Logic Apps, Entra ID, and Slack integration.**

## 🔹 Overview
This Logic App automates the process of **onboarding a new employee** into an organization by:
- **Creating an Entra ID user**
- **Assigning the user to the correct AD group**
- **Provisioning a dedicated Resource Group**
- **Sending a Slack notification to the new hire instead of an email**

## 🛠 Technologies Used
- **Azure Logic Apps**
- **Microsoft Entra ID**
- **Azure Resource Manager (ARM)**
- **Slack API for notifications**
- **GitHub for version control**

## 🔄 Workflow Steps
1. **Triggered by an HTTP request** (with employee details in JSON format)
2. **Creates the employee in Entra ID**
3. **Assigns the employee to the correct Entra ID group**
4. **Creates a dedicated Azure Resource Group** for the new hire
5. **Sends a welcome Slack message** instead of an email

## 📜 JSON Workflow Definition
The full **Logic App definition** is available in [`logicapp-definition.json`](logicapp-definition.json).

## 🚀 Deployment Instructions
### **1️⃣ Deploy via Azure Portal**
- Open **Azure Portal** → Navigate to **Logic Apps** → Create a new Logic App.
- Go to **Code View** → Paste the contents of `logicapp-definition.json`.
- Save & Test!

### **2️⃣ Deploy via Azure CLI**
Run the following command to create the Logic App from JSON:
```sh
az logicapp create --resource-group "your-rg-name" --name "user-onboard-logicapp" --definition logicapp-definition.json
