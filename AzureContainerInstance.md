# Azure Container Instance

#  # To view container 
    az container list -o table

#  # To stop container
az container stop --name hellowork --resource-group LearningLAB

#  # To start container
 az container start --name hellowork --resource-group LearningLAB


#  # To create container
az container create --resource-group LearningLAB --name mycontainer1 --image mcr.microsoft.com/azuredocs/aci-helloworld --ports 80

#  # To create container with public ip and dns name
az container create --resource-group LearningLAB --name mycontainer2 --image mcr.microsoft.com/azuredocs/aci-helloworld --dns-name-label aci-demo --ports 80

#  # To get the dns name and provisionstate

az container show --resource-group LearningLAB --name mycontainer1 --query "{FQDN:ipAddress.fqdn,ProvisioningState:provisioningState}" --out table

#  # To get inside container

az container exec -g LearningLAB --name hellowork --container-name hellowork --exec-command "/bin/bash"

#  # To Delete container
az container delete --resource-group LearningLAB --name mycontainer1
