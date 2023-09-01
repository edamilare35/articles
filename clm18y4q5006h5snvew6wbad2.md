---
title: "The Power of Automation: Deploying an ARM template in Microsoft Azure."
datePublished: Fri Sep 01 2023 21:33:53 GMT+0000 (Coordinated Universal Time)
cuid: clm18y4q5006h5snvew6wbad2
slug: the-power-of-automation-deploying-an-arm-template-in-microsoft-azure
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693612150845/62d6140c-2a3f-4123-850f-cf66e0c1018b.jpeg

---

In Microsoft Azure deploying ARM templates allows you to automate and replicate your infrastructure deployments, saving time and increasing efficiency. You can version control your templates, re-use them across different environments, and easily make changes when needed.

To deploy an ARM Template there are various methods of deploying
1. Using the Azure portal.
2. Azure PowerShell.
3. Azure CLI.
4. Azure DevOps.

It is best to choose a preferred method when deploying an ARM template. For faster and easier deployments we would concentrate on three of the methods listed above: Azure CLI, PowerShell and DveOps.

**Deploying an Azure Resource Management template locally Using Azure CLI**

To use Azure Resource you need to create an Azure account. You would need to install Azure CLI as well to your local machine.

To deploy an ARM template locally, you can follow these steps:

1. Install and Set Up Azure CLI: First, you need to have Azure CLI installed on your local machine. You can download and install it from the Azure CLI installation page. Once installed, open a command prompt or terminal window.

2. Sign in to Azure: Run the command `az login` in the command prompt or terminal to sign in to your Azure account. It will open a browser window or prompt you to enter your Azure credentials in the command line.

3. Set the Subscription: If you have multiple subscriptions, you can set the active subscription by running the `az account set --subscription <subscription_id>` command. Replace `<subscription_id>` with the ID of the subscription you want to use.

4. Create a Resource Group: Use the `az group create` command to create a resource group in which you want to deploy your resources. For example, `az group create --name MyResourceGroup --location "West US"`.

5. Deploy the ARM Template: Run the `az deployment group create` command to deploy the ARM template. Specify the resource group, deployment name, and the path to the template file. For example, `az deployment group create --resource-group MyResourceGroup --name MyDeployment --template-file ./myTemplate.json`.

6. Monitor Deployment Progress: You can monitor the deployment progress by running the `az deployment group show` command. Specify the resource group and the deployment name. For example, `az deployment group show --resource-group MyResourceGroup --name MyDeployment`.

That's it! You have now deployed an ARM template locally using Azure CLI. Remember to validate your template file before deploying and make sure you have the necessary permissions and access to the Azure resources you are deploying.


**Deploying an ARM template using Powershell**

To deploy an ARM (Azure Resource Manager) template locally using PowerShell, you can follow these steps:

1. Install the Azure PowerShell module if you haven't already. You can do this by running the following command in PowerShell:
```
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

2. Import the Azure PowerShell module:
```
Import-Module Az
```

3. Connect to your Azure account using the following command and follow the authentication steps prompted in the PowerShell console:
```
Connect-AzAccount
```

4. Set the Azure subscription where you want to deploy the ARM template:
```
Set-AzContext -SubscriptionId <subscriptionId>
```

5. Navigate to the folder that contains your ARM template files using `cd` to make the deployment context your current location.

6. Deploy the ARM template using the following command:
```
New-AzResourceGroupDeployment -ResourceGroupName <resourceGroupName> -TemplateFile <pathToTemplateFile>
```
Replace `<resourceGroupName>` with the desired name of the resource group, and `<pathToTemplateFile>` with the path to the ARM template file.

This command will deploy the resources defined in the ARM template to your Azure subscription.

Please note that you need to have the necessary permissions and Azure subscription access to perform this deployment.

**Deploying an ARM template using Azure Pipelines or GitHub Actions**

Deploying a template using DevOps would require a GitHub account, Visual Studio with Azure Pipeline extension, Azure Subscription, Azure DevOps Org with access to parallel jobs. Parallel job allows you run a single job at a time in your organization. 
Note: These only apply to Azure DevOps Services.

To deploy an ARM (Azure Resource Manager) template using Azure Pipelines or GitHub Actions, you can follow these general steps:

1. Set up your source control repository: Create a repository on GitHub and push your ARM template files to it.

2. Set up your deployment pipeline:

 **Azure Pipelines:**
a) Create an Azure Pipelines YAML file (azure-pipelines.yml) in your repository. 
b) Define a pipeline that defines the steps required to deploy your ARM template. 
c) Include tasks for checking out the repository, logging in to Azure, and running the `az deployment` command to deploy the ARM template. You can also include validation steps or environment-specific configurations as needed.
   
**GitHub Actions:** 
a) Create a GitHub Actions workflow file (e.g., .github/workflows/deploy-arm-template.yml) in your repository.
b) Configure the workflow to trigger on specific events (e.g., push, pull request), define the steps required to deploy your ARM template, and use appropriate actions (e.g., actions/checkout, azure/login, azure/arm-deploy) to carry out the deployment.

3. Configure deployment parameters: Define the necessary parameters for your ARM template deployment. These parameters may include resource group name, location, virtual machine sizes, etc.

4. Securely store deployment secrets: Azure Pipelines and GitHub Actions provide ways to store and retrieve secrets securely. Make sure you store any sensitive information like Azure credentials or deployment keys securely by using either environment variables or a secret storage mechanism provided by the respective platforms.

5. Trigger the deployment: With your pipeline or workflow defined, you can now trigger the deployment by pushing changes to the repository or manually triggering the pipeline or workflow execution.

Remember to test and validate your deployment process before using it in a production environment. You can leverage additional features provided by both Azure Pipelines and GitHub Actions to customize and enhance your deployment process as needed.



