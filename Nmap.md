![](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fmeterpreter.org%2Fwp-content%2Fuploads%2F2020%2F03%2Fnmap.png&f=1&nofb=1)


# Nmap courses

### What is Nmap?

![](https://blogvaronis2.wpengine.com/wp-content/uploads/2019/12/what-is-nmap-uses-1024x640.png)


### What Does Nmap Do?

![](https://blogvaronis2.wpengine.com/wp-content/uploads/2019/12/how-to-use-nmap-1024x640.png)

### How To Use Nmap

![](https://blogvaronis2.wpengine.com/wp-content/uploads/2019/12/nmap-prerequisites-1024x640.png)

## Nmap Cheat Sheet :
- Nmap Target Selection :

Scan a single IP	`nmap 192.168.1.1`

Scan a host	`nmap www.testhostname.com`

Scan a range of IPs	`nmap 192.168.1.1-20`

Scan a subnet	`nmap 192.168.1.0/24`

Scan targets from a text file	`nmap -iL list-of-ips.txt`

- Nmap Port Selection :

Scan a single Port	`nmap -p 22 192.168.1.1`

Scan a range of ports	`nmap -p 1-100 192.168.1.1`

Scan 100 most common ports (Fast)	`nmap -F 192.168.1.1`

Scan all 65535 ports	`nmap -p- 192.168.1.1`

- Nmap Port Scan types :


Scan using TCP connect	`nmap -sT 192.168.1.1`

Scan using TCP SYN scan (default)	`nmap -sS 192.168.1.1`

Scan UDP ports	`nmap -sU -p 123,161,162 192.168.1.1`

Scan selected ports - ignore discovery	`nmap -Pn -F 192.168.1.1`

- Service and OS Detection :

etect OS and Services	`nmap -A 192.168.1.1`

Standard service detection	`nmap -sV 192.168.1.1`

More aggressive Service Detection	`nmap -sV --version-intensity 5 192.168.1.1`

Lighter banner grabbing detection	`nmap -sV --version-intensity 0 192.168.1.1`

- Nmap Output Formats :

Save default output to file	`nmap -oN outputfile.txt 192.168.1.1`

Save results as XML	`nmap -oX outputfile.xml 192.168.1.1`

Save results in a format for grep	`nmap -oG outputfile.txt 192.168.1.1`

Save in all formats	`nmap -oA outputfile 192.168.1.1`

- Digging deeper with NSE Scripts :

Scan using default safe scripts	`nmap -sV -sC 192.168.1.1`

Get help for a script	`nmap --script-help=ssl-heartbleed`

Scan using a specific NSE script	`nmap -sV -p 443 –script=ssl-heartbleed.nse 192.168.1.1`

Scan with a set of scripts	`nmap -sV --script=smb* 192.168.1.1`


According to my Nmap install there are currently 581 NSE scripts. The scripts are able to perform a wide range of security related testing and discovery functions. If you are serious about your network scanning you really should take the time to get familiar with some of them.

The option --script-help=$scriptname will display help for the individual scripts. To get an easy list of the installed scripts try locate nse | grep script.

You will notice I have used the -sV service detection parameter. Generally most NSE scripts will be more effective and you will get better coverage by including service detection.

- HTTP Service Information : 


Gather page titles from HTTP services	`nmap --script=http-title 192.168.1.0/24`

Get HTTP headers of web services	`nmap --script=http-headers 192.168.1.0/24`

Find web apps from known paths	`nmap --script=http-enum 192.168.1.0/24`

- Detect Heartbleed SSL Vulnerability :

Heartbleed Testing	`nmap -sV -p 443 --script=ssl-heartbleed 192.168.1.0/24`

![](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fpullzone1-stationx.netdna-ssl.com%2Fwp-content%2Fuploads%2F2017%2F07%2FScreen-Shot-2017-07-07-at-14.37.37.png&f=1&nofb=1)

![](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcrazybulletctfwriteups.files.wordpress.com%2F2015%2F09%2F2-nmap-scan-type1.png&f=1&nofb=1)
