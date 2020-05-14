#Get the external IP from Powershell

This is a common need 


## If you don't have Internet Explorer available

This happened when trying to diagnose an Azure App Service with the Kodu Powershell

The answer is to use this

```
Invoke-RestMethod https://ipinfo.io/json
```

You can find more information about this brilliant tip at https://blog.netnerds.net/2013/09/powershell-two-liner-get-external-ip-address/
