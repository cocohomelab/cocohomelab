### Utilities
-ping -nslookup -dig -tracert -traceroute -telnet -netstat -lsof -nc -ps

### DHCP (Dynamic Host Configuration Protocol)
- DHCP server
  - ISP DHCP server
  - Local DHCP Server 
- The 4-Step Handshake - DORA (Discover - Offer - Request - Acknowledge)
- DHCP fails → Windows uses APIPA (169.254.x.x) → No internet
- The DHCP server provide the machine:
  - IP address
  - Subnet mask
  - Default gateway
  - DNS server (usually internal corporate or ISP DNS)

`If you manually set DNS on the PC, it overrides the DHCP-provided DNS.`

`Your PC will then:`
 
  `- Use the public DNS for all name resolution`
 
 `- Ignore the DHCP-provided DNS`

- Command:
- Quick diagnostic / troubleshooting flow
  - Contact ISP provider (ISP DHCP server)
  - Ping to gateway/dhcp server
  - check network connection (auto)
  - ipconfig /all
  - ipconfig /release
  - ipconfig /renew
  - Network Adapter - Properties - IPV4
    - `No default gateway`
    - `“DHCP Enabled: Yes”`

- To Ask/Think:


### DNS (Domain Name System)
- Concept:
  - DNS = the internet’s phone book that turns website names (FQDN) into IP addresses.
  - The DHCP server tells the machine which DNS server to use.
    - Internal DNS refer to Private DNS Server
    - External/Public DNS server refer to google : 8.8.8.8.
    - DNS record 

| Record    | Purpose         |
| --------- | --------------- |
| **A**     | Hostname → IPv4 |
| **AAAA**  | Hostname → IPv6 |
| **CNAME** | Alias           |
| **MX**    | Mail server     |
| **PTR**   | Reverse lookup  |
| **SRV**   | AD services     |

- Command:
  - nslookup
  - dig
- Quick diagnostic / troubleshooting flow
  -  Network Adapter - Properties - IPV4
    -  `No default gateway`
    -  `“DNS Enabled: Yes”`
  - ping to DNS server
  - nslookup
  - dig
  - ipconfig /flushdns : clear (flush) the DNS cache

- To Ask/Think (Things to Keep in Mind)
  -  


### Firewall
- Concept: Port & Packet
  - Type
    - Network Firewall
    - OS Firewall (tcp or udp)
    - Web Applicaton Firewall (tcp or udp)
- Quick diagnostic / troubleshooting flow
  - ping ip address
  - traceroute ip address
  - Check OS Firewall
  - Check Network Firewall

### Active Directory
- What is active directory
- To check:
  - user
  - permisson
### Database
-
- Command:
- Troubleshootign
- To Ask/Think:
> how to test connection?

### Webserver
- Command:
- Quick diagnostic flow
- To Ask/Think:
> how to test connection?

### Mail Server

### Network
- Command:
- Troubleshooting
- Quick diagnostic flow
  - IP address present?
  - NIC present?
  - Can I ping FQDN / Hostname / IPAddress?
  - Does the ip is VIP (Load Balancer) Origin IP
  - Can I ping gateway?
  - Can I ping 8.8.8.8?
  - Does DNS resolve?
  - Is routing clean?
  - Is the port open?
  - Is the port open machine?
  - Firewall or proxy involved?
  - Does it stop at hop?
- Advanced
  - Why does traceroute show * * *?
  - Router is:
    - Blocking ICMP
    - Rate-limiting
    - Or not responding to TTL expiry

🚫 Trap: “The router is down” 

- To Ask/Think:
  - how to test connection?
  - How to test latency?
  - How to test bandwitdh?
  - How to test routing?
  - How to test packet?
  - Virtual IP?
  - Proxy?
  - How to test Port from firewall? type of port?

### VPN
Concept :
- To access the 
- Tunnel
- Requirement for corporate environment
  - Antivirus / EDR
  - HIPS / DLPe 

### Virtual IP
Concept:
- Virtual IP infront of origin server
- check VIP via Virtual IP Manager

===
Operating System
- Windows Admintrator Login (Local)
  - .\Administrator

> Service
  - systemctl
> Process
  - ps -elf
> Port | Firewall
> Configuration files
> Task Scheduler
> DLL
---
Interview trick questions
