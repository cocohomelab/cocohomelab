## CrowdStrike: For SOC Analysts
Hailie Shaw, Blue Team Consulting

Module 1: Console Overview Get acquainted with the CrowdStrike console, your command center for proactive threat detection and incident response. Explore its interface, functionalities, and navigation to ensure a solid foundation for the rest of the course.

Module 2: Where to Spend Your Time Learn to prioritize effectively in a dynamic threat landscape. Understand the critical areas of focus within the CrowdStrike console to optimize your time and as it pertains to SOC work.

Module 3: Triaging a Detection Master the art of rapid detection triage. Develop skills to assess the severity of a detection, determine its scope, and decide on appropriate immediate actions.

Module 4: Useful Open Source Tools to Use Discover a curated toolkit of open-source resources that complement the CrowdStrike platform. Explore how to leverage these tools to enhance your threat intelligence and investigative capabilities.

Module 5: Event Search / CQL Delve into advanced event search techniques and learn how to craft powerful queries in CQL. Learn how to conduct host analysis and leveraging endpoint logs to your advantage.

Module 6: Real-Time Response Features Equip yourself with CrowdStrike's real-time response arsenal. Dive into containment strategies, remote actions, scripting, and other instant response capabilities.

Module 7: Sandbox & Blocking Actions Explore the CrowdStrike sandbox environment and understand its role in threat analysis. Learn to implement blocking actions effectively to halt threats in their tracks.

Module 8: Whitelisting / Exclusions Navigate the nuances of whitelisting and exclusions. Gain insights into striking the right balance between security and operational efficiency.

Module 9: Putting It All Together Immerse yourself in realistic scenarios where you'll apply your newfound knowledge. Walk through end-to-end incident response processes, from detection to resolution.

Module 10: Where to Go Next Chart your future course in the realm of cybersecurity. Discover avenues for continued learning, specialization, and skill refinement to stay ahead in the ever-evolving threat landscape.

### Notes

---

## Module 1 :

Key Takeaways :

### CrowdStrike for SOC Analysts – What This Course Covers (Why You Care)

### Purpose of the Course

* Designed **specifically for SOC analysts**
* Focuses on **hands-on detection triage, investigation, and response** in CrowdStrike Falcon
* Not a sales or admin-only overview — investigation-driven

### High-Level Course Structure (10 Modules)
### 1. Console Overview
* Learn **where things live** in the Falcon console
* Understand layout differences based on licensing
* Foundation for efficient navigation during incidents

### 2. Where SOC Analysts Should Spend Their Time

* Identifies:

  * Most-used pages for SOC work
  * Areas **you can ignore** unless you’re admin/engineering
* Helps reduce noise and speed up triage

### 3. Detection Triage (Start to Finish)

**Core SOC skill**

* How to:

  * Review detections
  * Understand severity, confidence, and context
  * Decide: benign, suspicious, or malicious
* End-to-end workflow for handling alerts properly

### 4. Open Source Tools for Research

* External tools to support:

  * File hash analysis
  * IP/domain reputation
  * Malware research
* Used **alongside CrowdStrike**, not replacing it

### 5. Next-Gen SIEM + LogScale

* CrowdStrike’s **Next-Gen SIEM**

  * Powered by **LogScale**
  * Uses **CrowdStrike Query Language (CQL)**
* Focus on:

  * Searching **endpoint telemetry**
  * Making sense of large log volumes
* Key for advanced investigations and threat hunting

### 6. Real Time Response (RTR)

* Remote interaction with hosts:

  * Run commands
  * Collect artifacts
  * Perform containment actions
* Critical for:

  * Live incident response
  * Validation and scoping

### 7. Sandbox & Malware Analysis

* Detonate suspicious files in:

  * CrowdStrike’s built-in sandbox
* Review:

  * Malware behavior
  * Indicators
  * Verdicts
* Apply **blocking actions** based on results

### 8. Whitelisting & Exclusions

