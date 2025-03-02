# terraform
Deploying Kubernetes using terraform!!!

===============

Prerequisites:-

For MacOs: 
  1. Install Azure CLI

#brew update
#brew install azure-cli
#az --version

  2. Install kubectl

#brew install kubectl
#kubectl version --client



===============

1. login to azure portal.

#az login


2. Set  the subscription ID

#az account set --subscription <your_subscription_id>

  3. Create service principle  account for authentication while deploying AKS using terraform :

#az ad sp create-for-rbac --name "terraform-sp" --role Contributor --scopes /subscriptions/<<Subscription-Id>>

  4. Verify Authentication:-

#az login --service-principal -u $ARM_CLIENT_ID -p $ARM_CLIENT_SECRET --tenant $ARM_TENANT_ID



Verify Subscription ID

az account show --query id --output tsv


5. Initialise terraform
	#terraform init

  6. Validate the terraform 
	#terraform plan

  7. Run the terraform
	#terrafrom apply 


Check All name spaces of Kubernetes and pods




8.)Delete the Kubernetes

#terraform destroy -auto-approve

