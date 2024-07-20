

```markdown
# Celebal Summer Internship's Week 7 Assignment: Azure Infrastructure Management Guide

This guide provides step-by-step instructions for managing Azure infrastructure using Azure CLI and PowerShell. It covers essential tasks such as managing subscriptions, creating users, assigning roles, provisioning resources, implementing policies, and securing secrets.

## Table of Contents

1. [Observing Assigned Subscriptions and Resources](#1-observing-assigned-subscriptions-and-resources)
2. [Creating an Azure Account (Azure Entra ID)](#2-creating-an-azure-account-azure-entra-id)
3. [Creating Test Users and Groups](#3-creating-test-users-and-groups)
4. [Assigning RBAC Roles](#4-assigning-rbac-roles)
5. [Creating a Custom Role](#5-creating-a-custom-role)
6. [Creating Virtual Machines and VNets using Azure CLI](#6-creating-virtual-machines-and-vnets-using-azure-cli)
7. [Creating and Assigning Policies at Subscription Level](#7-creating-and-assigning-policies-at-subscription-level)
8. [Creating an Azure Key Vault and Storing Secrets](#8-creating-an-azure-key-vault-and-storing-secrets)
9. [Configuring Access Policies for Key Vault](#9-configuring-access-policies-for-key-vault)
10. [Retrieving Secrets from Key Vault using Azure CLI](#10-retrieving-secrets-from-key-vault-using-azure-cli)
11. [Creating a VM from PowerShell](#11-creating-a-vm-from-powershell)

---

## 1. Observing Assigned Subscriptions and Resources

To observe which Azure subscriptions you have access to and what resources are deployed within those subscriptions, you can use Azure CLI:

```bash
az account list
```

For more details, refer to [What is Azure CLI](https://learn.microsoft.com/en-us/cli/azure/what-is-azure-cli).

---

## 2. Creating an Azure Account (Azure Entra ID)

If you don't have an Azure account yet, you can create one on the Azure portal at [https://portal.azure.com](https://portal.azure.com).

---

## 3. Creating Test Users and Groups

Create user identities and groups within Azure Active Directory (AAD) for testing purposes through the Azure portal.

---

## 4. Assigning RBAC Roles

Assign built-in RBAC roles to your test users using Azure CLI:

```bash
az role assignment create --assignee <user-id-or-principal-id> --role <role-name> --scope <scope>
```

For more information, see [Assign Azure roles using Azure CLI](https://docs.microsoft.com/en-us/cli/azure/role/assignment?view=azure-cli-latest).

---

## 5. Creating a Custom Role

Define and create a custom RBAC role using Azure PowerShell or Azure CLI:

```powershell
New-AzRoleDefinition -InputFile <path-to-role-definition-json>
```

Learn more about [Creating custom roles for Azure resources](https://docs.microsoft.com/en-us/azure/role-based-access-control/custom-roles).

---

## 6. Creating Virtual Machines and VNets using Azure CLI

Provision virtual machines and virtual networks using Azure CLI:

```bash
az vm create
az network vnet create
```

For detailed steps, watch [Creating VMs and VNets from Azure CLI](https://www.youtube.com/watch?v=DOywwse_j8I).

---

## 7. Creating and Assigning Policies at Subscription Level

Implement Azure Policies to enforce organizational standards:

- Create policies in Azure Policy definitions.
- Assign policies at the subscription level and monitor compliance.

Explore [Azure Policy overview](https://docs.microsoft.com/en-us/azure/governance/policy/overview) for more details.

---

## 8. Creating an Azure Key Vault and Storing Secrets

Securely store and manage secrets in Azure Key Vault:

- Create a Key Vault through Azure portal or Azure CLI.
- Store secrets securely within the Key Vault.

Refer to [Azure Key Vault documentation](https://docs.microsoft.com/en-us/azure/key-vault/general/overview) for guidance.

---

## 9. Configuring Access Policies for Key Vault

Control access to Key Vault by configuring access policies:

- Manage access policies in Azure Key Vault settings.
- Define permissions for authorized users and applications.

Learn how to [Manage access to Key Vault](https://docs.microsoft.com/en-us/azure/key-vault/general/secure-your-key-vault).

---

## 10. Retrieving Secrets from Key Vault using Azure CLI

Retrieve stored secrets programmatically using Azure CLI:

```bash
az keyvault secret show --vault-name <key-vault-name> --name <secret-name>
```

For more commands and options, refer to [Azure Key Vault CLI reference](https://docs.microsoft.com/en-us/cli/azure/keyvault/secret?view=azure-cli-latest).

---

## 11. Creating a VM from PowerShell

Automate virtual machine deployment using Azure PowerShell:

```powershell
New-AzVM -ResourceGroupName <resource-group-name> -Name <vm-name> -Image <image-name> -Location <location>
```

Explore [Azure PowerShell documentation](https://docs.microsoft.com/en-us/powershell/azure/new-azureps-module-az?view=azps-9.3.0) for comprehensive scripting.

---

## Additional Tips

- Ensure Azure CLI and Azure PowerShell are installed and up to date.
- Refer to Azure documentation and tutorials for detailed guidance.
- Follow security best practices when managing identities, roles, and secrets.

---