* How to:

  * Add exclusions safely
  * Whitelist legitimate software
* Important for:

  * Reducing false positives
  * Avoiding overblocking business apps
* Emphasizes **controlled and documented use**

### 9. Putting It All Together

* Full detection walkthrough:

  * Uses concepts from modules 2–8
  * Mirrors real SOC workflows
* Reinforces:

  * Investigation logic
  * Decision-making
  * Response sequencing

### 10. Next Steps

* Guidance on:

  * Additional CrowdStrike features
  * Other courses beneficial for SOC growth
* Helps analysts continue skill progression

### This course focuses on:

* **Efficient alert triage**
* **Deep endpoint investigation**
* **Practical response actions**
* **Using CrowdStrike as a true EDR/XDR platform**, not just AV


## Module 2:

Key Takeaways :

### 1. User Profile & Preferences (Do This First)

**Critical for investigations and reporting**

* **Set Time Zone to UTC**

  * Go to **Top-right user icon → User Preferences**
  * Set display time to **UTC**
  * Choose a clear date format (Month/Date/Year or your org standard)
  * Why it matters:

    * All SOC reporting is in UTC
    * Avoid mistakes when building timelines or writing incident reports
    * Prevent manual time conversions from local time zones

* **Enable “Stay Signed In”**

  * Found under **Display → Stay Signed In**
  * Prevents frequent logouts (CrowdStrike normally times out after ~15–20 minutes)
  * Still may timeout after long inactivity, but far less often
  * Saves time during active investigations

* **Theme Selection (Light/Dark)**

  * Moon/Sun icon in top right
  * Choose what reduces eye strain during long SOC shifts
  * No functional impact, purely usability

### 2. Console Layout Depends on Your Subscription

**Important for expectations and access**

* What you see in the left-hand menu **depends on your CrowdStrike license**

  * Examples:

    * Falcon Free Trial
    * Pro
    * Enterprise (common in SOCs)
* **Greyed-out features = not licensed**

  * Not broken
  * Not misconfigured
  * Simply not paid for

### Key SOC Impact

* Even **Falcon Enterprise**:

  * Does **NOT** automatically include:

    * Identity Protection
    * Full Next-Gen SIEM
  * Advanced Event Search:

    * Only includes **endpoint logs**
    * Network, cloud, and server logs require **additional licensing**

### 3. Understanding Menu Indicators

* **Yellow or Blue dots on menu items**

  * Indicates:

    * New feature
    * Updated capability
  * CrowdStrike uses this to flag changes analysts should review

* **Expandable / Collapsible Submenus**

  * Use the arrows to expand menus
  * Easy to miss features if menus are collapsed
  * If you “can’t find something,” check submenu expansion first

### 4. SOC Workflow Optimization (Highly Recommended)

### Use Bookmarks Aggressively

Bookmarks are a **huge productivity boost** for SOC analysts.

* You can bookmark **any console page**
* Examples of high-value bookmarks:

  * **Endpoint Detections** (alerts queue)
  * **Investigate → Advanced Event Search**
  * **Host Timeline**
  * **Documentation pages**

    * Agent installation (Windows, macOS, Linux)
    * Agent uninstall procedures
    * Command-line install switches

**SOC benefit**

* One click straight into:

  * Alert review
  * Log searching
  * Troubleshooting
* Eliminates repetitive menu navigation during incidents

### 5. What SOC Analysts Should Care About Most

From this module, the **SOC-relevant priorities** are:

1. **UTC time setting** (non-negotiable for incident response)
2. **Stay signed in** (efficiency during investigations)
3. **Know your licensed features**

   * Avoid chasing missing functionality
4. **Understand menu indicators**

   * Stay aware of new detection or investigation features
5. **Bookmark investigation-heavy pages**

   * Alerts
   * Advanced Event Search
   * Documentation

### SOC Bottom Line

