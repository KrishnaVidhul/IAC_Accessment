# Infrastructure as Code (IAC) using Bicep

This repository contains Infrastructure as Code (IAC) written in Bicep, an ARM template DSL, for deploying Azure resources.

## Parameters

The parameters section defines the input parameters required for the deployment:

- `location`: Specifies the Azure region for deploying the resources.
- `rgName`: Specifies the name of the resource group to deploy resources into.
- `vnetName`: Specifies the name of the virtual network.
- `subnetName`: Specifies the name of the subnet within the virtual network.
- `vmName`: Specifies the name of the virtual machine.
- `vmSize`: Specifies the size of the virtual machine.
- `adminUserName`: Specifies the admin username for the virtual machine.
- `adminPassword`: Specifies the admin password for the virtual machine.
- `dbServerName`: Specifies the name of the SQL server.
- `dbName`: Specifies the name of the SQL database.
- `storageAccountName`: Specifies the name of the storage account.

## Resources

The resources section defines the Azure resources to be deployed:

- Virtual Network
- Subnet
- Public IP Address
- Network Interface
- Virtual Machine
- SQL Server
- SQL Database
- Storage Account

## Output

The output section specifies the output of the deployment, which in this case is the public IP address of the virtual machine.

## Usage

To deploy these resources, you can use Azure CLI or Azure PowerShell.

```bash
az deployment group create --name myDeployment --resource-group myResourceGroup --template-file main.bicep --parameters parameters.json
