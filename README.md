## Configure the environment with the Add-AzureRmEnvironment cmdlt 
Follow the below link to configure the Azure Stack environment with Add-AzureRmEnvironment cmdlet and authenticate a user to the environment
https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure


# Set Deployment Variables
$myNum = "001" #Modify this per deployment
$RGName = "myRG$myNum"
$myLocation = "local"

$templateFile= "azuredeploy.json"
$templateParameterFile= "azuredeploy.parameters.json"
# For Suse $templateParameterFile= "suse.12.sp1.azuredeploy.parameters.json"
# For CentOS 6.7 $templateParameterFile= "centos.6.7.azuredeploy.parameters.json"
# For CentOS 7.2 $templateParameterFile= "centos.7.2.azuredeploy.parameters.json"

# Create Resource Group for Template Deployment
New-AzureRmResourceGroup -Name $RGName -Location $myLocation

# Deploy Template 
New-AzureRmResourceGroupDeployment `
    -ResourceGroupName $RGName `
    -TemplateFile $templateFile `
    -TemplateParameterFile $templateParameterFile
