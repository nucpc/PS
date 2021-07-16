# 
Enable Remote Desktop

Execute this command in NUC PC

##### Commands in the elevated Powershell:
```
Enable-PSRemoting -SkipNetworkProfileCheck -Force
Set-Item WSMan:\localhost\Client\TrustedHosts * -Force
Restart-Service WinRM
Get-Item WSMan:\localhost\Client\TrustedHosts
 
Get-NetConnectionProfile | Set-NetConnectionProfile -NetworkCategory Private
Set-NetFirewallProfile -Profile Private -Enabled False
winrm quickconfig -force



Test-WSMan {enter ComputerName or IP Address}
winrs -r:IP Address or Computername -u:Computername\admin -p:password cmd or powershell



````
Make sure when to used powershell command
winrs -r:IP Address or Computername -u:Computername\admin -p:password powershell

To View the currently
Powershell command remotely
Get-ItemProperty -Path HKLM:\Software\Microsoft\Windows\CurrentVersion\OEMInformation | Select-Object Model

Set new Model name
Set-ItemProperty -Path HKLM:\Software\Microsoft\Windows\CurrentVersion\OEMInformation -name "Model" -Value "Logitech Image:M203"

```
Set need to re-image
```
```
Set-ItemProperty -Path HKLM:\Software\Microsoft\Windows\CurrentVersion\OEMInformation -name "Model" -Value "Needs to be RE-IMAGE"
```
