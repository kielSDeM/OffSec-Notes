
# Nmap commands

#This command is used to find machines connected to my network.
```
nmap -sV -sP 10.0.0.15/24
```
I use this command to find open ports
```
nmap -sV 10.0.0.21
```
scans all ports on a network
```
nmap -sV -sP 10.0.0.15/24 -p-
```  
scans SYN packages on a network
```
nmap -sS -p- 10.0.0.21
```
command used to find vulnerabilities
```
nmap -sV --script vuln 10.10.75.170
```
