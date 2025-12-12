Wazuh HomeLab
- Built a Wazuh-based cybersecurity homelab to gain hands-on experience in SIEM, EDR, and XDR operations, demonstrating how diverse cybersecurity components integrate seamlessly.
- Explored how open-source telemetry, detection, and response map to enterprise security frameworks (MITRE ATT&CK, NIST, CIS).
- Implemented use cases including File Integrity Monitoring (FIM), Indicator of Compromise (IOC) management, and Active Response automation.
- Developed an understanding of how Wazuh parallels commercial solutions like Trellix, CrowdStrike, and Microsoft Defender for endpoint protection.

Key To understand:
- Concept
- Intergration

---
#### Security Tools / Threat Intelligence

Native integrations for threat detection.
- VirusTotal
- YARA
- OSQuery
- STIX/TAXII threat feeds
- AlienVault OTX
- CIS Benchmark SCAP
- MITRE ATT&CK mapping (built-in rules)

---

 #### Test Enviroment
 - Micro Workstation (physical) : RHEL + Wazuh
 - VM run on Windows 10 : Windows 10 
 - VM run on Windows 10 : Ubuntu

---
#### Deployment

4 step deployment strategy that actually works: planning phase.

- Map your infrastructure first (servers, workstations, network segments)
- Create deployment groups based on OS and function
- Use automation tools (Ansible, PowerShell, bash scripts)
- Set up centralized configuration management

---

#### Future Enhancement :
- intergrate with n8n
- Integrate with MCP (Model Context Protocol)
- Wazuh–MISP Integration
- Wazuh and Graylog for efficient log collection and analysis from all your endpoints.
- MISP to enhance your threat intelligence capabilities.
- Cortex and TheHive for streamlined incident response.
- Osquery to elevate your threat hunting and digital forensics efforts.


⭐ Summary Mapping (Simple Version)

Wazuh matches commercial EDRs in:
- FIM
- Logging
- IOC detection
- Compliance
- Vulnerability scanning
- Process monitoring
- Basic response actions

Commercial EDRs exceed Wazuh in:
- Behavioral detections
- Advanced analytics / ML
- Real-time threat blocking
- Endpoint isolation
- Enterprise-scale automation
- Deep kernel visibility


Reference:

https://tryhackme.com/room/wazuhct

https://docs.trellix.com/bundle/mvision-endpoint-detection-and-response-product-guide/page/UUID-539597b6-3a64-e122-8981-097a24897557.html

https://github.com/socfortress/Wazuh-Rules : Advanced Wazuh Detection Rules

https://www.misp-project.org/2025/10/06/wazuh-integration.html/ : Wazuh–MISP Integration

https://github.com/MISP/wazuh-integration : Wazuh–MISP Integration

✅ How to make your GitHub notes count as a real portfolio:

Do these and it becomes a strong portfolio:
- Organize your repo clearly
  - e.g., /CrowdStrike, /Trellix, /Wazuh, /EDR, /SIEM
- Add real hands-on examples
  - Screenshots
  - Lab steps
  - Detection queries
  - Configuration snippets
  - Troubleshooting notes
- Include a README
  - Explain what the repo is and what you learned.
- Show your thinking
  - Add summaries, diagrams, comparisons (e.g., “Wazuh vs CrowdStrike”).
  - Interviewers love when you show analysis, not just notes.