This module isn’t about detections yet—it’s about **setting yourself up to investigate efficiently, accurately, and without time confusion**. Get these basics right before touching alerts.


## Module 3:

Key Takeaways :

### Module 3 – Detection Triage (SOC Analyst Essentials)

### 1. Detection Dashboard Basics

**Detection retention**

* Detections: **90 days**
* Associated indicators (hash, IP, domain): **~1 year** (license-dependent)

**Filtering & visibility**

* Use **Add / Remove Filters** to narrow scope
* Column view:

  * Click any row to preview detection details
* **Group By** (very useful):

  * Command line
  * Host
  * Process
  * Username
  * Severity
    → Quickly understand **scope, impact, and false-positive patterns**

### 2. Detection Icons & Visual Cues (Read These Fast)

* **Falcon Black Shield** → CrowdStrike OverWatch detection (higher confidence)
* **Multiple hexagons** → Multiple detections / possible incident grouping
* **Green badge with check** → Process blocked
* **White shield with slash** → Process killed / operation blocked
* **MITRE icons inside detections** → Tactic/technique mapping
* **Color waves** → Severity (Critical → Informational)

👉 These visual indicators let you **prioritize within seconds**.

### 3. Detection Views (Same Data, Different Lenses)

All tabs show the **same data**, just visualized differently. Use what works best for you.

### Key Views:

* **Process Table**

  * Hierarchical: grandparent → parent → child
  * Shows full execution chain and command line
* **Process Tree**

  * Expand/collapse visual tree
  * Click processes/files for details
* **Process Graph**

  * Visual relationship view
* **Events Timeline**

  * Chronological, text-heavy
  * Best for fast, narrative-style review

📌 **Tip:** Be familiar with all views; switch depending on investigation style.

### 4. Where to Start Triage (Recommended Flow)

### Step 1: Open Full Detection View

* From detection row:

  * Right-hand panel → **Actions → Details View**
  * Or **See Full Detection**
* Full view provides **maximum context** (preferred for triage)

### Step 2: Investigate the Event

* Go to **Investigate → Investigate Event**
* Automatically:

  * Pulls agent ID
  * Filters on relevant process/target
* Opens **Advanced Event Search (endpoint logs)**

👉 This gives you a **head start** toward root cause analysis.

### 5. Key Triage Questions (Think in This Order)

These can usually be answered in **1–2 minutes** once experienced.

### Environment Context

* **Server or workstation?**

  * Workstations → easier to contain
  * Servers → high business risk, be cautious

### User Context

* Who ran it?

  * Domain admin?
  * Service account?
  * Standard user?
* Higher privilege = higher severity

### Alert Context

* Severity level?
* MITRE tactic/technique?
* OverWatch involved?
* Was anything blocked or killed?

### Threat State

* Is the process still running?
* Is malware active or already blocked?
* Any outbound network connections?

  * Beaconing / C2 = high priority containment

### Process & Execution

* Suspicious command lines?
* Abnormal parent-child relationships?

  * Word → cmd
  * Unusual paths (not System32)
* Unexpected execution locations?

### Intelligence & IOCs

* Known bad hash/IP/domain?
* Mapped to known threat actor?
* Any related activity elsewhere in environment?

### External Validation

* Hash/domain/IP lookups (OSINT)
* Sandbox results (if available)

### 6. Grouping Detections for Faster Insight

Use **Group By** to:

* See how many hosts are affected
* Identify repeat false positives
* Prioritize critical vs informational alerts
* Spot common command lines or processes

### 7. Actions After Triage

Depending on outcome:

* **False positive**

  * Plan exclusions (covered later)
* **True positive**

  * Block hash/IP/domain
  * Create custom IOA
  * Consider host containment
* **Uncertain**

  * Escalate with notes and recommendations

### 8. What to Document in Detection Notes (SOC Standard)

### Minimum Required

* Hostname
* OS (Server/Workstation, version)
* **UTC timestamps**
* Processes & command lines
* Summary of activity
* Actions taken

