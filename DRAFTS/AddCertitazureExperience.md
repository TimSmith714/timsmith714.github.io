# Adding a Certificate to a Function



## Verify the certificate


## Add to the Function
Go to the Function and click the Platfor Features tab, then SSL
Click the Private Key Certificates (.pfx) tab. Then Import App Service Certificate. 
Select the certificate you just bought in the blade that appears to the right. It will validate and then you can click the OK button.

Now you can add your bindings.
Click the Bindings tab (the left-most) and then Add TLS/SSL Binding.
Choose one of your domains (I had several subdomains for this project), then the certificate thumbprint for the domain and I set the TLS/SSL Type to SNI SSL. Click Add Binding

Repeat for any other subdomains.


## Set Function to request HTTPS
Now you have the certificates there's no point in not demanding them. 

Return to the Platform features tab in the Function Apps blade and click Custom domains.

Click On in the HTTPS Only option.
