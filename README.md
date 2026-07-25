# Investigation-of-a-Session-Hijacking-via-MAC-Spoofing
CyberLab-04


## Overview

This repository documents the analysis of a TCP session hijacking attack against a Telnet session.

The packet capture demonstrates an attacker taking over an active TCP connection by injecting packets after a change in the source MAC address.

## Objectives

- Examine the packet capture using Wireshark.
- Identify the point where the source MAC address changes.
- Identify suspicious network behavior.

  
## Environment

- Wireshark 4.x
- Protocol: Telnet (TCP/23)
- Capture Format: PCAP



## Findings

A detailed packet-by-packet analysis is available in:
findings.md

## Learning Objectives

- Evaluate evidence of TCP session hijacking.
- Identify packet injection
- Detect Layer 2 spoofing


