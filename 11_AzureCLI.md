# Azure CLI

In order to run commands against Azure, you'll need to install the Azure CLI.  This will allow you to run commands against Azure from the command line from your local machine.

## Task 1 - Install Azure CLI

Get the Azure CLI

1. Download the Azure CLI

    [Azure CLI Downloads](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli)

1. Run the installer to install the Azure CLI

## Task 2 - Validate Azure CLI is installed

Validate and log in to Azure

1. Validate that the Azure CLI is installed by running the following command:

```bash
az --version
```  

1. Log in to Azure by running the following command:

```bash
az login
```

1. Validate that you are logged in by running the following command:

```bash
az account show -o table
```

## Conclusion

You are now ready to start working with Azure from the command line.  
