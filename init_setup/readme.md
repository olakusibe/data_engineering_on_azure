### Setup Enviroment
Using PowerShell, open your PowerShell profile file, add the line to the file and save it
> notepad $profile
```powershell
$suffix = "<unique-suffix>"
```

Install Azure CLI if you don't have it, you can get it [here](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli) or invoke the following line in PowerShell (as administrator)
```powershell
$ProgressPreference = 'SilentlyContinue'; Invoke-WebRequest -Uri https://aka.ms/installazurecliwindows -OutFile .\AzureCLI.msi; Start-Process msiexec.exe -Wait -ArgumentList '/I AzureCLI.msi /quiet'; rm .\AzureCLI.msi
```

Login to Azure from the shell
```powershell
az login
```

Execute this command in the Azure CLI enviroment 
```powershell
az group create --location "<an-azure-location>" --name "<your-unique-resource-group-name>"
```
