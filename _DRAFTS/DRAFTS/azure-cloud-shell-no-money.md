# Getting the billing period with Azure CloudShell

There's a friendly rivarly in the office about 

az billing period list


Though have to set up a cloud shell first. Not too hard


Go to shell.azure.com
select a directory
choose Bash or PowerShell
An Azure file share is required - there will be a cost for this "small" according to dialogue". 
Select your subscription
I strongly recommend clicking Show advanced Settings to choose Resource Group, Storage account and File share. Give them a meaningful name
Click Create Storage

https://docs.microsoft.com/en-us/cli/azure/billing/period?view=azure-cli-latest

In the interface
From scratch, click Home and then Cost Management. Not the one at the bottom in the Tools section. If it doesn't appear. Click the More Services link at the top and search for "Cost Management + Billing"

Your account should then be shown along with the next bill date.

Sometimes I was presented with a screen asking for a Scope. Click the account you're checking in the main part of the screen to see the information


Cost Management _ Billing -> Overview


