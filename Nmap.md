Nmap Scanner
> Defination: ......

> Key functions

> Use case
- Packet Anayzer
- Infra and Network Troubleshooting
- Cybersecurity for monitoring and analyzing

> Knowledge: What You Need to Understand

🔹 Networking Fundamentals
- OSI Model: Focus on Layers 2–4 (Data Link, Network, Transport).
- Common Protocols: Ethernet, ARP, IP, TCP, UDP, ICMP, HTTP, DNS, TLS, DHCP.
- Packet Structure: Understand headers, payloads, ports, and sequence numbers.

🔹 Security Context
- Network Attacks: ARP spoofing, DNS poisoning, port scanning, exfiltration.
- Indicators of Compromise (IoCs): Suspicious IPs, unusual ports, malformed packets.
- Encryption Awareness: Know what you can’t see in HTTPS vs HTTP.


✅ Core Scans (fast + reliable)
- nmap <target> — quick scan of common ports 
- nmap -p- <target> — full TCP port sweep (1–65535) 
- nmap -sS <target> — SYN “stealth” scan 
- nmap -sU <target> — UDP scan (high value, often overlooked) 
- nmap -sn <target> — host discovery only (ping sweep) 
- nmap -Pn <target> — skip ping, treat host as up 

🧠 Enrichment (turn ports into answers)
- nmap -sV <target> — service version detection 
- nmap -A <target> — aggressive scan (OS + versions + scripts + traceroute) 
- nmap -O <target> — OS detection 
- nmap --traceroute <target> — path visibility 

🧰 NSE Scripts (where it gets powerful)
- nmap --script default <target> — default NSE scripts 
- nmap --script vuln <target> — vulnerability scripts 
- nmap --script http-enum <target> — web enumeration 
- nmap --script ssl-enum-ciphers <target> — TLS cipher analysis 
- nmap --script smb-enum-shares -p 445 <target> — SMB share enumeration 

📄 Output = professional workflow
- nmap -oN output.txt <target> — normal output 
- nmap -oX output.xml <target> — XML for automation 
- nmap -oG output.gnmap <target> — greppable output 



- Port
- IP Address
- DNS
- TCP Flags

> Skills: What You Need to Be Able to Do
- Tools Skills: Capture and Filter Packet - Analyzing
- Basic :

#### Start Wireshark with a specific interface
🔹 wireshark -i <interface> -k

#### Capture packets and save to file
🔹 wireshark -i <interface> -k -w capture.pcap

#### Open a specific capture file
🔹 wireshark capture.pcap

### Display Filters
- Display filters let you drill down to specific packet information.

#### Filter by IP address
🔹 ip.addr == 192.168.1.1

#### Filter by port
🔹 tcp.port == 443

#### Filter by protocol (e.g., HTTP, DNS, etc.)
http || dns

#### Filter by packet length
🔹 frame.len > 1000

#### Display only TCP retransmissions
🔹 tcp.analysis.retransmission

#### Show packets with specific TCP flags (e.g., SYN, ACK, FIN)
🔹 tcp.flags.syn == 1
🔹 tcp.flags.ack == 1
🔹 tcp.flags.fin == 1

#### Filter packets with a specific MAC address
🔹 eth.addr == aa:bb:cc:dd:ee:ff


### Capture Filters
### Capture filters are set before starting a capture to reduce the amount of data.

#### Capture only HTTP traffic
🔹 port 80

#### Capture only traffic to/from a specific IP
🔹 host 192.168.1.1

#### Capture traffic between two specific IPs
🔹 host 192.168.1.1 and host 10.0.0.1

#### Capture all ICMP (Ping) traffic
🔹 icmp

#### Capture only TCP traffic
🔹 tcp

#### Capture traffic on a specific subnet
🔹 net 192.168.1.0/24

- Infra and Network Troubleshooting
  - DNS
  - HTTP
  - IP Address (Source and Destination) 
- Cybersecurity for monitoring and analyzing
  - Capture DNS queries and responses; detect failed lookups or spoofed replies.

Use Case Scenario:
- Wireshark showing TCP 3-way handshake
> What I learned:
- I learned about TCP/IP (knowledge).
- I used Wireshark to capture and analyze packets (skill).
- I documented my results and shared screenshots on GitHub (proof).
