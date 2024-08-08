# RZJenkinTF
Simple Jenkins Pipeline working with TF to make deployments into azure


jenkins running on Ubuntu 20.08. 
install pipelines plugin on jenkins  
install terraform on jenkins server 
install azure credentials plugin 
make an new SPN in azure 
best way to do it is through az cli 
install azure cli on ubuntu - official documentation 
make an SPN (ServicePrincipalName)
az login - (go for browser based login)
notedown subscription id
use this cmd to make a new SPN 
az ad sp create-for-rbac --role="Contributor" --scopes="/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
you should get an output like this
{
  "appId": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
  "displayName": "axxxxxxxxxxxxxxxxxxxxxx",
  "password": "axxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
  "tenant": "xxxxxxxxxxxxxxxxxxxxxxxxxxx"
}
go to credentials inside jenkins 
make a new one 
select type as azureserviceprincipal 
use the detials mentioned above
at this point you should be set to use the files attached in here 