### Strong Additions

* OSINT links (hash/IP/domain research)
* Sandbox report links
* MITRE mapping
* Root Cause Analysis (if possible)
* Scoping:

  * Single host vs environment-wide
* Recommendations:

  * Block / exclude
  * Further investigation steps

📌 Especially important for **Tier 1 → Tier 2 handoff**

### 9. Skill Progression Reality

* Early on: triage takes longer
* With experience:

  * Malicious activity becomes **obvious and loud**
  * OverWatch detections often stand out
* Goal:

  * Quickly decide:

    * **Immediate escalation**
    * **Deep dive**
    * **Benign / tune**

### SOC Analyst Bottom Line

Module 3 teaches you how to:

* Read CrowdStrike detections **efficiently**
* Identify **true positives vs false positives**
* Use visual cues and logs to reach **fast, defensible decisions**
* Document investigations in a way that **supports escalation and reporting**

## Module 4:

Key Takeaways :

## Module 4 – Open Source Intelligence (OSINT) for SOC Analysts

**Goal:** Use free, industry-standard tools to enrich CrowdStrike detections and support investigation, triage, and ticketing.

## 1. Core Message for SOC Analysts

* The **methodology matters more than the tool**
  Skills learned here apply to **CrowdStrike, SentinelOne, Carbon Black, etc.**
* These tools are **essential for Tier 1 / Tier 2 analysts**
* OSINT enrichment strengthens:

  * Detection validation
  * Root cause analysis (RCA)
  * Confidence in escalation or closure
  * Ticket quality and documentation

## 2. Must-Know OSINT Tools (High Value)

### VirusTotal

**Use for:**

* Hashes, IPs, domains, URLs, filenames
* Community detections and comments
* Relationships between indicators
* Existing sandbox reports

**SOC Tip:**

* Look at **relationships and behavior**, not just AV scores
* Use VT links inside CrowdStrike detections when available

### ANY.RUN (Sandbox)

**Use for:**

* Executing suspicious files safely
* Observing:

  * Process spawning
  * Network connections
  * Registry changes
  * Dropped files

**Why it matters:**

* Teaches you **how malware behaves**
* Builds intuition for:

  * Parent/child process trees
  * Post-execution indicators
* Affordable and SOC-friendly

### Joe Sandbox

**Use for:**

* Reviewing detailed sandbox reports
* Often accessible via VirusTotal

**SOC Tip:**

* Even if *you* didn’t detonate it, **review existing reports**
* Same hash = valid behavioral insight

### Hybrid Analysis

**Use for:**

* Hash, URL, and file behavior analysis
* Correlating multiple detections

### Scan.io / URL & Domain Tools

**Use for:**

* Domain reputation
* Passive DNS
* WHOIS lookups

⚠️ **Never directly visit malicious domains**

### Shodan

**Use for:**

* IP reputation
* Open ports and exposed services
* Certificates and misconfigurations

### MXToolbox

**Use for:**

* Email header analysis
* Phishing investigations

## 3. Google (Used Safely)

**What to Google:**

* Process names
* DLLs and executables
* Command-line switches
* Legitimate file locations

⚠️ **What NOT to Google directly:**

* Malicious domains
* IPs or URLs (risk of accidental navigation)

**Rule of Thumb:**

> Google *what something is*, not *where it lives online*

## 4. CrowdStrike + OSINT Workflow

From a CrowdStrike detection:

1. Identify the **triggering indicator**
2. Pivot to:

   * VirusTotal
   * Hybrid Analysis
   * Sandbox execution
3. Extract:

   * Additional hashes
   * Network indicators
   * Persistence mechanisms
4. Use findings to:

   * Search your environment
   * Recommend blocks
   * Support RCA in the ticket

## 5. Gold-Standard Reference Resources

### SANS – “Find Evil / Know Normal” Poster (Windows)

**Why it’s critical:**

* Defines:

  * Common Windows executables
  * Expected file paths
  * Normal instance counts

