CrowdStrike: Zero to Falcon Admin

Description

Master the Falcon Platform from an Administrative Perspective

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
---
Notes:

Module 1: What is CrowdStrike/EDR
- Introduction to CrowdStrike/EDR
- Understanding Endpoint Detection and Response (EDR)
- Key features and benefits of CrowdStrike/EDR

🛡 What is an EDR tool?
- Endpoint detection And response.

Extra Notes:
- This is something that's pretty much it's going to be an agent.
- So an MSI, an X that's going to be deployed out to all of your endpoints, whether those are servers or workstations.
- And that agent is going to focus on detecting and responding to the security threats on those endpoints.
- A couple of different techniques that it will use to be able to detect.
- First we have the signature based detections.
- These are basically matching on a signature a known pattern that has fired and it's already been pre-written for the signature.
- It's very static.
- So if we want to make a note.
- We can kind of have our first type here.
- Be signature based, and we'll say static is associated to that.
- The second type of detection that you can have is behavioral.
- Behavioral is going to say more of a dynamic approach.
- So if we have static for signature, dynamic for behavioral this is going to detect on maybe behaviors associated with parent child relationships.
- For anomalous behaviors occurring on files or processes. Or an example would be if PowerShell spawn command line which spawned malware. Exe it's going to be looking out for different behaviors that say, you know, this isn't really matching on a signature like a static detection would, but it's going to be an odd behavior that we wouldn't expect to be legitimate and could potentially be malicious in your environment.
- And the tool will flag on the behavioral based detection.
- There is also a third type of detection.
- Heuristics.
- If you have a heuristic type detection, this is where the EDR tool will spend some time to learn the baseline of your environment for what's normal.
- It will take an encompass signature based and behavioral based detections and general activity occurring on your endpoints.
- To say this is occurring pretty frequently, so it's probably normal.
= And if there is an activity that occurs that's way outside the norm, it will make a heuristic based detection to say, I think this activity is highly anomalous based on what I've learned so far in your environment over, you know, three months plus of learning the baseline and it will fire a detection for you.
- You may hear EDR, also referred to as XDR.
- It's kind of like the new hip way of calling out EDR tools.
- And it's just saying that it has X feature of whatever kind of feature you're looking for within that tool, kind of going outside of just the standard endpoint detection and response outside of just the endpoint.
- Now we have a bunch of features that can help you additionally, with threat intelligence, Active Directory enumeration, vulnerability assessments, pretty much a whole XDR approach, instead of just detecting and responding to security threats based on signature behavioral or heuristic based detections, EDR can also leverage machine learning and AI to improve accuracy and efficiency.
- It provides real time monitoring.
- We'll put a little star next to that and detection of potential threats, real time monitoring.
- I put a star next to it because it's going to be as close as possible to real time monitoring as it can get.
- Sometimes the activity still occurs and your detection didn't block it, but it did give you an alert.
- But it is only real time monitoring for as close as the detections are scheduled or set to check or scan your environment for those detections.
- But sure, we'll say real time monitoring and you can also initiate automated responses to detected threats.
- And it will provide detailed logs and forensics for further investigation and prevention.
- We'll definitely see that in CrowdStrike as something that stands out.
- But overall, an EDR tool, some competitors in the market.
- CrowdStrike.
- Carbon black.
- Sentinel one.
- Huntress.
- All big players in the field of EDR tools.
- And definitely some of the market leaders, I would say are these three right here.
- So you're definitely on the right course to learn and master the CrowdStrike EDR tool.
- Now what makes CrowdStrike stand out?
- Definitely had to throw in this meme from the guys over at Red Canary.
- EDR actually stands for Expensive Data Recorder.
- Basically, just recording all of your events and doesn't actually block it.
- We still need analysts out there and administrators out there to make sure that you're checking into the console, the EDR tool every day to to respond and evaluate the detections and alerts that are showing up.
- But CrowdStrike, it has so many features.
- It really is the definition of a true XDR platform.
- There's so many new modules and additions that they're constantly making to the console, all to make it better and really increase the security posture of your organization.
- And it's becoming also very flexible with deployment options.
- Obviously, it supports multiple operating systems.
- What we'll talk about later on has an extremely.
- Friendly user interface.
- If you're coming from a Splunk background, you're going to be able to pick up CrowdStrike pretty quickly as the query language for when your threat hunting will be based off of SPL, and all of the dashboards and widgets that are kind of built into CrowdStrike throughout the console leverage Splunk dashboarding familiarity, and they're running on Splunk searches, so it will look very familiar to you off the bat has a very strong customer support.
- If you're a client of CrowdStrike, you have 24 access to their support portal to reach out to the CrowdStrike engineers.
- Anyone that you would need, open your support case and they have great turnaround time.
- And again, we've also talked about additional features within the console for vulnerability analysis threat Intel. Add enumeration.
- They have modules in there for assessing your cloud environment.
- They have a sandbox.
- Environment to run sample malware within there, and just a really great tool overall.
- Definitely one that falls under XDR and more consoles than more features within the console that I could probably ever list out.
- But I'm also not a sales engineer for CrowdStrike, but I definitely love the tool, and it's definitely something that stands out.


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
