# Assignments of week 3

## 1) Observe assigned Subscriptions Observe Azure Entra ID or create own Azure Entra ID in personal Azure account Create test users and groups Assign a RBAC role to user and test Create a custom role and assigned to users and test

1. As i was using normal free tier services , i was not allowed to assign custom rules to users or groups 

2. I was able to create test users as well as test groups 

  * User (beepic) 
  ![alt text](Resources/Screenshot%202025-06-12%20151853.png)

  * Group (beepic-group) 
  ![alt text](Resources/Screenshot%202025-06-12%20151924.png)

### important topics 

* Azure Enrollment : Azure Enrollment is the top-level agreement between a customer and Microsoft to use Azure services.
It's commonly seen in Enterprise Agreements (EA), Microsoft Customer Agreements (MCA), or individual Free Trials.
It defines who pays the bill and under what plan.

* Azure Substiption : A Subscription is a billing container for Azure resources (VMs, storage, databases, etc.).
Each subscription has:

1. A unique ID

2. A set spending limit

3. Access controls (via RBAC)

* Azure Tenant : A Tenant is a dedicated Microsoft Entra ID (formerly Azure AD) instance for your organization.
It stores users, groups, roles, apps, and policies.
Every Azure subscription is linked to one tenant for identity and access control.


## 2) Observe assigned Subscriptions Observe Azure Entra ID or create own Azure Entra ID in personal Azure account Create test users and groups Assign a RBAC role to user and test Create a custom role and assigned to users and test

Created a user (beepic) and assigned a RBAC Which is "Reader"

![alt text](Resources/Screenshot%202025-06-12%20153333.png)

## 3) Create Virtual maching and Vnet from Azure CLI


``` bash
// 0) login first from CLI
az login

// 1) To create resource group
az group create --name usingAzureCLI --location eastus

// 2) to create Virtual Network
az network vnet create --resource-group usingAzureCLI --name formedwithAzureCLI --address-prefix 10.0.0.0
/16 --subnet-name MYsubnet --subnet-prefix 10.0.1.0/24

//  3) to create Virtual Machine
az vm create --name VIRTUALMACHINE --resource-group usingAzureCLI --vnet-name formedwithAzureCLI --subnet MYSubnet --image Ubuntu2204 --admin-username azureuser --generate-ssh-keys
```

## 4) Create and assign a any policy at subscription level

### Creation of Azure Policy

Steps to do it 
1. Search Azure Policy and click on Policy
2. from the left hand side click on definations 
3. Click on + Policy Definition 
4. Provide details and make azure policy 



![alt text](Resources/<Screenshot 2025-06-16 165951.png>);

### Assign Azure Policy on Subscription

Steps to do it 
1. Go to your policy which you recently created 
2. Click on Assign Policy 
3. Fill scope : as your Subscription level
4. On parameters Block : assign the parameters you requeried , as i just wanted few locations to be considered to deploy my resources online , so i selected the locations that i need .

![alt text](Resources/<Screenshot 2025-06-16 170456.png>);
