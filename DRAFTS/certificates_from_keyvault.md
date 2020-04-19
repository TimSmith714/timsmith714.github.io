# Using a certifate from an Azure Key Vault

An Azure Key Vault is a great and secure place to store sensitive information such as passwords but it can also store certificates. The trick is getting hold of them afterwards. I was using .NET Core 2.0, which apparently doesn't support Certificates out of the Key Vault. (And, yes, it's out of support.)

## TL:DR
If you're using a Key Vault certificate with an Azure App Service, you need to add a setting to the configuration as well a reference to the 

Did end up flying blind slightly because the certificate I'd been given couldn't have the private key exported so I could never compare the local and web versions 

## Setting up the Key Vault

### Create an Access Policy for your App Service

- First, get the identification for your App Service. Open your App Service and click on Identity in the Settings section of the menu. 

- Click the Status option to turn it on

- You may need to Save and Refresh this setting

- When the Object ID appears click the icon on the right to copy it into your clipboard.

- Switch to the Key Vault and click Access policies in the Settings section of the menu.

- Click Add Access Policy.

- Choose the permissions for Key, Secret and Certificate. Ideally this should be the minimum to get the App Service working so I selected just GET on all three.

- Click Select principal and paste the ID from your App Service. It should appear in the list below.  Click it once and then click Select at the bottom.

- Click Add to save your changes.

### Get the link for your certificate

- Click Certificates in the Setting section of the Key Vault menu.

- Click on your certificate and then the version you want to use (most likely the Current Version)

- Scroll to the bottom of the page and click the icon on the right of the Secret Identifier to copy it to the clipboard. It might be worth pasting into a text editor until you're ready (or not, depends on your level or paranoia)

### Use the Configuration Settings to replicate the data in secrets.json

 - Go to the App Service (not the App Service Plan) and click Configuration

- Click New application Setting

- Set the Name to the value you've used in your code, for example `ApiSecrets:ServiceCertificate`

There's one more setting that I discovered was necessary to make this work


 - Click New application setting 

 - Set the Name to `WEBSITE_LOAD_USER_PROFILE` and the value to 1

### Using the Connected Services tool in Visual Studio

https://docs.microsoft.com/en-gb/azure/key-vault/vs-key-vault-add-connected-service



## Future stuff to try

https://docs.microsoft.com/en-us/azure/key-vault/tutorial-net-create-vault-azure-web-app
Tutorial: Use Azure Key Vault with an Azure web app in .NET

## Other stuff and links

### https://github.com/dotnet/runtime/issues/30658
This was where it started to become clearer as they suggested adding the WEBSITE_LOAD_USER_PROFILE = 1 setting. It didn't work for the OP but it did for me

### https://www.domstamand.com/loading-x509-cert-from-azure-keyvault-into-netcore-app/
This was helpful for the revelation that the certificate is received from the Key Vault in Base64 so it explained how to read it into the certificate

### https://azidentity.azurewebsites.net/post/2018/07/03/azure-key-vault-certificates-are-secrets
Useful along the way as explained that there's no password required for the certificate when got from the keyvault and also that there are separate links for the certificate and the secret

### https://docs.microsoft.com/en-us/aspnet/core/security/app-secrets?view=aspnetcore-2.0&tabs=windows#access-a-secret
Safe Storage of app secrets in development. Offical and helpful

### https://github.com/Azure/azure-sdk-for-net/blob/d9d93df6c75797a6027c125ab3ff61b2ac894102/sdk/keyvault/Azure.Security.KeyVault.Certificates/README.md
This NuGet package might make things easier. I didn't need it in the end but still