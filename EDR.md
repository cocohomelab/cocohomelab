## EDR

- EDR is a security tool that monitors company devices in real time to detect suspicious behavior.
- Instead of just blocking known viruses, it watches how programs behave. If something acts unusually — like trying to steal data or spread to other systems — it alerts the security team.
- The advantage of EDR is that it not only detects threats but also allows us to quickly isolate an infected device, stop the malicious activity, and investigate what happened before it spreads further.
- Features:
  - RTT
  - SIEM
  - Sandbox

### Telemetry analysis

Telemetry analysis is the process of collecting, correlating, and interpreting endpoint, network, and identity data to detect abnormal or malicious behavior and support investigation and response.

`Turning raw security data into actionable detection and response decisions`

Endpoint Telemetry & Data Sources :
- Process Creation
- Parent-Child Process Relationships
- Command-Line Arguments
- Process Injection
- DLL Load Events
- File Creation / Modification
- Registry Changes
- Scheduled Tasks
- Startup Items
- Service Creation
- Kernel Events
- Driver Loading
- Network Connections
- DNS Queries
- Authentication Events
- Token Manipulation
- Privilege Use
- User Context
- Host Context

Local Analysis

Cloud or Centralized Analysis
- Behavioral analysis: Detect anomalies in process chains, network connections, or privilege use
- Heuristics & rules: Apply pre-configured detection logic
- Threat intelligence correlation: Match events against known attacker infrastructure or malware
- Machine learning / anomaly detection: Identify unusual patterns or first-seen activity

Actions Response (decision logic) :

    - When you do each action
    - Why you choose one response over another
    - Risk considerations (false positives, business impact)
Actions Response option: 
- Automated Response
- isolate the host
- kill processes
- quarantine files
- support live investigation
- (Prevention, Mitigation, Containment, Eradication, Remediation, Recovery)

- Quarantine devices
- Kill process
- Stop process
- Execute shutdown operating system
- Execute user logoff
- Schedule reboot
- End quarantine device

- 
- Fine tune
- Clean up
- Audit (system and user)
  - Client protection coverrage / persentage
  - User login and credential

- Triage a Detection

MITRE ATTAck - TTP

How does EDR support MITRE ATT&CK mapping?
- EDR maps endpoint behavior to ATT&CK techniques to help understand attacker tactics.

Answer:

Reference:

https://docs.trellix.com/bundle/mvision-endpoint-detection-and-response-product-guide/page/UUID-539597b6-3a64-e122-8981-097a24897557.html

https://www.edr-telemetry.com/windows -> EDR Telemetry of Modern EDR Solutions

https://detectionstream.com/

https://thedfirreport.com/

https://www.dfirblog.com/

https://lolbas-project.github.io/#

https://www.loldrivers.io/

https://gtfobins.github.io/ : List of Unix binaries that can be used to bypass local security restrictions in misconfigured systems.

https://attack.mitre.org/

https://caldera.mitre.org/

TryHackMe : Room :

https://tryhackme.com/room/introductiontoedrs

Lesson Learned:


https://tryhackme.com/room/wazuhct

https://tryhackme.com/room/atomicredteam

https://tryhackme.com/room/caldera

https://tryhackme.com/room/baselineanomalies

https://tryhackme.com/room/ipanddomainthreatintel

https://tryhackme.com/room/irplaybooks

### Mapping to Real-World Environment

🔹 Lab Step: Detecting Mimikatz execution
🔹 Real-World Equivalent:

- EDR would show LSASS access attempts

- SOC would monitor Event ID 10 (object access)

- Defender ATP would raise “Credential Theft” alert

- Analyst triage involves checking if the parent process is suspicious

- Confirm by checking if the machine is domain-joined and high-value

🔹 How SOC responds:

- Isolate endpoint

- Reset credentials

- Check lateral movement

- Review logs for persistence

✅ Real-World Mapping Examples

🛡 THM Malware Analysis → Real World

- Behavior → Detection rules

- Strings → YARA rules

- Network traffic → EDR timeline

- Persistence → IR triage checklist

🪪 THM Windows Logs → Real World

- Event IDs → SIEM correlation rules

- Log patterns → Alert tuning

- Sysmon configs → Detection engineering basics

🔐 THM Privilege Escalation → Real World

- Windows UAC bypass → Admin abuse monitoring

- Service misconfig → GPO hardening

- Token manipulation → EDR behavior analytics

🖥 THM Endpoint Protection Rooms → Real World

- Defender scans → Anti-malware baseline

- EDR behavioral blocks → IOC coverage

- Command-line monitoring → Incident triage
