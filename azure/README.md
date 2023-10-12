# Terraform: Azure

Login to using az-cli:

az login
az account set --subscription "MarkMckillionSub"

Create a service principle:

az ad sp create-for-rbac --role="Contributor" --scopes="/subscriptions/9bb8a4ec-2f94-487a-a8e6-1044279566ab"

Export environment varibles for the SPN (PowerShell):

$Env:ARM_CLIENT_ID = "<APPID_VALUE>"
$Env:ARM_CLIENT_SECRET = "<PASSWORD_VALUE>"
$Env:ARM_SUBSCRIPTION_ID = "<SUBSCRIPTION_ID>"
$Env:ARM_TENANT_ID = "<TENANT_VALUE>"

Create resources with terraform (main.tf):
terraform init
terraform fmt
terraform validate
terraform apply

Inspect the resources:
terraform show
terraform state list

Delete the resources:
terraform destroy
