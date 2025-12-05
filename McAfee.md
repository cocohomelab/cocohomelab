McAfee ePO (Trellix ePolicy Orchestrator) On-prem

Modules:
- McAfee Threat Protection ( ENS)
- McAfee Data Leakage Protection Endpoint

---

McAfee ePO (Trellix ePolicy Orchestrator)

Core Components:
- ePO Server
- SQL Database
- Agent Handlers
- McAfee Agent (MA) on endpoints
- Repositories (Master, Distributed)
- Extensions (Modules installed on ePO)
- Policies + Tasks
---
-	ePO License Key
-	McAfee Grant Number

- Detailed ePO Server Configuration
    - ePO Database Server
        - Microsoft SQL Server 
    - Agent Handlers
        - Default (1) 
    - Check in Extensions and Master Repository
      
|      Product                               |      Extension Name                                   |
|--------------------------------------------|-------------------------------------------------------|
|     Data Loss Prevention                   |     Data Loss Prevention                              |
|     Data Loss Prevention Manager           |     Data Loss Prevention Manager                      |
|     ePO-MER                                |     MER for ePO                                       |
|     File and Removable Media Protection    |     File and Removable Media Protection               |
|     GTI Proxy                              |     GTI Proxy Agent                                   |
|                                            |     GTI Proxy Appliance                               |
|     Help Desk Tool                         |     Help Desk Tool for MCP and DLPE                   |
|     McAfee Agent                           |     McAfee Agent                                      |
|     Policy Auditor                         |     Benchmark Editor                                  |
|                                            |     Benchmark Editor Content Distributor              |
|                                            |     Findings                                          |
|                                            |     PACore                                            |
|                                            |     PARollup                                          |
|                                            |     Policy Auditor                                    |
|     VirusScan Enterprise                   |     VirusScan Enterprise 8.8                          |

   - Distributed Repositories
            - Branch
            - SuperAgents
- Detailed Agent Configuration
      - tets
-  ePO Server Automation
    - Client Tasks (Install Endpoints)
    - Client Tasks: McAfee Agent
    - Server Tasks: Update Master Repository
    - Replicate: Master Pull (HTTP)
    - System: Purge Threat and Event Logs
    - System: Purge Server Task Log
    - System: Lost & Found Sorting Task
    - System: Active Clients in Inactive Systems folder Sorting Task
    - Server Tasks: System: Inactive Clients Sorting Task
- Deployment Method
    - Golden Image
    - ePO server push
    - ePO server web
    - SCCM, Tanium
    - Microsoft GPO
    - Manual Installation
        - FramePkg.exe /Install=Agent /ForceInstall /Silent

- Ports
    - McAfee ePO requires communication on a number of ports to be available. 

|      Communication Type                 |      Port                                 |
|-----------------------------------------|-------------------------------------------|
|     Agent to Server                     |     TCP 8280                              | 
|     Agent to Server (Secure)            |     TCP 8443                              | 
|     Agent Wakeup                        |     TCP 8288                              |
|     Agent Broadcast                     |     TCP 8289                              |
|     Console to Application Server       |     TCP 8243                              |
|     Client to Server (Authenticated)    |     TCP 8244                              |
|     Security Threats Communication      |     TCP 8801 (Default - Cannot Change)    |
|     SQL Server                          |     TCP 3333                              | 




---



### Policies + Tasks

McAfee ePO Policies

Key policy categories:
- Threat Prevention Policies
    - On-access scan
    - On-demand scan
    - Behavioral protection
    - Heuristic levels
- Firewall Policies
- Web Control Policies
- ATP / Adaptive Threat Protection
- Endpoint Security Platform
- Device Control Policies
- Exploit Prevention

You should know:
- How to create a new policy
- How to assign it to specific systems/groups
- How to test and tune policies
- How to avoid breaking production

Notes : 
Windows client machines and Windows Server machines require different policies and tasks, because servers and clients have different roles, performance requirements, workloads, and risk profiles.
This is critical to avoid outages.

##### 🖥️  WINDOWS CLIENT (Windows 10/11) — Recommended Policies & Tasks
Windows endpoints are used by end-users, so the focus is on:
- User protection
- Prevention
- Web control
- Application behavior
- Frequent scanning

##### ✅ Recommended Policies
1. Threat Prevention – On Access Scan (OAS)
    - Balanced scanning
    - Scan on read + write
    - High heuristic only for suspicious files
    - Enable PUP detection
2. Exploit Prevention
    - Enable default rules
    - Enable office macros blocking
    - Enable browser exploit mitigations
3. Adaptive Threat Protection (ATP)
    - Enable real protect
    - Enable JTI (dynamic behavior blocking)
    - Medium aggressiveness
4. Web Control
    - Block malicious URLs
    - Block risky categories (e.g., phishing)
    - Allow safe browsing enforcement
5. Firewall
    - Default client profile
    - Basic inbound block rules
    - Allow business applications only

Recommended Client Tasks
- Daily DAT/Engine Update
- Weekly Full Scan
- Daily Quick Scan
- Agent Wake-up Call
- Report collection
- Product deployment (ENS, Firewall, Web Control)


##### 🖥️ WINDOWS SERVER (2012/2016/2019/2022) — Different Approach
Windows servers should NOT use the same policies as clients. Performance and stability are top priority.

##### ✅ Recommended Policies for Servers

1. Threat Prevention – On Access Scan
    - Scan on write only
    - Disable scan on read (performance)
    - Reduced heuristics
    - Avoid scanning database or backup directories
    - Exempt: SQL, Exchange, IIS, backup software
2. Exploit Prevention
    - Enable only server-relevant rules
    - Disable rules that impact server apps
3. ATP
    - Lower aggressiveness
    - Behavior monitoring only
    - Disable high-aggressive blocking unless required
4. Firewall
    - Usually off for servers OR in monitoring mode
    - Apply custom rules for DMZ or web servers
5. Web Control
    - Disabled (servers don’t browse the web)

Key difference:
- Servers require policy tuning to avoid performance impact.

Recommended Server Tasks
- DAT/Engine Update (less frequent, e.g., every 6–12 hrs)
- No scheduled full scan (only manual or monthly at downtime)
- Minimal agent wake-up calls
- Server deployment tasks (ATP, ENS TP)
- System properties collection

### Troubleshooting
ePO Server
- McAfee Log Level 8
- Check services:
    - Trellix ePolicy Orchestrator Applications Server
    - Trellix ePolicy Orchestrator Event Parser
    - Trellix ePolicy Orchestrator Server
- 
Agent + Windows client machines
- Reinstall agent
- Reinstall module on Windows client machines
- Clean up 300 MB of free disk space on Windows client machines
- McAfee Profiler to create exceptions for trusted files, applications, or paths to improve performance without creating a security risk

