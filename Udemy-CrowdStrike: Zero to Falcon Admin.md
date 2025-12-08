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

### Notes:
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

Extra Notes :
- We're talking about permissions roles capabilities for our users.
- So when we think about roles in I.T.
- Cybersecurity, we think of permissions.
- In CrowdStrike.
- They bundle up all of their permissions.
- So if you can do X, Y, or Z into.
- A rule, then you assign multiple roles to Your users.
- That is how you manage permissions within CrowdStrike.
- There's, I don't know, maybe 25 roles or so within the console.
- And these are going to be assigned and administered controlled provisioned new users by the Falcon admin.
- That's going to be you.
- So you don't want to over.
- Provision a new user with giving them too many roles that are outside of their assigned job duties or the functions that they need to take within the console.
- Because we want to think of a security mindset when we go through administrating the CrowdStrike console and state that we don't want to have a user be overprivileged with an environment because if a threat actor A to ever comes in to the environment and they have compromised a user that is overprivileged, this is the terrible attempt at a crown.
- I'm drawing on a user for someone having the King account or a God like account, because you've given them all 25 roles available within the console.
- Now that threat actor is going to have godlike privileges within your CrowdStrike or your console,and you can assume how that will be absolutely devastating.
- So we don't want to do that.
- And when you're administrating new users, just keep in mind what role would be applicable to give them based on their job function and then leave it at that.
- We're going to go over roles in the demonstration.
- One important note that we will get to as well is.
- The consideration around the real time response.
- We're going to call that RTR From now on, this is pretty much where you drop into a live show onto an end point.
- These there's only three of them.
- And even if you are a Falcon administrator, you are not given any capabilities to remote into a host via RTR.
- Off the bat, you need to be assigned one of the three rtr RTR roles to your account in order to be able to drop in.
- So just keep that in mind.
- It's a very important thing to note going down the list here.
- Since this is in blue, it must be important.
- So we have an associated domain email with your account that has to match the customer ID association with your console.
- So what does this mean?
- If my console that we'll see in the demonstration.
- My email domain for my business is blue team wins dot com.
- So my username is H Shaw at blue team wins dot com.
- That means I cannot add my gmail, my Yahoo or any other email domain that is not matching the business email domain that I registered when I became a crowdstrike client to the console.
- The email domain is going to be associated to your customer ID and you cannot add any other emails into your CrowdStrike console unless the email domain matches, you can open up a support ticket and ask for a one off with the team over at CrowdStrike to say, Hey, can you just add this Gmail account in?
- I wish you the best of luck.
- I think they will deny that based off of their security standards that they set and they really don't allow just generic emails to be added to the console.
- It needs to be a business email.
- So just wanted to make you aware of that.
- Some of the top roles we have here, Falcon Admin, as we mentioned, doesn't come with RTR off the bat and it also doesn't come with the custom IOA.
- IOA is indicator of attack.
- Those are going to be your custom detections that you can write.
- So if you want to perform any of those actions eaos or being able to drop into a shell onto a host, you need to assign the roles to yourself as a falcon admin or where it makes sense to the user who's going to be performing these functions as part of their job duty.
- We have a prevention policy Admin Falcon Console Guest, a Dashboard Admin Desktop Support
- Analyst Workflow
- Author help Desk analysts.
- There is again just so many roles within the console.
- We're going to show how to get a quick overview of what that role does before you sign it to a user when we see it in the console.
- So you don't have to memorize any of these, they're all available and well documented within the CrowdStrike documents.
- But the big things to keep in mind is really the Falcon administrator will provision users with the roles your business email domain can only be added to your console, and the Falcon admin role does not come preconfigured with custom EOA or RTR capabilities.
- Okay, let's dive in a little bit deeper on the RTR roles.
- As I mentioned, there are only three read, only analyst, active responder and administrator.
- So the read only analyst you basically got read only.
- Sorry, but nobody trusts you with any capabilities at all within the console and your read only.
- But I guess the flip side of that is you can't really do any damage because you got read only.
- So you can you can't do any custom scripts, you can't do any put actions.
- You pretty much can just look at files, look at logs, look at alerts, but you can't close any of the alerts.
- You can't triage or make comments.
- You can just look and observe.
- So you get the smiley face as you are probably green stick in the environment.
- But over time, hopefully you get promoted to at least the active responder where you can start using the get command and some custom scripts.
- So this doesn't say custom scripts, it says some custom scripts.
- So the responder is a little bit better then reader as you can do some additional commands.
- When you're on a shell for a host and you can run some custom scripts.
- But if you want to be able to run any custom script, you're going to need to be the RTR administrator.
- The admin can run all the commands within their.
- Think there's about 15 preconfigured commands that you can run on the shell, but you really don't need to know this number because you can create any custom script leveraging PowerShell and add that script to the console and then run that script on the endpoint.
- And there is no limit to what PowerShell command you can put into a script.
- All are fair game.
- So really no limitation for any kind of action you can take in RTR, at least not one that, I've come across yet.
- And the ability to upload files, download files, run commands, admin is going to be able to do anything and not run into any permission issues at all.
- Let's say you had a new user who you want to be able to view files on a host but not be able to pull any off.
- Which role would that fall under?
- That would be the read only analyst.
- So let's keep the RTR roles in mind.
- Again, if you're a Falcon admin as your role and you notice you can't connect to a remote host, that is because you do not have one of these three roles assigned to you.
- OC How to add a New user.
- Our favorite thing to do is provision users and add people to the console.
- Because we are administrators, we're going to go to host setup Falcon users and user management.
- Here you're going to be able to click the three dot ellipses on the side or the create user.
- Button that will be there and it will walk you through all the steps to fill out their first name, last name, their email.
- And of course, as we mentioned, that email needs to be associated to the business domain email that's registered with the side of the console, the customer ID.
- Keep that in mind.And.
- The rolls.
- This is where you can assign the roles that you're going to give that new user.
- Now, after you create the user, there's a couple of actions you can do.
- If you go back into the user management, let's say that we now have the user, Haley at Blue Team Consulting. Dot com.
- Well, if we click on the ellipsis, it'll bring up the details and we can do all of the following actions in there.
- You can reset the users MFA or to two factor authentication.
- You can choose the option to reset a password, you can delete the user, etc. So creating a user that's the create user button.
- And then once the user is created, the ellipses are three dots, whatever this is called.
- That is where you can pull up all the details and take additional actions on the user.
- Now, the only thing you can really change after the user is created is their first name and their last name. That's it.
- Once the email is registered, it's kind of locked in.
- You can change their roles to you can add or remove some roles as the as an admin, depending on your permissions, but you're not going to really be able to change the email address.
- What you would do is delete the user and then re add them with a new email invitation.
- Setting up email notifications emails.
- Good rule filtering is always good to go with outlook because otherwise we get overwhelmed and we all love emails.
- Anyways, you're going to go to support and resources general settings and then scroll all the way to the bottom.
- And you can also set up email notifications through endpoint security crowd score incidents and then click on an incident and be able to set up email notifications there.
- But Hayley, what if you go to the incidents page and you don't see the option to set up email notifications?
- Well, what roles are assigned to you?
- You're going to ask yourself that a lot when you're in the console for if you can do something or if you can't do something, ask yourself what roles you're assigned to and maybe you're not supposed to be able to see it or perform that function.
- Also, what is an incident?
- An incident is made up of multiple detections.
- When CrowdStrike feels that a certain sequence of events in a timeline.
- Triggers enough detections for it to be overly concerned or really say this qualifies to be promoted from four separate detections to one incident.
- It will combine all of the detections and put them into your incidence page.
- The incidence page is going to be different than your detections page, but you can also view your incidence within your detections page.
- So if I didn't confuse you enough with what I just said, we'll be sure to cover that and the demonstration.
- But just be aware that there is a separate section in the console to view all of your incidents, and it's definitely a bit more granular with the descriptions of what's going on.
- As CrowdStrike felt, those series of detections were a bit more serious and they kind of give you a nice write up in description and additional details about the events that happened.
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

---
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
