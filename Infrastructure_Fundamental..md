### DNS
- Concept:
  - DNS = the internet’s phone book that turns website names (FQDN) into IP addresses.
    - Internal DNS refer to Private DNS Server
    - External/Public DNS server refer to google : 8.8.8.8.
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

- To Ask/Think:
> Internal DNS
> External/Public DNS

### DHCP
- Provide an ipadress
- DORA (Discover - Offer - Request - Acknowledge)
- DHCP fails → Windows uses APIPA (169.254.x.x) → No internet
- Command:
- Troubleshooting
  - Ping to gateway/dhcp server
  - check network connection (auto)
  - ipconfig /all
  - ipconfig /release
  - ipconfig /renew
  - Network Adapter - Properties - IPV4
    - `No default gateway`
    - `“DHCP Enabled: Yes”`

- To Ask/Think:

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

VPN
-
-
Virtual IP
- check VIP via VIP manager

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
