# Wireshark Advanced Cheat Sheet

A complete guide to using Wireshark with commands and filters for network troubleshooting and analysis.

A complete guide to using Wireshark with commands and filters for Cybersecurity analysis.

---

## Table of Contents
- [Basic Commands](#basic-commands)
- [Display Filters](#display-filters)
- [Capture Filters](#capture-filters)
- [Advanced Analysis Tips](#advanced-analysis-tips)
- [Real-World Examples](#real-world-examples)
- [Shortcuts and Tips](#shortcuts-and-tips)

---

## Basic Commands
```bash
# Start Wireshark with a specific interface
wireshark -i <interface> -k

# Capture packets and save to file
wireshark -i <interface> -k -w capture.pcap

# Open a specific capture file
wireshark capture.pcap

## Display Filters
## Display filters let you drill down to specific packet information.

# Filter by IP address
ip.addr == 192.168.1.1

# Filter by port
tcp.port == 443

# Filter by protocol (e.g., HTTP, DNS, etc.)
http || dns

# Filter by packet length
frame.len > 1000

# Display only TCP retransmissions
tcp.analysis.retransmission

# Show packets with specific TCP flags (e.g., SYN, ACK, FIN)
tcp.flags.syn == 1
tcp.flags.ack == 1
tcp.flags.fin == 1

# Filter packets with a specific MAC address
eth.addr == aa:bb:cc:dd:ee:ff


## Capture Filters
## Capture filters are set before starting a capture to reduce the amount of data.

# Capture only HTTP traffic
port 80

# Capture only traffic to/from a specific IP
host 192.168.1.1

# Capture traffic between two specific IPs
host 192.168.1.1 and host 10.0.0.1

# Capture all ICMP (Ping) traffic
icmp

# Capture only TCP traffic
tcp

# Capture traffic on a specific subnet
net 192.168.1.0/24

```

Reference :


https://www.malware-traffic-analysis.net/

https://labex.io/free-labs/wireshark
