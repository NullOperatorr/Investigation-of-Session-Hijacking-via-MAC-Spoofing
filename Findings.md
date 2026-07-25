# Findings

## Overview

The objective of this investigation is to examine the captured network traffic, identify abnormal behavior, and determine whether the evidence is consistent with TCP session hijacking.

---

## Environment

| Item | Value |
|------|------|
| Protocol | Telnet |
| Transport Protocol | TCP |
| Analysis Tool | Wireshark |

---

# Analysis

## Phase 1 – Normal Communication

The packet capture begins with a standard Telnet traffic between the client and the Telnet server.

<img width="1901" height="524" alt="image" src="https://github.com/user-attachments/assets/5dc14e1f-fbf8-4173-aad3-22b226cec9cf" />


---

## Phase 2 – MAC Address Transition

During the active Telnet session, the source MAC address associated with the client IP changes unexpectedly while the IP address remains unchanged.

This behavior indicates a Layer 2 identity change that is consistent with MAC spoofing or ARP spoofing.

<img width="1907" height="371" alt="image" src="https://github.com/user-attachments/assets/38e0c147-7eaa-4692-8961-9d9e44cb92f1" />
<img width="1919" height="353" alt="image" src="https://github.com/user-attachments/assets/06298557-6326-496f-8fe4-bc2acf5597ab" />


---

## Phase 4 – TCP Anomalies

Following the MAC address transition, Wireshark identifies TCP analysis events, including:

- ACKed unseen segment

The communication continues using the new MAC address while maintaining the existing TCP session.  

<img width="1876" height="715" alt="image" src="https://github.com/user-attachments/assets/93d20883-b8fe-482f-b20b-6da12d525b5e" />

---

# Findings

The investigation identified the following observations:

- An established Telnet session over TCP.
- An unexpected change in the client's source MAC address.
- TCP analysis anomalies reported by Wireshark.

---

# Conclusion

Based on the observable network evidence, the packet capture is a TCP session hijacking scenario by Layer 2 MAC spoofing.

