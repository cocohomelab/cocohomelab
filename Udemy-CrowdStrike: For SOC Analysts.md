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

Module 1:

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


Module 2:

Key Takeaways :

## 1. User Profile & Preferences (Do This First)

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

## 2. Console Layout Depends on Your Subscription

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

## 3. Understanding Menu Indicators

* **Yellow or Blue dots on menu items**

  * Indicates:

    * New feature
    * Updated capability
  * CrowdStrike uses this to flag changes analysts should review

* **Expandable / Collapsible Submenus**

  * Use the arrows to expand menus
  * Easy to miss features if menus are collapsed
  * If you “can’t find something,” check submenu expansion first

## 4. SOC Workflow Optimization (Highly Recommended)

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

## 5. What SOC Analysts Should Care About Most

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


Module 3:

Key Takeaways :

Module 4:

Key Takeaways :

Module 5:

Key Takeaways :

Module 6:

Key Takeaways :

Module 7:

Key Takeaways :

Module 8:

Key Takeaways :

Module 9:

Key Takeaways :

Module 10:

Key Takeaways :