**Examples of instant red flags:**

* `lsass.exe` outside `System32`
* `svchost.exe` in user directories
* Multiple copies of system binaries

🎯 **SOC Value:**
Knowing *what’s normal* lets you spot *what’s malicious* instantly.

### Linux Resource – Sandfly Security

**Use for:**

* Linux compromise assessment
* Detection commands
* Files and logs of interest

**Reality check:**

* Most SOC analysts are Windows-strong, Linux-weaker
* This is a **practical cheat sheet**, not deep forensics

## 6. Key Analyst Habits to Build

* You will **never memorize everything**
* Googling is normal—even for senior analysts
* Always:

  * Validate file location
  * Validate execution context
  * Correlate multiple data sources
* **Document your findings** in tickets:

  * Why it’s malicious
  * What evidence supports it
  * What indicators were validated

## Bottom Line for SOC Analysts

* OSINT tools **turn alerts into answers**
* They make your investigations:

  * Faster
  * Defensible
  * Easier to escalate or close
* These skills directly translate to:

  * Tier 1 → Tier 2 growth
  * CrowdStrike certification readiness
  * Real-world SOC performance

## Module 5:

Key Takeaways :

## Module 5 – Raw Endpoint Log Searching (CrowdStrike KQL)

**Goal:** Investigate endpoint activity using CrowdStrike’s **Advanced Event Search** with the new **KQL (Next-Gen SIEM Query Language)**.

## 1. What Changed (Why This Matters)

* CrowdStrike moved from **Splunk backend → Next-Gen SIEM with KQL**
* Advanced Event Search now:

  * Is **faster**
  * Uses a **new query language**
  * Shows **raw endpoint telemetry**
* This is **endpoint logs only** (not full SIEM unless subscribed)
* Logs primarily cover **active processes that generated events**

🎯 **SOC Impact:**
This is where you live during investigations.

## 2. Where Analysts Spend Their Time

**Path:**
`Next-Gen SIEM → Advanced Event Search`

Key UI elements:

* Field selector (left panel)
* Timeline + event volume graph
* Time range selector (Splunk-like)
* Results in **key:value pairs**

## 3. Critical Fields Every SOC Analyst Should Know

### `event_simpleName`

**Tells you WHAT happened**
Examples:

* Process start / end
* File write
* Network connection
* DNS request
* Scheduled task creation
* User logon / logoff

📌 **Almost always include this in tables**

### Raw Fields (prefixed with `@`)

Most important:

#### `@timestamp`

* Raw event time
* **Linux Epoch format**
* Must be converted for reporting

#### `@rawstring`

* **Entire raw endpoint event**
* Contains ALL captured fields
* Always include for:

  * Validation
  * Future reference
  * Missed field recovery

🧠 **Rule:**
If you export data, **always include `@rawstring`**.

## 4. Commonly Used Investigation Fields

* Command line
* File name / file path
* Image file name
* Target image file name
* Hashes
* Username
* Domain
* IP / port data

💡 Tip:
Type partial field names (e.g., `ip`) to discover available fields.

## 5. Understanding File Paths

CrowdStrike uses paths like:

```
\Device\HarddiskVolume3\Windows\System32\cmd.exe
```

🔄 **Convert mentally to:**

```
C:\Windows\System32\cmd.exe
```

Just replace:

* `Device\HarddiskVolumeX` → drive letter

## 6. Searching Basics (Fast Wins)

### String / Wildcard Search

```
/string_to_search/i
```

* Forward slashes = string match
* `i` = case insensitive

✅ Use this constantly to:

* Find program names
* Find commands
* Find artifacts without exact field names

### Host-Scoped Searching

Always scope first:

* `agent_id = <ID>`
  **or**
* `computer_name = <hostname>`

🎯 Prevents noisy results.

## 7. Time Handling (Non-Negotiable Skill)

* `@timestamp` is **epoch**
* Convert to:

  * Human readable
  * **UTC (Zulu)**

Why UTC?

* No regional confusion
* Standard SOC reporting
* Clean timelines

📌 **Always include timestamp conversion in base searches**

## 8. Repeatable Base Search (Best Practice)

### Base Search Concept

* **Red = stays the same**
* **Green = variables you change**

Always include:

1. Host identifier (agent ID or computer name)
2. Timestamp conversion to UTC
3. Event filter (string or `event_simpleName`)
4. Table of relevant fields

Only change:

* Event type
* String filter
* Output fields

🎯 **This is how you scale investigations quickly**

## 9. Common Investigation Examples

### Command History

* Filter: `event_simpleName = CommandHistory`
* Fields:

  * Command line
  * Username
  * Process info

### Scheduled Task Creation

* Filter: `event_simpleName = ScheduledTaskCreated`
* Fields:

  * Task name
  * Task author
  * Executable
  * Arguments

## 10. Group By & Stacking Analysis

### Why Group By?

* Identify:

  * What’s most common
  * What’s rare (often malicious)

### Network Example

* Filter: `NetworkConnect`
* Group by:

  * `RemoteAddressIP4`
* Count
* Sort descending
* Limit results

Use cases:

* Beaconing
* Unexpected outbound IPs
* Port abuse (22, 80, 3389)

### Authentication Example

Group by:

* Computer name
* Username
* Logon type
* Local IP
* Remote IP

💡 Add filters like:

* `logon_type = 10` (RDP)

### DNS Example

* String search: `/rclone/i`
* Group by: domain name

Quickly highlights:

* Data exfil tools
* Cloud abuse
* Malware infrastructure

## 11. Exporting Data (When You Don’t Want KQL)

### Export Workflow

1. Build search
2. Include:

   * UTC timestamp
   * All fields of interest
3. Run search
4. Save → Export

Formats:

* CSV (most common)
* JSON
* NDJSON
* Plain text

⚠️ CSV only includes fields in your `table` statement.


### Excel-Based Analysis

* Filter
* Sort
* Stack
* Build timelines

🧠 **Real-world SOC workflow:**

* Multiple CSVs per host:

  * Network activity
  * Logons
  * Process execution
  * Command history

This is normal and effective.

## 12. SOC Reality Check

* You don’t have to choose:

  * **KQL OR CSV**
* Strong analysts use:

  * KQL for fast filtering
  * CSV/Excel for deep review

🎯 Best analysts are **tool-agnostic and flexible**

## Bottom Line for SOC Analysts

* Advanced Event Search is **core investigation tooling**
* Learn:

  * Base searches
  * Time conversion
  * Group by analysis
* Always:

  * Scope to host
  * Normalize time (UTC)
  * Export when needed
* This directly improves:

  * Speed
  * Accuracy
  * Timeline reconstruction
  * Escalation quality

## Module 6:

Key Takeaways :

## Module 6 – Real Time Response (RTR)

**Goal:** Perform live, remote endpoint investigation and response **without user awareness**, directly from the CrowdStrike console.


## 1. What RTR Is (SOC Reality)

* RTR = **Live remote shell** on the endpoint
* No user notification or visibility
* You are effectively “on the box” remotely
* Works for:

  * Windows
  * Linux

🎯 **Primary SOC Use Cases**

* Triage suspicious activity
* Collect artifacts
* Kill malicious processes
* Pull malware samples
* Validate detections
* Support containment & remediation

## 2. Command Environment Basics

* **Linux-style command interface** for *all* hosts
* Even on Windows:

  * Default commands are Linux-like
  * PowerShell commands/scripts still work

📌 **Key Difference**

* Windows:

  * Use PowerShell syntax in scripts
* Linux:

  * Use bash-style scripts

## 3. RTR Tabs (Critical Distinction)

### Tab 1: Run Commands

**What it is:**

* Limited to **~25 pre-built CrowdStrike commands**
* Only supported switches allowed

