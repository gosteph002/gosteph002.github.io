# 🚩 [Network Traffic] Write-Up

**Category:** [Networking]
**Difficulty:** [ Easy]

## 📝Objective
[The purpose of the room was to know what network traffic analysis is, know what can be observed, know how to observe network traffic,  the sources and flow of network traffic.]  
---
## Summary
[Network Traffic analysis involves capturing, inspecting, and analyzing data as it flows in a network. It aims go give visibility on what is communicated inside and outside the network.
Network traffic analysis is done to: Monitor network performance, check for abnormalities, Detect suspicious activity and to reconstruct attacks during incident response.
What network traffic can be observed: Traffic in TCP/IP layers e.g Application, Transport, Internet and Link layers.
Traffic sources: Intermediary; Devices through which traffic passes(firewalls, switches, routers) Endpoint; Devices where traffic originates and ends( hosts, servers, IoT devices)
Traffic Flows: North-South; Flows from the LAN to WAN includes protocols like (HTTPS, DNS, SSH VPN) East-West; stays within LAN(file shares, application communication)
How can we observe Traffic: Through logs, full packet capture and through network statistics ]

## Challenge
[The exercises involved placing a network tap in the most efficient location and inspecting the network traffic.]
## Scenario 1
 [Malicious PS Download: A user using a random workstation clicked on a phishing link and an HTTP request was initiated to download a malicious Powershell file. The task was to find the appropriate  place to put a tap so that we can capture the web traffic.]
 ## Solution
 [The tap should be put at the web proxy. Since, all devices in the network send their HTTP requests to this device, placing the tap there means capturing all web traffic exiting and entering the network.]
 <img width="2523" height="1312" alt="powershell malicious download" src="https://github.com/user-attachments/assets/4ef9f5cf-f955-49e9-bc7b-2d9757543cd0" />


## Scenario 2
[DNS Infiltration: A workstation was compromised and malicious C2 instructions were infiltrated via DNS TXT records. The task is to find the most efficient place to put the tap to capture the traffic.] 
## Solution
[On top of the DNS server. Since this device handles all external DNS queries and replies on behalf of host which means all DNS passes through it.]
<img width="2533" height="1299" alt="DNS infiltration" src="https://github.com/user-attachments/assets/914461c5-d582-4cc2-abb1-1a3ee54e1592" />


## 🧠 What I Learned
* [The most efficient place to place a network tap to capture intended traffic without affecting performance. ]
