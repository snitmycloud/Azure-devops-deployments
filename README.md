
This template deploys a simple Linux VM such as ubuntu 14.04, ubuntu 15.10, sles 12 SP1, CentOS 6.7, CentOS 7.2

Note: please use the default values for linuxPublisher, linuxOffer, linuxSku, linuxVersion found in azuredeploy.json or parameters.json while creating the manifest.json in PIR


Deployment steps
Deploy to Azure Stack portal using custom deployment
Deploy through Visual Studio using azuredeploy.json and azuredeploy.parameters.json. Note: for other Linux versions deployment, rename the *.azuredeploy.parameters.json to the default name before deploying via VisualStudio
Deploy the solution from PowerShell with the following PowerShell script
## Configure the environment with the Add-AzureRmEnvironment cmdlt 
Follow the below link to configure the Azure Stack environment with Add-AzureRmEnvironment cmdlet and authenticate a user to the environment
https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure



