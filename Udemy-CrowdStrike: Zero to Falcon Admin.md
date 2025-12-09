## CrowdStrike: Zero to Falcon Admin
Hailie Shaw, Blue Team Consulting

### Master the Falcon Platform from an Administrative Perspective

This course is designed to provide learners with an in-depth understanding of CrowdStrike/EDR, a powerful endpoint security tool. Participants will learn how to install and configure CrowdStrike/EDR, manage hosts, create and manage prevention policies, customize IOAs, manage exclusions and quarantines, and troubleshoot issues.

Module 1: What is CrowdStrike/EDR
- Introduction to CrowdStrike/EDR
- Understanding Endpoint Detection and Response (EDR)
- Key features and benefits of CrowdStrike/EDR

Module 2: Users and Roles
- User and role management in CrowdStrike/EDR
- Understanding permissions and access levels
- Best practices for user and role management

Module 3: Installation
- CrowdStrike/EDR installation prerequisites
- Installing CrowdStrike/EDR on endpoints
- Post-installation configurations and best practices

Module 4: Troubleshooting
- Troubleshooting common issues with CrowdStrike/EDR
- Best practices for effective troubleshooting

Module 5: Uninstalling & Sensor updates
- Uninstalling CrowdStrike/EDR from endpoints
- Updating CrowdStrike/EDR sensors
- Best practices for sensor management

Module 6: Host management
- Managing hosts using CrowdStrike/EDR
- Understanding host groups and policies
- Best practices for host management

Module 7: Prevention policies
- Creating and managing prevention policies in CrowdStrike/EDR
- Understanding policy rules and configurations
- Best practices for policy management

Module 8: Custom IOAs
- Creating custom Indicators of Attack (IOAs) in CrowdStrike/EDR
- Understanding IOA rules and configurations
- Best practices for custom IOA management

Module 9: Exclusions and Quarantines
- Managing exclusions and quarantines in CrowdStrike/EDR
- Understanding exclusion and quarantine rules and configurations
- Best practices for exclusion and quarantine management

What you’ll learn
- Gain mastery of the Falcon platform: Learn how to navigate and use the various features of the CrowdStrike Falcon platform related to administrative duties.
- Learn the core principles of endpoint protection, including deployment, host management, troubleshooting, and response.
- Learn best practices for security operations: Gain an understanding of industry-standard security practices and how to apply them to your organization.
- Cybersecurity Engineering Concepts for Configuring an EDR Console

## Notes

---

Module 1: What is CrowdStrike/EDR
- Introduction to CrowdStrike/EDR
- Understanding Endpoint Detection and Response (EDR)
- Key features and benefits of CrowdStrike/EDR

🛡 What is an EDR tool?
- Endpoint detection And response.
- Focuses on detecting and responding to security threats on ednpoints
- Uses a combination of signature-based and behavioral-based detection techniques
- Cab leverage machine learning and artificial intelligence to improve accurancy and efficiency
- Provides real-time monitoring and detection of potential threats
- Can initiate autoomated resosnses to detect threats
- Provides detailed logs and forensic data for further investigation and prevention 
🛡 What makes Crowstrike Stand Out?
- Advanced capabilities
- Flexible deploment options
- User-friendly interface
- Strong customer support
- Lots of additional features within the console

Key Takeaways :

⭐ 1. **What is an EDR?**

**EDR = Endpoint Detection & Response**

* Deployed as an **agent** (MSI, PKG, etc.) to endpoints (servers + workstations)
* Monitors, detects, and responds to threats on endpoints

🔍 **Three Detection Types**

1. **Signature-based (Static)**

   * Matches known, pre-written patterns
   * Similar to traditional antivirus
   * Good for known threats, not adaptable

2. **Behavioral-based (Dynamic)**

   * Detects suspicious parent/child process behavior
   * Example: *PowerShell → cmd → unknown malware.exe*
   * Catches novel or obfuscated threats

3. **Heuristic-based**

   * Learns baseline of normal activity over time (months)
   * Flags outliers or anomalies
   * Combines signature + behavior + activity patterns

⭐ 2. **EDR vs XDR**

* **EDR** focuses on endpoint threats
* **XDR** adds broader capabilities:

  * Threat intelligence
  * Vulnerability scanning
  * Active Directory enumeration
  * Identity protection
  * Cloud workload assessments
  * Sandbox analysis
  * And more

**CrowdStrike = a full XDR platform**, not just an EDR.

⭐ 3. **EDR Capabilities**

* Real-time (near real-time) monitoring
* Machine learning + AI detections
* Automated response actions
* Detailed logs, telemetry, and forensic data
* Investigation and threat hunting support

⭐ 4. **Major EDR Players**

* **CrowdStrike** (market leader)
* **Carbon Black**
* **SentinelOne**
* **Huntress**

⭐ 5. **Why CrowdStrike Stands Out**

🎯 **Key Strengths**

* True **XDR** platform with many optional modules
* Rich features beyond EDR:

  * Threat intelligence
  * Vulnerability management
  * Identity/AD security
  * Cloud posture assessments
  * Sandbox analysis
* **Lightweight agent** and **minimal system impact**
* **Broad OS support**
* Extremely **user-friendly UI**

🎯 **Splunk-Like Experience**

* Query language resembles **SPL**
* Dashboards and widgets feel Splunk-like
* Easy transition for anyone with Splunk experience

🎯 **Strong Customer Support**

* 24/7 support portal
* Fast response times
* High-quality engineering team

### 🎯 **Deployment Flexibility**

* Modern, scalable cloud-native architecture
* Quick onboarding & easy deployment

⭐ 6. **Funny But True: “EDR = Expensive Data Recorder”**

* EDR alone doesn't fix everything
* You still need analysts & administrators reviewing alerts
* CrowdStrike helps, but human monitoring is essential

📌 **One-Sentence Summary**

**EDR tools detect and respond to endpoint threats using signature, behavioral, and heuristic methods—CrowdStrike stands out as a powerful XDR platform with strong usability, broad features, and high-quality support.**

---

Module 2: Users and Roles
- User and role management in CrowdStrike/EDR
- Understanding permissions and access levels
- Best practices for user and role management

🛡 Roles
- Permission 
- Users are assigned by the Falcon admin
- Must have an associated domain email/CID association
- CID needs to be associated with your companies email domain, if not=CS customer support

✅ Top Roles:
- Falcon Admin - doesn't come with manage custom IOA or connect to host (RTR and custom IOAs manager)
- Preventions Policy Admin
- Falcon console guest
- Dashboard Admin
- Desktop Support Analyst
- Workflow Author
- Help Desk Analyst

🔹 Role Access in cumulative to combine roles for capabilities

✅ A note on Real Time Responder (RTR) Roles
- RTR - Read only analyst - can't do custom scripts ot"PUT" actions
- RTR - Active Responder - can use the "GET" command, some custom scripts
- RTR - Administrator - custom scripts, upload files, run commands 

✅ How to add a new user
- Host setup > falcon users > user management
- Can reset 2FA, passwords, delete users, create users

✅ Setting up Email notifications
- Support and resources > general settings > scroll to the bottom
- Endpoint security > crowstrike incidents
  - Can set up email notifications 

Key Takeaways :

⭐ 1. **Roles = Permissions Bundles**

* CrowdStrike uses **roles** to group permissions.
* Users can have **multiple roles** assigned.
* **Do NOT over-provision** users—follow least privilege.

  * Overprivileged accounts = major risk if compromised.

⭐ 2. **Email Domain Requirement**

* **User email must match the customer’s registered domain.**
  Example: If the customer ID is tied to *blueteamwins.com*, all users must have *@blueteamwins.com*.
* Gmail, Yahoo, Hotmail, etc. **cannot** be added.
* CrowdStrike almost never approves exceptions.

⭐ 3. **Critical Role Behavior**

🔹 **Falcon Administrator**

* Full console admin but **missing two capabilities by default**:

  1. **RTR (Real Time Response)**
  2. **Custom IOA** (Indicators of Attack)
* Must add those roles **manually** if needed.

🔹 Other common roles:

* Prevention Policy Admin
* Falcon Console Guest
* Dashboard Admin
* Desktop Support Analyst
* Workflow Author
* Help Desk Analyst
  (Each well-documented in the console.)

⭐ 4. **RTR (Real Time Response) Roles**

RTR = Remote shell / live terminal into an endpoint.

Only **three** RTR roles exist:

1️⃣ **RTR Read-Only Analyst**

* View only
* No actions, no scripts, no closing alerts
* Safest for entry-level analysts

2️⃣ **RTR Active Responder**

* Some “get” commands
* Limited custom-script execution
* Basic containment actions

3️⃣ **RTR Administrator**

* **Full RTR capabilities**
* Run *all* commands
* Run *any* custom PowerShell script
* Upload/download files, take full action
* No practical limitation

➡️ **Even Falcon Admins cannot use RTR unless one of these roles is assigned.**

⭐ 5. **Adding a New User**

**Path:**
`Host Setup → Falcon Users → User Management`

Steps:

1. Click **Create User**
2. Enter name, email (must match org domain)
3. Assign roles
4. Save

After creation (via the 3-dot ellipsis):

* Reset password
* Reset MFA
* Delete user
* Edit first/last name
* Add/remove roles
  (Note: Email cannot be changed—delete & recreate instead.)

⭐ 6. **Email Notifications**

Two ways to configure:

Option 1 – General Settings

`Support & Resources → General Settings → (scroll to bottom)`

Option 2 – Incident Notifications

`Endpoint Security → Crowd Score → Incidents → Notification Settings`

If you **don’t see notification options**:

* You probably **don’t have the right role**.

⭐ 7. **Incidents vs Detections**

* **Detections:** Individual alerts/events.
* **Incidents:**

  * A *collection of related detections*
  * CrowdStrike automatically promotes groups of detections into a **single incident** when the combined activity is significant.
  * Richer description, additional context, and a consolidated timeline.

Incidents have their own console section but can also be viewed from the detections area.

📌 **One-Sentence Summary**

**Users in CrowdStrike are permissioned through roles, email domains must match the customer ID, RTR requires special roles, and incidents are grouped detections with more detailed context.**

---

Module 3: Installation
- CrowdStrike/EDR installation prerequisites
- Installing CrowdStrike/EDR on endpoints
- Post-installation configurations and best practices

✅ Manual vs Automatic Installs
- Should be able to complete sensor roll out to all hosts within 45 days
  - Do not shutdown or reboot the host while the sensor is installing
1. Manual Install
  - Small number to deploy
    - Hosts setup and management > sensor download > installer based on OS > download > copy CID
    - Doubleclick the pkg file > CID > go through installation
    - Verify sensor is running: sc.exe query csagent
2. Automatic install
  - SCCM or automated push
  - Host setup > sensor downloads > sensor installer based on OS > download > copy ID
  - Run on CLI via your deployment tool
    - \<installler file name> /install /quite /norestart CID=\<Customer ID>

✅ Points of Note
- Make sure you have the correct installer for version OS
  - Sensor Release Matrix in knowledge based article (n-1. n-2) 
- FQDN need to be on allowed list = Documentation Cloud IP addresses
  - need to be alllowed in network for those, see docs for IPs and domains for data between sensors and cloud  

✅ Networking Items
- Installer makes several attempts to connect to the cloud
  - If failure, it will uninstall
- Network Dependencies:
  - outbound SSL traffic (port 443)
- Sensors uses certificate pinning
  - add falcon domain and IPs to bypass any firewall/proxy deep packet inspection = DPI
  - pinning=what certs are valid, certs get pinned CA public keys to check against

🔹 Specific URLs and IPs will differ based on what cloud instance yu are on (US1, US2, GOV, etc)

🔹 Check Cloud IP Documentation

✅ Windows Installation
- Requirements:
  - LM hosts (might be disable)
  - Network store interface
  - Windows base filtering engine
  - Windows power services
  - WinHTTP auto proxy (if using proxy)

🔹 In order to use the NGAV that comes with CS, Windows Defender must be disable
* Can't change the installation path

- How to :
  - GUI or CLI, both need company code (CID)
  - \<installer file name> /install /quiet /norestart CID=\<Customer ID>
  - /quite = no UI prompt
  - /norestart = ensures the host doesn't reboot after install
  - sc.exe query csagent

✅ Linux Installation
- CLI Install option, no GUI available. *make sure you check what OSs are supported "uname -a" to get kernel version (to make sure the version is supported)
  - Ubuntu : sudo dpkg -i \<installer file name>
  - RHEL, CentOS, Amazon Linux : sudo dnf install \<installer file name>
  - SLES : sudo zypper install \<installer file name>
- Register it with: sudo /opt/crowdstrike/falconctl -s --cid=\<CID>
- Configure CrowdStrike : sudo /opt/crowdstrike/falconctl configure
- To start the CrowdStrike service : sudo systemctl start crowdstrike
- To check the falcon service is running : ps -e | grep falcon-sensor

✅ MacOS Installation (revisit to jotdown notes)
- Elavated privillages needed
- JAMF to script out and install, always more customization on the CLI compared to GUI
- Grab the right sensor pkg file, double click and roll or go to CLI
  - Install file on host
  - License the sensor with CID
- To install : sudo installer -verboseR -package \<installer filename> -target /
- Register the sensor : sudo /Applications/Falcon.app/Contents/Resources/falconctl license \<CID>
- sudo /Applications/Falcon.app/Contents/Resources/falconctl load
- sudo /Applications/Falcon.app/Contents/Resources/falconctl stats

** Kernel extensions (KEK) will need to be approved

✅ Installation Tokens (Registration Token)
- Host setup > installation tokens
  - 1 year, 90 days, 30 days, does not expire
  - can aligh best to your org, maybe 30 days is best
  - can stagger all 50 that are available to you
- Prevent unauthorized installations
- Opt-in : it off by default
- Set expiration to rotate tokens
- 50 tokens per CID
- Create in falcon console or through API
- Keep them secret, for preventing anyone from installing the sensors
- Audit log will show who has tokens on the console

Key Takeaways : 

**1. Installation Types**

**Manual Install**

* Best for **small numbers of hosts** (one-off installs).
* Navigate to **Host Setup & Management → Sensor Downloads** to get the installer.
* **Copy your Customer ID (CID)** — required to register the sensor.
* Run the installer manually; enter CID during the wizard.
* Verify sensor is running:
  **`sc query csagent`** (Windows).

**Automatic / Mass Deployment**

* For **large-scale rollout** (hundreds to thousands of hosts).
* Use **SCCM, Intune, JAMF, scripts, or other deployment tools**.
* Install silently using something like:
  `WindowsSensor.exe /install /quiet /norestart CID=<CID>`
* **Do NOT reboot during installation**; it can cause the sensor to fail.
* Goal: complete rollout **within 45 days**, but follow your environment’s limits.

**2. Best Practices for Deployment**

* **Deploy in stages** (pilot/test groups → production).
  Never deploy to full prod immediately.
* Ensure **exclusions/whitelists** are configured if another AV is still present.
* Ensure **correct OS installer** is used and that the OS version is supported.
* Follow **CrowdStrike’s Sensor Release Matrix**; use current or N-1 versions.
* Configure firewall/proxy rules **before installing**.

**3. Network Requirements**

* Sensor attempts to connect to the cloud for ~20 minutes; if it can’t, it **uninstalls itself**.
* Allow outbound **HTTPS (443)** to CrowdStrike cloud.
* Whitelist **CrowdStrike FQDNs, IPs, and certificates** (varies by US-1, US-2, GovCloud, etc.).
* CrowdStrike uses **certificate pinning** — proxies/firewalls doing **DPI** may break installation unless bypassed.

**4. Windows Requirements**

* Required Windows services:

  * **Network Store Interface (NSI)**
  * **Windows Filtering Platform (WFP)**
  * **HTTP Auto Proxy** (if using proxy)
  * **Power Services**
* For Falcon **Next-Gen AV**, **Windows Defender must be disabled**.
* Installation path **cannot be changed**.
* Verify service status:
  **`sc query csagent`**.

**5. Linux Install**

* No GUI install; **CLI only**.
* Check kernel compatibility using:
  **`uname -r`**
* Two-step process:

  1. **Install** package (apt, yum, zypper, etc.).
  2. **Register** the sensor:
     `falconctl -s --cid=<CID>`
* Start service and verify via:
  **`ps -ef | grep falcon-sensor`**.

**6. macOS Install**

* Requires **elevated privileges**.
* Deploy via **JAMF** or CLI.
* Two-step process: install → register with CID.
* macOS requires manual or MDM-based approval of:

  * **System Extensions / Kernel Extensions**
  * **Full Disk Access**
* Use **falconctl** to register and verify operation.

**7. Installation Tokens**

* Located under **Host Setup → Installation Tokens**.
* Off by default — **enable manually**.
* Purpose: prevent unauthorized install/uninstall (anti-tamper).
* Token lifetimes: **30 days, 90 days, 1 year, or no expiration**.

  * Best practice: **30 days** for security.
* Limit: **50 tokens per CID**.
* Can be created via UI or **API** (copy the API secret key immediately).
* Token usage in CLI:
  `--provisioning-token <TOKEN>`
* Audit logs show who created/deleted tokens or keys.

**Summary**

This module emphasizes correct installer selection, CID handling, firewall preparation, staged rollout, OS-specific requirements, and the use of installation tokens for security. The most critical points: **don’t reboot during install, whitelist network paths first, deploy in controlled phases, and verify the sensor is running**.

---
Module 4: Troubleshooting
- Troubleshooting common issues with CrowdStrike/EDR
- Best practices for effective troubleshooting

✅ The Checklist
- Is the OS supported by CS?
- System requirement met for what services need to be running?
- KEX approved for Macs?
- Did you verify that the sensors is running?
- Network requirement met for the correct enable/allowed lists at the Firewalls?
- `netstat.exe -f` with admin creds to see if the falcon domain name or falcon cloud IPs is showwing an established connection
- If can connect to the cloud: can host get on the internet? Are you using a proxy and are those settings correct? Firewall/Network settings correct? Check that the host trust the CS CA?
- Are there other products interfering with the falcon sensor? (Avast, McAfee, etc)
- Is the timeout issue? Agent install will timeout after 20min. Can override with the `ProvNoWait` parameter in the command line: \<installer file name> /install /quite /norestart CID=\<Customer ID> ProvNoWait=1
- What do the logs say? Any error codes present? (%LOCALAPPDATA%\temp\ for anything matching crowdstrike around time of installation)

✅ RFM (Reduced Functionality Mode)
- The sensor enters safe mode, limited logging if any based on the OS affected
- Unsuppoeted Kernel updates
- Use the sensor dashboards available to check what sensors have entered RFM

🔹 Options to address:
- Rollback the system updates or downgrade to an older version of that system
- Bear and grit it until falcon release a sensor update for that Kernel

Key Takeaways:

This module provides a **step-by-step troubleshooting methodology** that solves **~99% of sensor issues**.
It moves from **simple → complex**, ensuring you don’t jump straight into logs before checking basics.

**1. Start With the Basics**

✔ **1. OS Supported?**

* Verify the target OS is **officially supported** by CrowdStrike.
* Unsupported OS = failed install.

✔ **2. System Requirements Met?**

* Check required **system services and components** for the OS.

  * Examples:

    * Windows: NSI, WFP, HTTP Auto Proxy, etc.
    * macOS: System/Kernel Extension approvals.
    * Linux: Supported kernel version.

✔ **3. Is the Sensor Running?**

* Windows:
  **`sc query csagent`**
* Linux:
  **`ps -ef | grep falcon-sensor`**
* macOS:
  **`falconctl stats`**

If it’s not running → fix before going further.

**2. Network Troubleshooting (Most Common Problem Area)**

✔ **4. Firewall & Network Rules Correct?**

* Ensure **all CrowdStrike FQDNs, IPs, URLs**, and **port 443** are allowed.
* Must be done **before installation**.

✔ **5. Can the Endpoint Reach the Cloud?**

* **Ping** CrowdStrike cloud URLs/IPs.
* If ping works → check connectivity:

  * **`netstat -f`** (Windows) to confirm **established connections**.

✔ **6. Does the Host Have Basic Internet Access?**

* If internet is broken → everything else fails.

✔ **7. Proxy Settings Correct?**

* If using a proxy:

  * Ensure proper configuration according to documentation.
  * Check for **DPI (deep packet inspection)**—can break certificate pinning.

✔ **8. Certificate Trust**

* Host must trust the **CrowdStrike Certificate Authority** (e.g., GoDaddy).
  Missing CA = connection failure.

**3. Installer & Command Line Validations**

✔ **9. Correct Installer Package?**

* Wrong OS version, architecture (ARM vs x86), or wrong sensor version can break install.

✔ **10. Correct CID (Customer ID)?**

* A wrong CID registers the host to **someone else’s tenant**.

✔ **11. Correct Command Line Syntax?**

* Validate silent install parameters, tokens, and flags.

**4. Timeout Issues**

✔ **12. Did the Sensor Fail After 20-Min Timeout?**

* Sensor tries ~20 minutes to reach the cloud; if it can’t, it **uninstalls itself**.
* Use the flag to bypass the wait:

  * **`--prov-no-wait=1`**
* This is useful in slow or restricted network environments.

**5. Conflicts With Other Products**

✔ **13. Other Security Tools Interfering?**

* AV or EDR running without proper exclusions may:

  * Block the sensor
  * Delete files
  * Prevent registration

Make sure bidirectional exclusions are in place.

**6. Logs (Last Resort)**

✔ **14. Review Local Sensor Logs**

* Location (Windows):
  **`%localappdata%\Temp`**
* Look for:

  * Install logs
  * Error codes
  * Fail timestamps

Then compare error codes with **CrowdStrike documentation**.

**7. If All Else Fails**

✔ **15. Open a Support Ticket**

Include:

* What steps were checked in the troubleshooting list
* Logs
* Error messages
* OS info, installer version, network details

Support will respect a well-prepared ticket.

**8. Reduced Functionality Mode (RFM)**

**What is RFM?**

* Sensor goes into a **limited/safe mode** when it encounters unsupported conditions.

**Common Causes**

* **OS/kernel updates not yet supported** by the current sensor.
* Sensor doesn’t understand the updated kernel → drops into RFM.

**Behavior**

* Limited or no logging
* Reduced protection
* Impacts visibility

**Actions When a Sensor Enters RFM**

1. **Wait for CrowdStrike to release a sensor update** supporting the newest kernel/OS.
2. **Roll back the OS/kernel update**, or downgrade to a supported version.

Use the **Sensor Dashboard** to identify sensors in RFM.

**Summary**

Module 4 provides a **repeatable troubleshooting checklist** covering:

* OS compatibility
* System requirements
* Sensor state
* Network connectivity
* Installer correctness
* Conflicts
* Logs
* RFM behavior

Following the checklist solves nearly all installation and connection issues.

---

Module 5: Uninstalling & Sensor updates
- Uninstalling CrowdStrike/EDR from endpoints
- Updating CrowdStrike/EDR sensors
- Best practices for sensor management

✅ Steps for Uninstall 
- Control panel > programs and features > uninstall
- Download a CS uninstall tools from "Tools Downloads" in console
  - CSUninstallTool.exe
  - HKLM\system\crowdstrike should be gone
- Find the host in host management, reveal maintenance token and copy
  - Support > tool download > sensor removal tool based on OS > download it
  - Uninstall via CLI :
    - Windows :
      - CSUninstallTool.exe MAINTENANCE_TOKEN=<token> /quiet
      - CSUninstallTool.exe /quiet
    - MacOS
      - sudo /Library/CS/falconctl uninstall --maintenance-token (for 1 host)
    - Linux
      - Ubuntu : sudo apt-get purge falcon-sensor
      - RHEL, CentOS, Amazon Linux : sudo dnf remove falcon-sensor
      - SLES : sudo zypper remove falcon-sensor
- Use "PUT" file of CSUninstallTool.exe from "Tools Downloads" onto CS files
- Put the file on the host; Then run "run CSUninstallTool.exe MAINTENANCE_TOKEN=<token> /quiet  - from RTR
- Valodate the sensor uninstall by navigating to HKLM\system\crowdstrike\ and C:\windows\system32\drivers\crowdstrike

✅ Uninstall and Maintenance Protection
- Can't uninstall without a token if maintenance protections is enabled
- Bulk maintenance mode: Not recommended globally, one token to rule them all Sensor update has to be off
- Use targeted hosts groups which require manual updates
- Bulk Uninstall:
  - 1 Token for all hosts in that policy or with the bulk maintenance mode enable  

✅ Sensor Updating
- Should be in a policy
- Host setup and management > sensor update policies > create new > name it > create
- Set the settings:
  - uninstall and maintenance protection : on
  - sensor version : Auto-latest or N-1 or whichever you want to set
  - Auto-latest = test pilot machines to see how the latest sensor goes
  - N-1 or N-2 for best practice
  - Sensor version Updates off = manual management of the updated sensor versions

✅ Update Throttling
- Limit number of hosts performing updates at once
- Think about the network resources it takes to update 5000 endpoints all at the same time...
- Set the number of hosts peer minutes that you want to have updated in Support and Resources > General Settings
- Best Practice:
  - TEST groups!
  - N-1
  - N-2 for the paranoid
  - Go Slow 

Key Takeaways:

⭐ 1. **Golden Rule: EVERYTHING in CrowdStrike = Groups + Policies**

* Always manage hosts through **groups**, with **policies** assigned to those groups.
* This applies to:

  * Sensor uninstall
  * Sensor update
  * Maintenance mode
  * Any environment-wide configuration

⭐ 2. **Uninstalling Sensors — Best Practices**

✔ To uninstall properly, your policy must:

1. **Enable Sensor Uninstallation & Maintenance**
2. **Turn OFF Sensor Version Updates**

✔ Why?

* Maintenance protection prevents tampering → requires **maintenance token**
* Updates must be off so the uninstall isn’t overwritten by auto-update

⭐ 3. **Sensor Uninstall Methods**

**A. One-off / Local Uninstall**

* Windows:
  `Control Panel → Programs & Features → Uninstall CrowdStrike Falcon Sensor`
* Mac/Linux equivalents available

**B. Using the CrowdStrike Uninstall Tool**

* Download at: **Support → Tool Downloads → Sensor Removal Tool**
* Run with maintenance token:

**Windows example:**

```
CrowdStrikeUninstallTool.exe --maintenance-token <TOKEN> --quiet
```

**Mac example:**

```
sudo falconctl uninstall --maintenance-token <TOKEN>
```

**Linux examples:**

* Ubuntu: `sudo apt-get purge falcon-sensor`
* RHEL/CentOS: `sudo yum remove falcon-sensor`
* SUSE: `sudo zypper remove falcon-sensor`

**C. Uninstall via RTR (Real Time Response)**

* Upload uninstall tool via RTR
* Use **put** command to drop file
* Run uninstall command from shell
* Must have RTR role assigned (active or admin)

⭐ 4. **Verify Sensor Is Gone**

**Windows:**

* Registry key removed:
  `HKLM\System\CrowdStrike`
* Driver removed from System32

**Linux/Mac:**

* No CrowdStrike PID visible
* Service/process removed

⭐ 5. **Maintenance Protection & Tokens**

 🔹 Key rule:

**If maintenance protection is enabled → you CANNOT uninstall without the maintenance token.**

* Prevents:

  * Threat actors disabling the sensor
  * End-users uninstalling it to bypass security
* Always enable maintenance protection (best practice)

⭐ 6. **Bulk Maintenance Mode**

Used to uninstall the sensor from **multiple hosts** using **one maintenance token**.

 ✔ Good for:

* Large, controlled migrations
* Temporary maintenance on a defined subset

 ❌ Bad (and dangerous) for:

* Applying to ALL endpoints
* Poor group management
* Threat actor obtaining the token → mass uninstall

Best practice:

* Create **targeted host groups**
* Use **bulk maintenance** ONLY for those specific hosts
* Keep auto-updates OFF in that policy

⭐ 7. **Updating Sensors (Sensor Update Policies)**

 ✔ Sensor updates are always done through:

`Host Setup & Management → Sensor Update Policies`

 The policy defines:

* Which **sensor version** endpoints will use
* Whether **auto-update** is enabled
* Throttling settings

Version Strategy:

* **N (latest)** = risky for production
* **N-1** = recommended for production
* **N-2** = conservative/stable option
* Don’t go beyond N-2 → means you're falling behind too far

⭐ 8. **Auto-Update Best Practices**

* **Do NOT auto-update production**
* Use **test groups** first:

  * A few servers
  * A few workstations
  * Various OS types

Let test groups run for a while before pushing to prod.

⭐ 9. **Update Throttling**

Prevents bandwidth overload when thousands of endpoints update.

Configure in:

`Support & Resources → General Settings → Sensor Update Throttling`

 Set "hosts updated per minute":

* Small org: 50
* Medium: 250
* Large: 500–1000
  (Depends on network bandwidth)

Always test throttling before full rollout.

📌 **One-Sentence Summary**

**Uninstallation and updates in CrowdStrike are managed through host groups and policies, require maintenance protection and tokens, should be carefully throttled, and must be tested using controlled groups before affecting production.**

---

Module 6: Host management
- Managing hosts using CrowdStrike/EDR
- Understanding host groups and policies
- Best practices for host management

✅ Host Groups
- Dynamic
  - Use whenever possible and can be automated
  - AD and dynamic is a good way to manage hosts, OU grouping
- Static
  - Defined manually via host IDs/Agent IDs list or by selecting them in the console
  - Good for testing of systems that you test every time
  - Can cause duplications
  - Only if you have a relly good nomenclature for all your hosts... not likely
  - AIDs can get pretty long to manage them by that random strings of names
  - Can assign up to 1k hosts to a static group at a time

```
Make one:
- Host setup > host groups > add new group > name and fill out > add group > edit > set filter
  - Filters only come from the sensors that are installed and sebd the data back to console
- A host can be in multiple groups with each group targetting diffrent policies
```
- Roll out your groups slowly, with small subsets of hosts to use as a samples
- By default, all your Assigned Policyes to your hosts groups are BLANK. You add the policies as you go configure the host groups (firewall, response, ML, IOAs, preventions, update policies)
- Be wise in what you use to set your host groups matching policy:
  - OU, platform, usage of wildcarhs
  - Leverage sensor tags where it makes sense 
 
✅ Tagging Hosts
- For organizations and filtering on your hosts
- Sensor grouping tags: added during sensor install:
~~~
CLI:
GROUPING_TAGS="HR,Prod" : at the end of the installation CLI command, after company code (windows)
falconctl grouping-tags set "tags" : MacOS
falconctl -s -- tags="tag1,tag2" : linux
~~~
DON'T USE SPACES

- Sensor grouping tags, if messed up on Windows install, will need to be fixed in the registery and then reboot and then new update from the sensor will make the chage needed
  - configured on the sensor themselves, only way to edit is via the registery
- Falcon grouping tags: in the console, can add more details to them if needed
- 237 -character limit for the tags, can have 50 tags per host, 1000 tags per CID  

✅ Hosts that don't check in
- If host hasn't checked in past 45 days, it will age out, sensor is gone with it. Sensor needs to be reinstalled
- If a deleted host has an active sensor, the detections will still come into the console
- Host management > trash can icon > info for hosts that have been deleted or aged off (Can restore) 

✅ Helpfull Host Reports
- Dashboard and Reports > all dashboards >
- Exec Summary and sensor health are good ones

Key Takeaways:

**1. Two Types of Host Groups**

CrowdStrike host groups allow you to organize endpoints and assign policies.

**A. Dynamic Host Groups (Preferred)**

* Automatically assign hosts based on **filters/criteria**.
* Examples of filters:

  * OS = Windows / Linux / macOS
  * Server vs. Workstation
  * AD OU
  * Sensor version
  * Tags
* A host automatically joins the group if it matches all filters.
* You can set **multiple criteria** (AND logic) to make groups more granular.
* **Flexible**, **automatic**, and ideal for production environments.
* Supports **wildcards** (`*`) for pattern matching (e.g., Version = `5.*`).
* Filters only appear once sensors send the relevant data back to the console.

**Best practice:**
Use dynamic host groups for **99% of real-world deployments**.

**B. Static Host Groups**

* You must manually assign hosts by:

  * Hostname
  * Host ID
  * Agent ID (AID)
* Host membership **does not change automatically**.
* Useful for:

  * Testing (e.g., sensor update pilots)
  * High-control scenarios
  * Special groups like traveling employees
* Limited to **1000 hosts per static group**.

**Downside:**
Requires extremely clean asset naming conventions—rare in most organizations.

**2. Agent ID (AID)**

* Unique identifier for each sensor.
* Problems occur in virtual/VDI environments if golden images are cloned **without sysprep** → multiple hosts sharing the same ID (big issue).

**3. Host Group Overlaps & Policy Precedence**

* A host **can belong to multiple groups**.
* Each group may have a different policy assigned.
* **Policy precedence** determines which one wins.
  The highest-ranked policy applies to the host.
* You will revisit precedence later in the course.

**4. Rolling Out Host Groups**

* Deploy gradually using a small sample group first.
* Policies assigned to host groups start **blank**—you must configure them.
* Policies include:

  * Sensor update policies
  * Prevention/Detection ML settings
  * Custom policies
  * RTR (Real Time Response)
  * Firewall
  * And many more

The policy catalog is large—experience makes it easier.

**5. Sensor Tagging**

Two types of tags:

**A. Sensor Grouping Tags (set at install time)**

Used in filters for dynamic groups.

**B. Falcon Grouping Tags (in console)**

Additional metadata applied to hosts.

**How many tags?**

* Up to **50 tags per host**
* Up to **1000 tags per customer**
* Max length: **237 characters**

**Tagging Syntax (IMPORTANT)**

**Windows:**

```
GROUPING_TAGS=prod,critical
```

Placed *after* the `SSO=CustomerID` parameter.
**Never use spaces.**
Spaces require painful registry edits + reboot.

**macOS:**

```
sudo falconctl grouping-tags=set prod,critical
```

**Linux:**

```
sudo /opt/CrowdStrike/falconctl --grouping-tags="prod,critical"
```

Use commas, **no spaces**, to add multiple tags.

**6. Host Check-In Behavior & 45-Day Rule**

* If a host **does not check in for 45 days**, it **ages out** of the console.
* The sensor becomes inactive and must be **reinstalled**.

Deleted hosts:

* Clicking the **trash can** removes the host from the UI **but does NOT uninstall** the sensor.
* Deleted/aged-out hosts remain in the trash for 45 days.

**Recommendation:**
Regularly compare:

* Your internal inventory
* CrowdStrike Host Management export

to catch missing or inactive sensors.

**7. Dashboards, Reports, and Monitoring**

Useful dashboards:

* **Executive Summary**
* **Sensor Health**
* **Inactive Sensors** (very important)

Use filters such as:

* Hostname
* Days since last check-in (>30)
* Version
* RFM (Reduced Functionality Mode)

You can export CSVs and monitor hosts approaching the 45-day expiration.

Bookmark important pages for quick access.

**8. Best Practices Summary**

✔ Prefer **dynamic host groups**

✔ Use granular filters and wildcards

✔ Use static groups for test pilots or special cases

✔ Tag hosts carefully (no spaces)

✔ Monitor hosts with dashboards and exported reports

✔ Reinstall sensors that haven’t checked in for 45 days

✔ Be aware of policy precedence when hosts belong to multiple groups

---
Module 7: Prevention policies
- Creating and managing prevention policies in CrowdStrike/EDR
- Understanding policy rules and configurations
- Best practices for policy management

<img width="1161" height="366" alt="Module 7 - Prevention policies" src="https://github.com/user-attachments/assets/ee77b356-db76-4730-a964-92cdaee76e45" />


✅ What makes up Preventions Policies
- Sensor visibilities
- NGAV (can slide the detection vs preventions settings from cautions -> extra aggressive)
- Malware protection
- Behavior and ML detections

✅ Preventions Policy Precedence
- Hostmay be assigned to more than one policy
- If no host assigned to a policy, it will drop to the last precedence policy=default
- Default=catch all policy

~~~
Make one:
endpoint security > prevention policy > create new > platform > name > create
- enable setting > save > confirm > enable > enable policy
- set the precedence order
~~~

✅ Default, Phase 1.2.3 Prevention Policies
- Phase 1 : Intended for customer setting up falcon for the first time
  - rapid deployment strategy, doesn't fully protect, should be used during initial deployment and alongside AV
  - should use for minimum time
- Phase 2 : Intended if you have no AV or EDR solution currently in place
  - a bit more protective in polocy settings
  - should use for 30 days
  - Start introducing IOA
- Phase 3 : The ideal standard level of protection for your hosts
  - Should try to get there in 90 days to ensure adequate protection of your endpoints     

Key Takeaways:

This module explains how **CrowdStrike prevention policies** work, how to configure them, and how to choose the right phase when rolling out Falcon to an environment.

**1. Big Picture: How Prevention Policies Work**

CrowdStrike uses a layered structure:

**1. Hosts → placed into Host Groups**

* Host groups can be **dynamic** (recommended) or **static**.

**2. Policies → created individually**

Examples of individual policy types:

* **Next-Gen AV policy**
* **IOA (Indicators of Attack) policy**
* **Firewall policy**
* **Sensor update policy**
* **Machine learning & behavior policies**
* **Sensor visibility settings**

Each of these is configured separately.

**3. Prevention Policy → bundle of all policies**

A **Prevention Policy** = a collection of multiple individual policies.

**4. Prevention Policy → assigned to Host Groups**

Host groups receive one assigned **prevention policy**, which determines all protection settings for that group.

**2. Detection vs. Prevention Sliders**

CrowdStrike uses **sliding scales** from:
**Cautious → Normal → Aggressive → Extra Aggressive**

**🚨 IMPORTANT RULE**

**Detection must always be set *higher* (more aggressive) than Prevention.**
Prevention should never exceed Detection.

Mnemonic: **Daring Hippos Prefer Lasagna**

* **D**etections = **Higher**
* **P**reventions = **Lower**

Why?

* Detection only *observes*
* Prevention *acts* (blocks/terminates)
* You cannot prevent more than you detect
* Preventing without detecting = irrational and unsafe

**3. Policy Precedence**

A host can belong to **multiple host groups**, and therefore multiple policies.

CrowdStrike resolves this using **Precedence**:

* The **lower the number**, the **higher the precedence**.
* The policy with the **highest precedence (rank 1)** wins.
* Host falls back to **Default Policy** if no other policy applies.

**Use the Default Policy as a “catch-all detector”**

If a host lands in the Default Policy:

* It means it did **not** match any dynamic/static group.
* This indicates something is wrong (filtering, group assignment, OS mismatch, etc.).

**4. Out-of-the-Box Prevention Policies**

CrowdStrike ships with:

1. **Default Policy** (catch-all)
2. **Phase 1**
3. **Phase 2**
4. **Phase 3** (optimal protection)

**Which phase should you apply during deployment?**

**If the environment already has an existing AV solution (McAfee, Symantec, etc.):**

➡️ Start with **Phase 1**

* Least aggressive
* Reduces false positives
* Avoids conflict with the existing AV
* Safer during coexistence

**If the environment does NOT have an AV currently installed:**

➡️ Start with **Phase 2**

* Provides moderate protection immediately
* No risk of conflicting with another AV
* Prevents leaving the environment exposed

**Phase 3**

* Final target for all hosts
* Most protection
* Should be reached **within 90 days** of deployment
* Tuned and stable environment required

**5. Recommended Rollout Strategy**

Falcon recommends a **tiered rollout** with tuning at each stage.

**General timeline (best practice):**

* **Days 0–30:** Phase 1
* **Days 30–60:** Phase 2
* **Days 60–90:** Phase 3 (optimal)

Adapt based on environment size:

* Small org (500 endpoints): accelerate
* Large org (10k–15k endpoints): move slower, follow 90-day structure

**Why gradual?**

* Prevent excessive false positives
* Tune detections & apply exclusions
* Avoid impacting business operations
* Handle conflicts with legacy AV tools

**6. Creating and Enabling a Prevention Policy**

Steps:

1. Go to **Endpoint Security → Prevention Policies**
2. Click **Create New**
3. Choose platform (Windows / macOS / Linux)
4. Name the policy
5. Configure all detection/prevention sliders and settings
6. **Save**
7. **Enable** the policy (not enabled by default)
8. Assign it to the appropriate host group
9. Adjust **precedence** if needed

**7. Administrator Best Practices**

✔ Understand the separation between **policies vs. prevention policies**
✔ Keep Detection sliders more aggressive than Prevention
✔ Use a tiered rollout to minimize false positives
✔ Monitor hosts landing in the **Default** policy
✔ Regularly tune exclusions and whitelist legitimate apps
✔ Move all hosts to **Phase 3** within 90 days
✔ Test everything on small pilot groups before broad rollout

**8. Mental Model Summary**

* **Host groups** decide *who* gets the policy
* **Policies** define *what* the rules are
* **Prevention policy** = bundle of all rules
* **Precedence** determines *which* one wins
* **Phase policies** control *how aggressive* the deployment is

---

Module 8: Custom IOAs & IOC Management
- Creating custom Indicators of Attack (IOAs) in CrowdStrike/EDR
- Understanding IOA rules and configurations
- Best practices for custom IOA management

✅ What are IOAs?
- Indicator of Attack
- Custom IOCs to implement into CS via gerex pattern matching
- Actions : Monitor, Detect, Block Executions, Kill Process (depends on what Rule Type you select)
- Rule Types : Process Creation, FIle Creation, Network Connection, Domain Name
- Endoint security > Configure > Custom IOA Rule Groups

<img width="1076" height="183" alt="Module 8 - Custom IOAs   IOC Management" src="https://github.com/user-attachments/assets/dd15757b-05bb-40cb-b350-94d601b8c62c" />

✅ Diffrent options based on OS
- Rule Types : Process Creation, FIle Creation, Network Connection, Domain Name

<img width="852" height="208" alt="Module 8 - Custom IOAs   IOC Management-2" src="https://github.com/user-attachments/assets/51deb131-141c-45bd-94ee-6cf9353bb6a0" />

✅ How they appear in Detections
- CustomIOA... Will be the prefix in the event name of the detection
- Can see what rules triggered the detection to fire

✅ Review of Regex and CS Gotchas
- .* still works for wildcards
- Need to escape \ just as usual
- Leave all unused fields as .*
- Always TEST the rule before implementing. Just because test pattern is correct doesn't mean it's the right regex for the job!

🔹 What we can do with IOAs:
- Block CIDR ranges of IPs
- Blocking IPs
- Blocking Domains
- File Names
- File Paths
- Parent, Grandparent file names
- Command Line Argument, Parent command lines

✅ IOC Management
- Keep in mind, these are all sensor based actions
- Can assign a severity to the detections (color codes can be set in preferences)
- Can put to a spesific host group, or all hosts
- Can add tags into IOC being implemented "Bad IP", "Adware", "IT Tool"

<img width="846" height="164" alt="Module 8 - Custom IOAs   IOC Management-3" src="https://github.com/user-attachments/assets/aee35591-32e0-4d1b-924d-21b7629fda56" />


✅ Icons!

<img width="1092" height="544" alt="Module 8 - Custom IOAs   IOC Management-4" src="https://github.com/user-attachments/assets/05b78b6f-3857-476a-ac05-739b34c2e6ef" />

Key Takeaways:

⭐ **1. IOA (Indicators of Attack)**

IOAs define *behavioral* patterns to detect or prevent malicious activity.
They rely on **regular expressions** for matching.

**What IOAs Can Match**

* File names
* File paths
* Process names
* Command-line arguments
* Parent process / grandparent process
* Domains / URLs
* IP addresses (Windows only)
* Network connections (Windows, macOS)

**Syntax**

* **IOAs use REGEX**
* **Exclusions use GLOB syntax**

  * Much simpler, no escaping slashes or spaces
* In IOAs, all unused fields must be `.*`

**Actions IOAs Can Take**

(depending on OS + rule type)

* Monitor
* Detect
* Block & Kill
* Block Execution

**IOA Rule Types**

| Rule Type          | Windows | macOS | Linux |
| ------------------ | ------- | ----- | ----- |
| Process Creation   | ✅       | ❌     | ❌     |
| File Creation      | ✅       | ❌     | ❌     |
| Network Connection | ✅       | ⚠️    | ❌     |
| Domain Name        | ✅       | ❌     | ❌     |

⭐ **2. IOA Workflow (Must Know)**

**Order matters!**

1. **Create IOA Rule Group**
2. **Add IOA rules (regex)**
3. **Enable each rule individually**
4. **Enable the rule group**
5. **Assign IOA group to a Prevention Policy**

> Then that **prevention policy** is assigned to a **host group**.

⭐ **3. Testing IOAs (Critical!)**

Bad regex can break production systems.

**Always test:**

* Use Investigate → Search to see what files/processes match your regex
* Use Console IOA tester (not fully reliable)
* Test on a small host group first

⭐ **4. Regex Gotchas**

* Use full and correct regex—escaping required

* Incorrect: `.*a.exe`

  * This matches too much (anything ending in “a”)

* Correct: `.*\\a\.exe`

* Escape:

  * Directory separators `\\`
  * Dots `\.`
  * Spaces `\s`

⭐ **5. What IOAs Are Useful For**

* Blocking malicious IPs (Windows only)
* Blocking malicious domains
* Blocking suspicious command-line patterns
* Blocking PowerShell behaviors
* Blocking specific file paths
* Blocking parent/child process combinations
* Detecting C2 infrastructure
* Creating custom detections for red-team simulations

⭐ **6. IOC Management**

Separate from IOAs (different menu entirely).

**Location:**
Endpoint Security → IOC Management

**You can upload:**

* IPs
* Hashes
* Domains

**Allows:**

* Bulk uploads
* Assigning to host groups
* Tagging (C2, malware family, campaign name, date, etc.)

**IOC Actions**

| IOC Type | Detect      | Block           | Allow     | Nothing |
| -------- | ----------- | --------------- | --------- | ------- |
| IP       | ✅           | ❌ (Detect only) | ❌         | ✅       |
| Hash     | ✅           | ✅               | Allowlist | ✅       |
| Domain   | Detect only | ❌               | ❌         | Yes     |

> **Important:** IP & Domain *blocking* must be done via **IOAs**, not IOC Management.

⭐ **7. IOC Limitations**

* IP blocking in IOC = detect-only
* Domain IOC = detect-only
* Endpoint-only enforcement → *not a replacement for firewall blocks*
* Always block malicious IPs/domains at the network perimeter too

⭐ **8. Overwatch & Detection Icons**

**Color severity scale**

* Blue → Informational
* Green → Low
* Yellow → Medium
* Orange → High
* Red → Critical

**Important Icons**

* **Green shield + check** → Process blocked
* **White/gray shield** → Process killed
* **Linked circles** → Part of an Incident
* **Falcon icon** → OverWatch detection (CrowdStrike threat hunters)

Each detection is mapped to a **MITRE ATT&CK tactic/technique**.

⭐ **9. Best Practices**

* Always test IOAs before rollout
* Use small pilot groups first
* Use tags to track history and context
* Use IOAs for advanced behavioral security
* Use IOC Management for indicators-based enrichment
* Double down with network-level controls (firewalls, IPS)

⭐ **One-Sentence Summary**

**IOAs = behavior-based custom detection & prevention using regex; IOC Management = static indicator tracking using detect/block/allow, with major limits on IP/domain blocking.**

---

Module 9: Exclusions and Quarantines
- Managing exclusions and quarantines in CrowdStrike/EDR
- Understanding exclusion and quarantine rules and configurations
- Best practices for exclusion and quarantine management

✅ What is an Exclusion?
- How to tune your console
- These are whitelisted, trusted processes, that you want to exclude from detections (preventions)
- Could be another AV or EDR solution to add exclusions for
- 4 Types :
  - Machine learning (file path) exclusion = manual or via detection page to create (GLOB syntax)
    - File paths
  - Machine learning (certificate) exclusion
  - Indicator of attack (IOA) exclusion = configured via the detection page only (regex)
    - behavioral exclusions that come up for False Positive Crowdstrike detections
  - Sensor visibility exclusion = completely ignored by the falcon sensor. Use with caution, or don't use at all
    - last resort option
    - sensor wont reallt log events, either
  - Exclusions will apply to ALL hosts or to specific Hosts Groups your select    

Ref: https://www.sonicwall.com/support/knowledge-base/crowdstrike-cs-exclusions/kA1VN0000000ITB0A2

✅ GLOB Patterns
- Uses matches found in detections to create the exclusion
- Assumes drive letters, so you don't need to add them
- Limit of 1 pattern per exclusion
- \*\ For one folder
- \** For recursive

🔹 How to add a ML Exclusion :
- In filter bar : triggering file: \<filename> and then group by hash, group by command line, etc and then copy it
- Go to endpoint > exclusion > ML exclusion > all hosts > next > paste in command line in exclusion pattern, click detection and preventions check box > create
  - ** always test the pattern
- Example for Malwarebytes : *\Program Data\Malwarebytes* *Program Files\Malwarebytes*

✅ Quarantined Files
- Need to enable it in the prevention policy
- Not available on the Linux platform, but should be soon
- Locally stored malware files will be stored on the host for 30 days, then deleted
  - Windows: \Windows\System32\drivers\CrowdStrike\Quarantine
  - MacOS : /Library/Application Support/CrowdStrike/Falcon/Quarantine

- When Downloading/Uploading a Quarantine File:
  - Password is infected, for a stop and pause moment to take note
  - 32mb is max suze to upload to the cloud-windows amd mac only
  - Local qurantine on a host=30 days
  - Cloud storage=90 days (90 days together max, not 120 days)

Key Takeaways:

✅ **CrowdStrike — Exclusions & Quarantine: Key Points**

⭐ 1. **What Exclusions Are**

Exclusions = **whitelisting** trusted files, processes, or paths so CrowdStrike does **not detect or block them**.

Used for:

* False positive tuning
* Allowing legitimate company-wide apps
* Allowing AV coexistence
* Preventing interference with IT tools (RMMs, backup tools, etc.)

Exclusions can apply:

* To **all hosts**
* Or **specific host groups**

⭐ 2. **Three Types of Exclusions**

**1. Machine Learning (ML) Exclusions**

* Use **GLOB syntax**
* Manual entry or created directly from detection page
* Most common type
* Used for whitelisting file paths, executables, etc.

**2. IOA Exclusions**

* Use **REGEX**
* Created only via detection page or Custom IOA section
* Behavioral allow-listing (e.g., allow certain PowerShell commands)

**Note:**
If added in **IOA section**, you're making a *block rule*;
If added in **Exclusions**, you're making an *allow rule*.

**3. Sensor Visibility Exclusions (Dangerous)**

⚠️ **Highest risk** – sensor will completely ignore the process/path.

* No detections
* No logs
* Full blind spot
* Use **only as last resort**
* Never exclude broad paths (e.g., `C:\Program Files\**`)

⭐ 3. **Glob Patterns (Used for ML Exclusions)**

Glob syntax = simpler than regex.

Key Rules:

* Assumes **drive letter automatically**
* One exclusion = **one pattern only**
* `*` = match within a directory
* `**` = recursive through subdirectories
* Doesn't cross directory separators
* Easier to whitelist software (e.g. RMM tools, AV products)

Example (whitelist Malwarebytes):

```
*/ProgramData/Malwarebytes/* 
```

⭐ 4. **How to Add an Exclusion (Workflow)**

1. From a detection → Get triggering file, hash, or command line
2. Copy the specific field
3. Go to
   **Endpoint Security → Exclusions → Machine Learning**
4. Choose scope (all hosts or specific groups)
5. Paste pattern
6. Check **“Detections and Preventions”**
7. Test pattern
8. Create

⭐ 5. **Why Testing Is Critical**

Improper exclusions can:

* Disable protection
* Hide real attacks
* Allow malware to run undetected

Always test Glob or Regex to ensure it only allows intended files.

⭐ 6. **Quarantine Files**

CrowdStrike can quarantine malicious files **locally + in cloud**.

**Requirements**

* Must be enabled in the prevention policy
* Must have the correct admin role
* **Not available for Linux** (as of the course)

**Locations**

**Windows:**
`C:\Windows\System32\drivers\CrowdStrike\Quarantine\`

**macOS:**
`/Library/Application Support/CrowdStrike/Falcon/Quarantine/`

**Retention**

| Location   | Duration                                         |
| ---------- | ------------------------------------------------ |
| Local host | 30 days                                          |
| Cloud      | Up to 90 days total (includes the 30 days local) |

Not 30 + 90 = 120; total lifecycle = 90 days max.

**Passwords**

* Downloaded quarantine ZIP password = **infected**

Purpose:
Makes you stop and think before opening potential malware.

**Upload Limit**

* Max upload size = **32 MB**

⭐ 7. **When to Use Which Exclusion Type**

| Need                                  | Use                                       |
| ------------------------------------- | ----------------------------------------- |
| Whitelist file paths                  | **ML exclusion (glob)**                   |
| Allow certain behavior                | **IOA exclusion (regex)**                 |
| Last-resort, hide activity completely | **Sensor Visibility (avoid if possible)** |
| AV coexistence                        | ML exclusions for AV folders              |

⭐ 8. **Best Practices**

* Use **specific**, not broad, glob patterns
* Avoid Sensor Visibility except for extreme edge cases
* Document exclusions and why they exist
* Test all patterns before rollout
* Apply to host groups when possible—not global
* Quarantine files should be reviewed quickly (risky to store)

📌 **One-Sentence Summary**

**Exclusions safely whitelist trusted files/processes (ML = glob, IOA = regex, Sensor Visibility = risky blind spots), while quarantine temporarily isolates suspicious files for up to 90 days total between host and cloud.**
