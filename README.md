# elevate-task-1
Port Scanning in Local network using Nmap 
# Task 1 - Scan Your Local Network for Open Ports

## Date: May 28, 2025
- Intern: Aravind Kumar
- Organization: Elevate Labs - Cybersecurity Intern  

## Tools Used
- Nmap v7.94SVN
- OS: Kali Linux

## Objective
Scan the local network (`192.168.106.0/24`) to discover open ports and identify active hosts to understand potential exposure.

## Local IP Range
- My IP: `192.168.106.160`
- Subnet: `/24` (255.255.255.0)
- Network range scanned: `192.168.106.0/24`

## Scan Summary
- **192.168.106.74**: All 1000 ports filtered
- **192.168.106.105**: Port `53/tcp` open (DNS)
- **192.168.106.160**: All 1000 ports closed

## Key Findings
- One device running DNS service on port 53
- Most other ports were filtered or closed
- Only 3 devices responded on the network

## Potential Security Implications
- Open DNS port may be vulnerable if misconfigured.
- Devices with filtered ports could be using firewalls or IDS.
---

## Files Included
- `scan_results.txt`: Full scan result output
- `README.md`: This file

## Packet Filtering Observations 
- During the Nmap scan of the locla network (192.168.106.0/24), the host at IP address 192.168.106.74 showed all 1000 scanned TCP ports as filtered. This typically indicates that a firewall or packet filtering system in place 
- Nmap did not recieve any response for the probes sent to these ports, which results in them being marked as Filtered 
- This is a common security strategy used to resuce visbility of network services and to prevent port enumeration by attackers