**Use cases:**

* Quick, safe actions
* Standardized operations

Examples:

* `ls`
* `cd`
* `cat`
* `file_hash`
* `netstat`
* `ps`
* `kill`
* `put`
* `get`
* `run`
* `help`

⚠️ You **cannot** run arbitrary commands here.

### Tab 2: Edit & Run Scripts (Most Powerful)

**What it is:**

* **No real limitation** (besides size/file constraints)
* Run:

  * Full PowerShell scripts
  * Bash scripts
  * Custom enumeration

**SOC Value:**

* Full host inspection
* Custom tooling
* Advanced triage

🧠 **Anything you can do in PowerShell → you can do here**

## 4. Side Menu (Often Forgotten, Very Important)

Expand it during RTR sessions.

Provides:

* Host type (server vs workstation)
* First seen / last seen
* Sensor version
* Deployment group
* Agent ID
* IP & MAC
* OS details
* Recent detections

🎯 **Use this to quickly understand the host context**

## 5. Script Repository (Tier 2 / Tier 3 Useful)

* Upload scripts to CrowdStrike console
* Stored centrally
* Select and run during RTR sessions
* Equivalent to:

  * Upload → execute

Useful for:

* Standard triage scripts
* Host enumeration
* IR automation

## 6. Host Status & Network Containment

### Host Must Be:

* Powered on
* Connected to CrowdStrike cloud

### Network Contained Hosts:

* Still allow:

  * Communication to CrowdStrike
  * RTR sessions

🎯 **Critical SOC Insight**

> You can still investigate a network-contained host via RTR.

## 7. Default Commands SOC Analysts Should Know

| Command     | Purpose                 |
| ----------- | ----------------------- |
| `help`      | List available commands |
| `ls`        | List directory contents |
| `cd`        | Change directory        |
| `mkdir`     | Create directory        |
| `cat`       | View file contents      |
| `ps`        | Running processes       |
| `netstat`   | Network connections     |
| `kill`      | Terminate process       |
| `file_hash` | Hash a file             |
| `put`       | Upload file             |
| `get`       | Download file           |
| `run`       | Execute file/script     |

📌 No tab-completion → type carefully
📌 Use **double quotes** for paths with spaces


## 8. File Collection & Malware Handling

### When Using `get`:

* Files are:

  * **Zipped**
  * **Password protected**
* Default password:
  **`infected`**

🎯 **Why this matters**

* Prevents accidental execution
* Proper malware handling practice

### File Size Limitations

* Windows / Linux:

  * ~2–4 GB max
* Large files may:

  * Be double-zipped
  * Restart compression automatically

📌 Double-zip behavior is normal

## 9. PowerShell vs Default Commands

Example:

* Default command:

  * `file_hash`
* PowerShell equivalent:

  * `Get-FileHash`

👉 Either works, depending on the tab used.

## 10. Analyst Productivity Tips

* Use:

  * Google
  * ChatGPT
* For:

  * PowerShell syntax
  * Script templates
  * Command references

⚠️ **Key Reminder**

> Tools don’t replace analysis — they enable it.

You’re paid to:

* Know **what** to collect
* Know **why** it matters
* Interpret results correctly

## 11. How to Launch an RTR Session

### 3 Ways:

1. **Event Actions**

   * From raw event logs → “Connect to Host”
2. **Incident Page**

   * Ellipses → “Connect to Host”
3. **Detection Page**

   * Click “Connect to Host”

📌 Host must be online.

## Bottom Line for SOC Analysts

* RTR is **one of the most powerful tools in CrowdStrike**
* Learn:

  * Default commands
  * Script execution
  * Safe file handling
* RTR enables:

  * Deep triage
  * Malware collection
  * Live validation
  * Effective containment follow-through

## Module 7:

Key Takeaways :





Module 8:

Key Takeaways :

Module 9:

Key Takeaways :

Module 10:

Key Takeaways :
