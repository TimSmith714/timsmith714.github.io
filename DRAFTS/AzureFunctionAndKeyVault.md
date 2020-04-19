# Using a KeyVault with an Azure Function

Looks like much as with a normal App Service you can create a secrets.json in your Visual Studio copy by right clicking the project and clicking Manage User Secrets


## Add Function to Key Vault

### Create an Identity for the Function

Go to the Function and click Platform Features

Click Identity in the Networking section

Turn the Status to On, click Save and then Yes

Copy the Object ID
