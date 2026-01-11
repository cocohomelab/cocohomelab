### `What Information is Sensitive Information ?`

In **DLP (Data Loss Prevention)**, **Sensitive Information** means data that could cause harm to an individual or an organization if it is **exposed, stolen, altered, or misused**. DLP systems are designed to detect and protect this kind of data.

### Common Types of Sensitive Information

#### 1. **Personal Identifiable Information (PII)**

Information that can identify a person:

* Full name (with other identifiers)
* Home address
* Phone number
* Email address
* Date of birth
* National ID numbers

#### 2. **Financial Information**

Data related to money or payments:

* Credit/debit card numbers
* Bank account numbers
* IBAN, routing numbers
* Transaction records

#### 3. **Authentication & Security Data**

Information used to access systems:

* Passwords
* PINs
* Security questions/answers
* Encryption keys
* API keys, access tokens

#### 4. **Health Information (PHI)**

Medical or health-related data:

* Medical records
* Diagnosis details
* Prescription information
* Health insurance numbers

#### 5. **Corporate / Confidential Business Data**

Organization-specific sensitive data:

* Trade secrets
* Source code
* Internal emails
* Business plans
* Contracts
* Pricing strategies

#### 6. **Intellectual Property (IP)**

Creative or proprietary work:

* Designs
* Research data
* Patents (before public release)
* Algorithms

#### 7. **Regulated Data**

Data protected by laws or regulations:

* GDPR (EU personal data)
* HIPAA (US health data)
* PCI-DSS (payment card data)
* FERPA (student records)

### Why DLP Cares About Sensitive Information

DLP tools help to:

* Prevent data leaks (email, USB, cloud, web uploads)
* Enforce compliance with laws and policies
* Reduce insider threats and human error


Endpoint DLP
- Monitors all network endpoints — including servers, cloud repositories, computers, mobile devices, and more — to prevent data loss or misuse
- Facilitates classification of sensitive data, streamlining compliance reporting
- Tracks data stored on devices, even those that are off-network


Endpoint DLP

`“Protect where people actually work”`
- Endpoint DLP (USB, copy/paste, print, screenshots)
- Basic data classification and labeling
- Better coverage for remote work

Data-Centric Endpoint DLP

`“Protection follows the file”`
- Automatic data classification on endpoints
- Sensitivity labels persist when files are:
  - Copied
  - Uploaded
  - Shared
- Encryption or access control enforced locally

Behavior-Based Endpoint DLP

`“Detect risky behavior, not just actions”`
- UEBA on endpoint activity
- Flags anomalies such as:
  - Mass file access
  - Unusual copy patterns
  - Off-hours data movement

- File Access Anomalies
  - Mass file access across multiple folders or shares
  - Rapid open/read of sensitive files without edits
  - Accessing files unrelated to user’s role or project
  - Repeated access to archived or rarely used data
  - Sudden spike in file access volume compared to baseline

- Copy / Exfiltration Behavior
  - Large-scale copy to:
    - USB devices
    - External drives
    - Network shares
  - Repeated copy/paste actions in short timeframes
  - Copying sensitive data into:
    - Personal apps (WhatsApp, personal email, browsers)
    - Unsanctioned tools
  - Clipboard usage across different apps unusually fast

- Time-Based Anomalies
  - Off-hours data movement (late night / weekends)
  - Data access immediately before:
    - Resignation notice
    - Account deactivation
  - Sudden activity after long periods of inactivity

- Application Behavior Anomalies
  - Sensitive data opened in unusual applications
  - Switching between multiple apps to move data quickly
  - Use of compression tools (ZIP/RAR) on sensitive files
  - Screenshot or screen-capture bursts

- Device & Environment Signals
  - Data movement from a new or rarely used device
  - Activity from unmanaged or downgraded security posture devices
  - Sudden VPN disconnect followed by data access
  - Change in OS security controls prior to data movement

- User Intent & Risk Indicators
  - Attempts to bypass controls (renaming files, changing extensions)
  - Repeated policy violations after warnings
  - Just-in-time risky behavior aligned with job change signals
  - Combination of low-risk events forming high-risk patterns

---

Use Case
- Mapping DLP alerts to MITRE ATT&CK


How DLPe trigger
- DLP will trigger the rule only when the classification criteria is met.




Baseline vs Mature DLP

Baseline DLP is about visibility and learning. Mature DLP is about precision enforcement and risk reduction. The transition between the two is driven by policy tuning, user behavior understanding, and business alignment.”
