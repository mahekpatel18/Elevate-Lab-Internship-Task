# Task 1 - Network Port Scanning (Cyber Security Internship)

 Objective
To scan the local network for open ports using Nmap and understand potential network exposures.  



## Tools Used
- Nmap
- Wireshark (optional)


## Local IP Range
Detected using `ipconfig` on Windows:  
  IPv4 Address: 192.168.120.133  
  Subnet Mask: 255.255.255.0  
  IP Range: 192.168.120.0/24  




##  Nmap Command Used
nmap -sS 192.168.120.0/24 -oN result.txt    

## Nmap scan report for 192.168.120.6  
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http

## Nmap scan report for 192.168.120.133
PORT     STATE SERVICE
443/tcp  open  https

## Port	Service	Description
22	SSH	Secure login; target for brute-force  
80	HTTP	Unencrypted web server  
443	HTTPS	Encrypted web traffic  
21	FTP	Insecure if misconfigured  
23	Telnet	Obsolete and insecure  
3389	RDP	Risky remote desktop protocol  

## Potential Security Risks
Port 22 (SSH) may allow brute-force attacks  
Port 80 (HTTP) is not encrypted — MITM/sniffing possible  
Unknown or unnecessary open ports could expose vulnerable services    

## Wireshark Packet Capture (Optional)  
Filter used in Wireshark:  tcp.flags.syn == 1 && tcp.flags.ack == 0  
it Shows TCP SYN packets when Nmap sends during scanning.  
(Optional screenshot included )  


## Conclusion
This task helped me:
Learn to use Nmap for scanning  
Identify open ports and understand services running  
Analyze network exposure and risks using port scanning  

## Files Included:
result.txt – Nmap scan output  
TASK-1.docx – Full task report  
README.md – This file  

