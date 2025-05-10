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
