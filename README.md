# Investigation-of-a-Session-Hijacking-via-MAC-Spoofing
CyberLab-04


## Overview

This repository documents the analysis of a TCP session hijacking attack against a Telnet session.

The packet capture demonstrates an attacker taking over an active TCP connection by injecting packets after a change in the source MAC address.


<img width="1129" height="386" alt="image" src="https://github.com/user-attachments/assets/3661dcea-8563-4b39-a9bf-ad1326e41566" />  




## Objectives

- Examine the packet capture using Wireshark.
- Identify the point where the source MAC address changes.
- Identify suspicious network behavior.

  
## Environment

- Wireshark 4.x
- Protocol: Telnet (TCP/23)
- Capture Format: PCAP



## Learning Objectives

- Evaluate evidence of TCP session hijacking.
- Identify packet injection
- Detect Layer 2 spoofing


