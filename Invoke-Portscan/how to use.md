generate file port

#######################################################################################

for i in {1..10000}; do (echo $i) done > openports.txt

#######################################################################################

on target


upload openports.txt and Invoke_Portsscan.ps1


#######################################################################################

powershell -ep bypass


Import-Module .\Invoke-Portscan.ps1


Invoke-Portscan -Hosts internal_target_IP -T 4 -PortFile openports.txt

#######################################################################################
