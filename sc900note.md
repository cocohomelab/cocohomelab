- What i've learn:
- ## Describe security and compliance concepts
	- ^^Describe the shared responsibility model^^
		- **On-Premises**:
			- The organization is fully responsible for all aspects of security and compliance, including physical security, encrypting data, and managing infrastructure.
		- **Cloud Deployment Models**:
			- **IaaS (Infrastructure as a Service)**:
				- The customer is responsible for the software components like operating systems, applications, and network security.
				- The cloud provider manages the physical infrastructure (hardware, network, data center security).
			- **PaaS (Platform as a Service)**:
				- The customer is responsible for applications and data.
				- The cloud provider manages the underlying hardware and operating systems.
			- **SaaS (Software as a Service)**:
				- The customer is responsible only for data, accounts, identities, and devices.
				- The cloud provider manages everything else, including the software, hardware, and operating system.
		- **Core Responsibilities Retained by the Customer**:
			- **Data and Information**: The customer owns and must protect their data in any cloud model.
			- **Devices**: Customer responsibility includes securing mobile devices, PCs, printers, etc.
			- **Accounts and Identities**: Ensuring the security of user accounts and identities remains the customer’s responsibility.
		- **Benefits of the Shared Responsibility Model**:
			- Clarifies which security tasks are handled by the cloud provider and which are the customer’s responsibility, ensuring a clear division of duties for security and compliance.
			  
			  This model helps organizations understand and manage their security duties based on the type of cloud service (IaaS, PaaS, or SaaS) they are using.
	- ^^Describe defense-in-depth^^
		- ### 1.  **Defense in Depth**
		- **Layered Security Approach**: Defense in depth uses multiple layers of security to protect systems. If one layer is breached, subsequent layers will prevent unauthorized access.
		- **Examples of Security Layers**:
			- **Physical security**: Limiting access to data centers.
			- **Identity & access controls**: Using multifactor authentication (MFA) and access policies.
			- **Perimeter security**: DDoS protection to prevent service disruptions.
			- **Network security**: Network segmentation and access control to limit communication between resources.
			- **Compute security**: Protecting virtual machines (VMs) by restricting access.
			- **Application security**: Securing applications and ensuring they are free from vulnerabilities.
			- **Data security**: Protecting sensitive data through access management and encryption.
		- ### 2.  **CIA Triad (Confidentiality, Integrity, Availability)**
		- These are the core principles of cybersecurity:
			- **Confidentiality**: Ensuring sensitive data (e.g., passwords, financial data) is kept private. Encryption is a common method to ensure confidentiality.
			- **Integrity**: Ensuring data or messages are accurate and unchanged. Data should not be tampered with in transit or storage.
			- **Availability**: Ensuring data and services are accessible to authorized users when needed, while maintaining security.
		- ### 3.  **Importance for Exam** :
		- **CIA Triad** is a foundation of cybersecurity, so understanding how it applies to systems, networks, and applications is crucial.
		- **Defense in Depth** exemplifies a multi-layered security approach, which you need to recognize as a best practice in preventing breaches.
		- ### Key Concepts for the SC-900 Exam:
		- Layers of security work together to create a defense system that slows down or stops attackers.
		- The **CIA Triad** is central to security strategies, ensuring the confidentiality, integrity, and availability of systems and data.
		- You may encounter questions on how these principles apply to Microsoft's security offerings and how they can be implemented in Azure and other Microsoft environments.
		  
		  Understanding these security layers and how they align with **Confidentiality, Integrity, and Availability** will help you grasp essential concepts for the SC-900 exam.
	- Describe the Zero Trust model
		- ### Zero Trust Overview:
		- **Assumes no trust**: Everything, even within the corporate network, is considered untrusted. The model operates on the principle of "trust no one, verify everything."
		- **Why it's necessary**: Traditional security models are no longer sufficient to prevent attackers from bypassing access controls. Zero Trust strengthens security by eliminating trust in any part of the network.
		- **Key Practices**:
			- **Multi-factor authentication** is used in addition to passwords.
			- Users are granted **least privilege** access to specific apps/data, not entire networks.
		- ### Zero Trust Guiding Principles:
		- **Verify Explicitly**: Authenticate and authorize users based on multiple data points (identity, location, device, etc.).
		- **Least Privilege Access**: Provide **just-in-time** and **just-enough** access (JIT/JEA), ensuring only necessary permissions for users.
		- **Assume Breach**: Always act under the assumption that a breach may occur. Implement segmentation, encryption, and monitoring to minimize damage and improve response.
		- ### Six Foundational Pillars:
		- **Identities**: Verify user, service, or device identities with strong authentication, ensuring least privilege access.
		- **Devices**: Monitor device health and compliance to reduce attack surfaces.
		- **Applications**: Manage applications, including **Shadow IT** (unauthorized apps), permissions, and access controls.
		- **Data**: Classify, label, and encrypt data. Protect data at rest and in transit.
		- **Infrastructure**: Secure infrastructure (on-prem or cloud) through assessments, configurations, and telemetry to detect and respond to threats.
		- **Networks**: Segment networks, use micro-segmentation, and implement real-time protection, monitoring, and encryption.
		- ### Diagram Representation:
		  
		  A Zero Trust model integrates these principles and pillars to enforce end-to-end security across an organization.
		  
		  **Key Takeaways for SC-900**:
		- Understand the principles of Zero Trust (Verify explicitly, Least privilege, Assume breach).
		- Know the foundational pillars: Identities, Devices, Applications, Data, Infrastructure, and Networks.
		- Recognize that Zero Trust aims to secure the entire IT environment, not just the network perimeter.
	- ^^Describe encryption and hashing^^
		- ### Types of Encryption:
		- **Symmetric Encryption**:
			- Same key is used to both encrypt and decrypt data.
			- Example: AES encryption.
		- **Asymmetric Encryption**:
			- Uses a public-private key pair.
			- Data encrypted with a public key can only be decrypted with the corresponding private key, and vice versa.
			- Example: HTTPS (used in secure web browsing).
		- ### Data Encryption:
		- **Data at Rest**:
			- Refers to data stored on a physical device (e.g., server, database).
			- Encryption protects data by making it unreadable without the decryption key.
		- **Data in Transit**:
			- Refers to data moving across networks (e.g., internet, private networks).
			- Encrypting data in transit (e.g., HTTPS) ensures it’s protected from eavesdropping or tampering.
		- **Data in Use**:
			- Refers to data being processed, such as in RAM or CPU caches.
			- Uses encryption technologies that create secure enclaves to protect data while being processed.
		- ### Hashing:
		- **Hashing**: Converts data into a fixed-length value (hash). It's used for unique identification, such as storing passwords.
			- **Key points**:
				- Hashing does not use keys.
				- The same input always produces the same hash.
				- Hashes are irreversible (cannot be decrypted back to the original data).
				- Used in password storage (e.g., comparing the hash of entered password with stored hash).
				- **Salt**: A random value added to the input before hashing to protect against brute-force attacks.
		- ### Key Concepts:
		- **Encryption** is used to protect sensitive data by making it unreadable without a key.
		- **Data at Rest, in Transit, and in Use** refer to different stages of data that can be protected through encryption.
		- **Hashing** is used for data integrity (like passwords) and doesn’t require a decryption key.
		  
		  This summary includes the most important concepts about encryption and hashing for the SC-900 exam, with emphasis on types of encryption and their use cases.
	- ^^Describe Governance, Risk, and Compliance (GRC) concepts^^
		- ### **Governance**
		- Governance is the system of rules, practices, and processes used to direct and control an organization's activities.
		- It includes setting policies and procedures to manage access to resources and define administrative privileges.
		- Often driven by external standards, obligations, and expectations.
		- ### **Risk**
		- Risk management involves identifying, assessing, and responding to threats that can affect company objectives.
		- Risks come from **external sources** (e.g., economic, political, security breaches, weather) and **internal sources** (e.g., data leaks, fraud, insider threats).
		- ### **Compliance**
		- Compliance refers to adhering to laws, regulations, and standards set by governments or regulatory bodies.
		- It includes ensuring that data is protected and processes follow legal mandates.
		- Compliance is **not the same as security** but requires security measures to meet legal standards.
		- ### **Key Compliance Concepts**
		- **Data Residency**: Regulations governing where data can be stored and how it can be transferred, processed, or accessed.
		- **Data Sovereignty**: Data must adhere to the laws of the country where it’s collected, stored, or processed.
		- **Data Privacy**: Laws that govern the collection, processing, use, and sharing of personal data.
		- ### **Summary**
		- A **structured approach** to managing GRC helps reduce risks and improve compliance.
		- Organizations should ensure they meet **minimum compliance standards** and implement strong **security measures** to protect sensitive data.
		- Understanding **compliance concepts** like data residency, sovereignty, and privacy is crucial for managing data within legal requirements.
- ## Define identity concepts
	- ^^Define identity as the primary security perimeter^^
		- ### **1. Changing Collaboration Needs**
		- **Digital collaboration** has become essential, with employees and partners needing to access resources from anywhere, on any device, and without productivity loss.
		- **Remote work** has increased, emphasizing the need for flexible and secure access to organizational resources.
		- ### 2.  **Expanded Security Perimeter**
		- Traditional **perimeter-based security** is no longer sufficient.
		- The security perimeter now extends beyond the corporate network to:
			- **SaaS applications** (business-critical workloads hosted outside the corporate network).
			- **BYOD (Bring Your Own Device)**: Personal devices employees use to access corporate resources from home.
			- **Unmanaged devices** used by external partners or customers.
			- **IoT devices** in the corporate network and customer locations.
		- ### 3.  **Identity as the New Security Perimeter**
		- **Identity** has become the primary method of securing assets. It is now the cornerstone of security because it defines who or what can access resources.
		- **Identity** refers to the data used to authenticate and authorize users, devices, or applications (e.g., usernames, passwords, authorization levels).
		- ### 4.  **Four Pillars of Identity Infrastructure**
		- Organizations should adopt a comprehensive approach to identity management, focusing on the following pillars:
			- **Administration**: Creation and management of identities for users, devices, and services. Ensures identities are appropriately governed and updated.
			- **Authentication**: Verifying identity through credentials (e.g., usernames and passwords) to ensure legitimacy.
			- **Authorization**: Determining the level of access an authenticated identity has to resources.
			- **Auditing**: Tracking identity-related activities for compliance and security, including reporting, alerts, and governance.
			  
			  Addressing these pillars is essential for a secure, identity-driven access control system. Understanding these concepts will help in securing organizational resources and preparing for the SC-900 exam.
	- ^^Define authentication^^
		- **Authentication (AuthN)**:
		- The process of verifying the identity of a user, device, or system.
		- Example: Username and password combination to access a computer or device.
		- The goal is to confirm that the person is who they claim to be.
	- ^^Define authorization^^
		- **Authorization (AuthZ)**:
		- The process of determining what an authenticated user can access or do.
		- Example: A hotel keycard allows access only to specific areas like your room.
		- The goal is to define what resources and actions the authenticated person is permitted to interact with.
	- ^^Describe identity providers^^
		- **Modern Authentication:**
		- **Definition**: Modern authentication refers to authentication and authorization methods used between a client (e.g., laptop or phone) and a server (e.g., website or application), managed by an identity provider.
		- **Identity Provider (IdP)**: Central to modern authentication, an IdP creates, maintains, and manages identity information. It provides authentication, authorization, and auditing services.
		- **Centralized Authentication**: All authentication services are supplied by a central IdP, which stores and manages the information required to authenticate users.
		- **Key Benefits**:
			- Establishes policies for authentication and authorization.
			- Monitors user behavior and detects suspicious activities.
			- Helps reduce malicious attacks.
		- **How It Works**:
			- The client provides an identity to the IdP, which authenticates it.
			- Once verified, the IdP issues a **security token**.
			- The client sends the token to the server for validation.
			- The server trusts the IdP to validate the token, granting access to resources based on the token's data.
			  
			  **Examples of Identity Providers**:
		- Microsoft Entra ID, Google, Amazon, LinkedIn, GitHub.
		  
		  **Single Sign-On (SSO)**:
		- **SSO** allows users to log in once and use the same credentials to access multiple applications or resources.
		- **Federation**: Setting up SSO between multiple identity providers is called federation, allowing seamless access across different services.
		  
		  These concepts highlight modern authentication's central role in simplifying and securing user access across multiple systems. For the SC-900 exam, understanding how identity providers, authentication tokens, and SSO work is crucial.
	- ^^Describe the concept of directory services and Active Directory^^
		- **Directory**: A hierarchical structure that stores network objects' information, accessible by users, administrators, services, and applications.
		- **Directory Service**: Manages and makes directory data available to users and services.
		- **Active Directory (AD)**: A Microsoft service used in on-premises domain-based networks, introduced in Windows 2000. The most common component is **Active Directory Domain Services (AD DS)**. Key functions include:
			- **Storing Information**: About domain users, devices, etc.
			- **Credential Verification**: Verifies identities of network members.
			- **Access Control**: Manages user permissions and access rights.
			- **Domain Controller (DC)**: A server running AD DS to manage the domain.
		- **AD DS**: Central to on-premises IT, enabling organizations to manage users with a single identity, but has limitations for:
			- Mobile devices
			- SaaS apps
			- Modern authentication methods
		- **Microsoft Entra ID**: Formerly Azure AD, part of the **Microsoft Entra** family. It evolved to support:
			- Identity as a Service (IDaaS)
			- Cloud and on-premises applications
			- Mobile and modern authentication
			  
			  Understanding the differences between AD DS and Entra ID is crucial, as Entra ID offers more modern identity management across cloud environments and on-premises setups.
			  
			  For the exam, focus on:
		- The role of **Active Directory Domain Services (AD DS)** in on-premises networks.
		- The evolution to **Microsoft Entra ID** to support modern cloud and mobile environments.
	- ^^Describe the concept of federation^^
		- Federation allows users to access services across different organizations or domains without needing separate usernames and passwords. This is achieved by establishing a trust relationship between identity providers (IdPs) in each domain.
		  
		  Key points:
		- **Federation Workflow**:
			- A user in Domain B (authenticates with IdP-B) tries to access a website in Domain A (uses IdP-A for authentication).
			- IdP-A and IdP-B have a pre-configured trust relationship, so the website in Domain A trusts the user authenticated by IdP-B.
			- Access is granted based on the established trust, not the user's credentials for Domain A.
		- **Bidirectional Trust**:
			- Trust isn't automatically bidirectional. IdP-A may trust IdP-B, but unless configured, IdP-B may not trust IdP-A.
		- **Real-World Example**:
			- A user logging into a third-party site using a social media account (e.g., X). Here, X is an identity provider, and the third-party site might use a different identity provider (e.g., Microsoft Entra ID). A trust relationship between the two IdPs enables this login.
			  
			  Understanding federation for the SC-900 exam involves recognizing how trust relationships between IdPs facilitate seamless access across domains without the need for multiple credentials.
- ## Describe function and identity types of Microsoft Entra ID
	- ^^Describe Microsoft Entra ID^^
		- ### Overview:
		- **Microsoft Entra ID** is a cloud-based **identity and access management (IAM)** service used by organizations to manage sign-ins and access to both internal and external resources.
			- **Internal resources**: Corporate apps, intranet, and cloud apps.
			- **External resources**: Microsoft Office 365, Azure portal, and other SaaS apps.
		- ### Key Features:
		- **Identity and Access Management**: Simplifies managing access to cloud and on-premises applications with a unified identity system.
		- Can synchronize with **on-premises Active Directory**, other directory services, or work as a **standalone service**.
		- Supports **bring-your-own-device** policies and facilitates **collaboration with partners and customers**.
		- ### Important Concepts:
		- **Tenant**: An instance of Microsoft Entra ID for a specific organization. It includes all resources like users, groups, and devices. Each tenant has a unique **tenant ID** and domain name (e.g., `contoso.onmicrosoft.com`).
		- **Directory**: A logical container within a tenant that holds identity-related resources (users, groups, apps, devices). The terms **directory** and **tenant** are often used interchangeably.
		- **Multi-tenant**: An organization with multiple instances of Entra ID. Reasons for this include mergers, acquisitions, or operating in different regions with specific compliance requirements.
		- **Identity Secure Score**: A security indicator that shows how well your organization aligns with Microsoft's security best practices. It helps measure and improve identity security posture with tailored actions for improvement.
		- ### Who Uses Microsoft Entra ID:
		- **IT admins**: Control access to resources based on business needs (e.g., requiring multi-factor authentication).
		- **Developers**: Use Entra ID to implement **single sign-on (SSO)** and build personalized apps using organizational data via APIs.
		- **Subscribers** to Azure, Microsoft 365, or Dynamics 365 automatically get access to Microsoft Entra ID. Premium licenses can enhance the service.
		  
		  By focusing on these core concepts, you'll be better prepared for the **SC-900 exam**, as these topics cover the fundamental aspects of identity and access management within the Microsoft cloud environment.
	- ^^Describe types of identities^^
		- **Types of Identities**:
			- **User Identities**: Represent people (internal and external users). Internal users are employees authenticated within the organization, while external users (guests) are customers, vendors, or partners. **UserType** can be *Member* or *Guest*.
			- **Workload Identities**: Assigned to software-based objects (applications, VMs, services). These are crucial for authentication and secure access to resources.
			- **Device Identities**: Assigned to hardware like phones, laptops, or printers, allowing for device management and Single Sign-On (SSO) to resources.
			- **External Identities**: Includes external (B2B) users who access organizational resources, typically using their own credentials through external identity providers.
		- **Workload Identity Types**:
			- **Service Principal**: An identity for applications after they are registered with Microsoft Entra ID.
			- **Managed Identities**: Automatically managed identities tied to Azure resources. There are two types:
				- **System-assigned**: Tied to the lifecycle of a single resource.
				- **User-assigned**: Can be assigned to multiple resources, independently managed.
		- **Device Identity Types**:
			- **Microsoft Entra Registered Devices**: For personal devices (BYOD) accessing organizational resources.
			- **Microsoft Entra Joined Devices**: Devices owned by the organization and used to sign in with organizational accounts.
			- **Microsoft Entra Hybrid Joined Devices**: Devices that are joined to both Active Directory and Entra ID.
		- **Groups in Entra ID**:
			- **Security Groups**: Manage access to shared resources and can include users, devices, or service principals. Used for security policies like MFA.
			- **Microsoft 365 Groups**: Used for collaboration, providing access to shared mailboxes, calendars, and resources.
			- **Dynamic Membership**: Groups can be configured to automatically add/remove users based on rules.
		- **Authentication and Access**:
			- **Internal vs. External Authentication**: Internal users authenticate with Entra ID, while external users authenticate with third-party identity providers.
			- **UserType Property**: Defines whether users are internal (Member) or external (Guest).
			  
			  Understanding these identity types and their roles is crucial for implementing identity management and security in Microsoft Entra ID. This knowledge also supports Zero Trust principles by ensuring access is granted only to necessary identities and securing resources through managed identities.
	- ^^Describe hybrid identity^^
		- **Hybrid Identity**: Hybrid identity refers to a unified identity system that works across both on-premises and cloud environments. It enables users to have a single identity for accessing resources regardless of where those resources are hosted (on-premises or in the cloud).
		- **Provisioning and Synchronization**:
			- **Provisioning**: The process of creating identities in different directory systems, such as when an on-premises user in Active Directory is provisioned into Microsoft Entra ID (cloud).
			- **Synchronization**: Ensures that identity data for users and groups is consistent across both on-premises and cloud environments.
		- **Microsoft Entra Cloud Sync**: This service helps achieve hybrid identity by synchronizing and provisioning users, groups, and contacts between on-premises Active Directory and Microsoft Entra ID. It uses a lightweight agent that acts as a bridge between the two directories.
		- **SCIM Specification**: The System for Cross-domain Identity Management (SCIM) is a standard used to automate the exchange of user and group identity information between systems. It facilitates provisioning and deprovisioning of users and groups across different identity domains, including Microsoft Entra ID.
		- **Key Technology**: The Microsoft Entra Cloud Sync agent leverages the SCIM specification to enable inter-directory provisioning and synchronization, simplifying hybrid identity management.
		  
		  In short, Microsoft Entra Cloud Sync helps manage identities across both on-premises and cloud environments, ensuring smooth authentication and authorization for users. SCIM is crucial for automating this process.
	- ^^Describe external identities^^
		- ### Key Concepts:
		- **Collaboration with External Users:**
			- Microsoft Entra External ID enables secure collaboration with people outside your organization, such as partners, consumers, or business customers.
			- External identities can include corporate, government-issued accounts, or social identities like Google or Facebook.
		- **Tenant Configurations:**
			- **Workforce Tenant Configuration:** For internal employees and apps, but can invite external business partners or guests (B2B collaboration).
			- **External Tenant Configuration:** Used for external-facing apps (such as consumer apps or business customer apps).
		- **B2B Collaboration (Business-to-Business):**
			- Allows external partners or guests to access your organization's apps and resources.
			- Guests authenticate with their own identity provider and are granted access to specific resources without needing a new set of credentials.
		- **Customer Identity and Access Management (CIAM):**
			- For organizations or developers creating apps for consumers or business customers.
			- Provides self-service registration, personalized sign-ins (including single sign-on), and customer account management.
			- Benefits include enhanced security, compliance, and scalability, with integration into Microsoft Entra ID.
		- ### Important Scenarios:
		- **Collaborate with Business Guests:** Use **B2B collaboration** to allow employees to share applications and services securely with business partners or guests.
		- **Secure Apps for Consumers and Business Customers:** Leverage **External ID** to manage consumer identity and authentication for consumer-facing apps.
		- ### Tenant Configuration Choices:
		- **Workforce Tenant:** Best for internal business and partner collaboration.
		- **External Tenant:** Ideal for managing external-facing apps, especially for consumer and customer apps.
		  
		  These points are crucial to understanding Microsoft Entra External ID and its role in identity and access management when dealing with external users, which is likely to be part of your SC-900 exam.
- ## Describe authentication capabilities of Microsoft Entra ID
	- ^^Describe the authentication methods^^
		- **Password-based Authentication**:
			- **Issues**: Passwords are common but vulnerable in single-factor authentication (SFA). They can be easily guessed or hacked.
			- **Recommendation**: Use more secure authentication methods like **passwordless** authentication to reduce security risks.
		- **Phone-based Authentication**:
			- **SMS-based Authentication**: Users receive a text with a verification code. Used both as a primary (rare) and secondary (common) form for **multifactor authentication (MFA)** or **self-service password reset (SSPR)**.
			- **Voice Call Verification**: Users receive an automated voice call and must press # to verify identity. Used for secondary authentication only.
		- **OATH Authentication**:
			- **TOTP (Time-based One-Time Password)**: Generates codes using software (apps) or hardware tokens. Used as a secondary form of MFA or SSPR.
		- **Passwordless Authentication** (Primary Goal for Security):
			- **Windows Hello for Business**: Replaces passwords with strong 2FA (PIN or biometric + device certificate/key). It provides higher security by requiring both the device and biometric/PIN to authenticate.
			- **FIDO2**: Fast Identity Online (FIDO) An open standard for passwordless authentication. Users authenticate with an external or platform security key (USB, Bluetooth, NFC). It's highly secure and eliminates the need for passwords.
			- **Microsoft Authenticator App**: A mobile app that provides passwordless authentication using biometrics or PIN on iOS/Android devices. It also supports OATH codes for secondary authentication during MFA or SSPR.
		- **Certificate-Based Authentication (CBA)**:
			- **X.509 Certificates**: Used in **public key infrastructure (PKI)** for identity authentication. It serves as a primary form of passwordless authentication.
		- **Primary vs. Secondary Authentication**:
			- Some methods (like **Windows Hello for Business** and **FIDO2**) can serve as **primary** authentication, while others (such as SMS, OATH, Microsoft Authenticator) are used as **secondary** forms, typically in MFA or SSPR scenarios.
		- ### Key Takeaways for the Exam:
		- **Passwordless** methods (e.g., **Windows Hello for Business**, **FIDO2**, **Microsoft Authenticator**) are highly encouraged for better security.
		- **Primary Authentication**: Windows Hello, FIDO2, and certificate-based authentication.
		- **Secondary Authentication**: SMS, voice call, OATH (TOTP), and Microsoft Authenticator app during MFA or SSPR.
		  
		  Focus on the shift toward passwordless solutions, the security benefits of MFA, and the different authentication methods supported by Microsoft Entra ID.
	- ^^Describe multi-factor authentication (MFA)^^
		- ### Multifactor Authentication (MFA):
		- **Definition**: MFA adds an extra layer of security by requiring multiple forms of identification during sign-in (e.g., a password and a fingerprint).
		- **Key Components**:
			- **Something you know**: Typically a password or PIN.
			- **Something you have**: A trusted device like a phone, hardware key, or FIDO2 security key.
			- **Something you are**: Biometrics, such as a fingerprint or face scan.
		- ### Microsoft Entra MFA:
		- **How it works**: MFA is automatically integrated into the sign-in process of Microsoft Entra ID, prompting users to verify their identity using registered methods.
		- **Admin control**: Administrators can require specific verification methods, while users can manage their own verification methods through the MyAccount portal.
		- ### Verification Methods:
		- **Options for MFA** include:
			- Microsoft Authenticator app
			- Windows Hello for Business
			- FIDO2 security key
			- OATH hardware or software token (preview)
			- SMS
			- Voice call
		- ### Security Defaults:
		- **What they are**: Security defaults are a set of basic security features recommended by Microsoft to increase an organization’s security posture.
		- **Features of Security Defaults**:
			- Enforces MFA registration for all users.
			- Requires admins to use MFA.
			- Triggers MFA when necessary for users.
		- **Use cases**: Ideal for organizations that want basic security without advanced configurations, especially for those using free Microsoft Entra ID licenses. However, they might not be suitable for organizations with more complex security needs or higher-tier licenses (P1 or P2).
		- ### Key Takeaways for the Exam:
		- Understand the **three factors of MFA** (something you know, something you have, something you are).
		- Be familiar with **MFA methods** supported by Microsoft Entra (Authenticator app, Windows Hello, FIDO2, SMS, etc.).
		- Know how **Security Defaults** work and when to use them. They are useful for basic security but may not be enough for organizations with complex needs.
		  
		  These concepts are fundamental to understanding security in the context of Microsoft Entra ID and are critical for the SC-900 exam.
	- ^^Describe self-service password reset^^
		- **What SSPR does**: Self-service password reset (SSPR) allows users to reset or change their password without requiring IT support, reducing help desk calls and increasing productivity.
		- **Benefits**:
			- Reduces IT support costs.
			- Improves user productivity by enabling quicker password recovery.
			- Allows admins to roll out security settings without disrupting user sign-ins.
			- Provides audit logs for security monitoring.
		- **Requirements**:
			- Users need a **Microsoft Entra ID license**.
			- Users must be **enabled for SSPR** by an administrator.
			- Users need to **register authentication methods** (e.g., mobile app, email, phone, security questions).
		- **Authentication Methods**:
			- Mobile app notification, mobile app code, email, mobile phone, office phone, security questions (secondary authentication during password reset only, not for sign-in).
		- **Administrator Role**:
			- Admin accounts are enabled for SSPR by default, but they must use **two authentication methods** (e.g., email, phone, authenticator app).
			- Admins cannot use **security questions** for password reset.
		- **Password Write-back**: Allows password updates to be synced with on-premises Active Directory, ensuring users can use updated credentials without delay.
		- **Email Notifications**: Admins can configure notifications to alert users and global admins when an SSPR event occurs, especially for admin account resets, adding an extra security layer.
		  
		  These points highlight how SSPR improves both user experience and security management in Microsoft Entra ID.
	- ^^Describe password protection and management capabilities^^
		- **Microsoft Entra Password Protection** is designed to reduce the risk of weak passwords. It detects and blocks known weak passwords and their variants, including custom weak passwords specific to your organization.
		- **Global Banned Password List**:
			- This list includes known weak passwords (e.g., "P@$$w0rd" or "Password1") and is automatically enforced by Microsoft for all users in a Microsoft Entra tenant.
			- The list is regularly updated based on real-world security data (password spray attacks).
			- Password variations (e.g., "Passw0rd1") are also blocked using a fuzzy-matching algorithm.
			- The global banned password list cannot be disabled.
		- **Custom Banned Password List**:
			- Admins can define a custom list of banned passwords tailored to the organization's needs, such as brand names, product names, or internal terms.
			- This list is combined with the global list to block weak passwords, improving security.
		- **Password Spray Attack Protection**:
			- Microsoft Entra helps defend against password spray attacks (where attackers try weak passwords on multiple accounts). It blocks the use of weak passwords commonly targeted in these attacks.
		- **Hybrid Security Integration**:
			- Microsoft Entra password protection can be integrated with on-premises Active Directory environments. Domain controllers receive the banned password lists and policies to enforce strong passwords even in hybrid environments.
		- **Multifactor Authentication**:
			- While Entra password protection improves password strength, it is still recommended to use multifactor authentication (MFA) as an additional layer of security. Passwords alone are not sufficient.
			  
			  This feature is available with **Microsoft Entra ID P1 or P2** licenses. It helps improve security by blocking weak or easily guessable passwords and defending against password spray attacks.
- ## Describe access management capabilities of Microsoft Entra ID
	- ^^Describe Conditional Access^^
		- ### Conditional Access Overview
		- **Conditional Access** in Microsoft Entra ID is a security feature that determines whether a user can access resources based on specific criteria, or "signals."
		- **Signals** include factors such as user identity, location, device, app, and risk level, which help enforce access control decisions after the user has been authenticated.
		- It works through **if-then statements**, such as: "If the user is in a certain group, require multi-factor authentication (MFA) to access an app."
		- ### Key Concepts
		- **Conditional Access Policies**: These policies decide whether access is granted or blocked. After the user authenticates, these policies evaluate several factors to determine access.
		- **Components of Conditional Access Policy**:
			- **Assignments**: Defines the conditions for who, what, where, and when the policy applies.
				- **Users**: Who the policy applies to (e.g., groups, specific users, external guests).
				- **Target Resources**: Includes cloud apps, user actions, and authentication context (e.g., requiring a managed device).
				- **Network/Location**: Specifies trusted IPs or locations to restrict access based on geographic or network considerations.
				- **Conditions**: Conditions include sign-in and user risk (i.e., suspicious login activities) and device platform (i.e., mobile or desktop OS).
			- **Access Controls**: Defines the actions that occur once the policy criteria are met.
				- **Block Access**: Denies access to the resource.
				- **Grant Access**: Access is granted with additional controls like requiring MFA or device compliance.
				- **Session Controls**: Apply limited access, such as blocking document download or requiring frequent re-authentication.
		- ### Important Points:
		- **Enforcement After Authentication**: Conditional Access policies are applied after the initial authentication, so they're not a first line of defense (e.g., against denial-of-service attacks).
		- **Assignments = Who, What, Where**: The **assignments** component controls the conditions for the policy—like which users, resources, or locations it applies to.
		- **Access Controls = How Access is Managed**: **Access controls** define what happens after the policy is triggered—whether access is granted, blocked, or subject to additional conditions.
		  
		  In summary:
		- **Assignments** define the policy's scope (who, what, where, when).
		- **Access Controls** define the policy's enforcement (grant, block, or session controls).
	- ^^Describe Global Secure Access in Microsoft Entra^^
		- ### **Microsoft Entra Overview**
		- **Global Secure Access**: A unifying term for Microsoft Entra Internet Access and Microsoft Entra Private Access. It converges Zero Trust network, identity, and endpoint access controls to secure access to any app or resource, from any location, device, or identity. It's part of a new category of network security solutions known as **Security Service Edge (SSE)**.
		- ### **Microsoft Entra Internet Access**
		- **Purpose**: Secures access to SaaS applications and internet-based apps while protecting users, devices, and data from threats.
		- **Features**:
			- Identity-centric Secure Web Gateway (SWG) solution.
			- **Conditional Access**: Enforces compliant network checks during authentication and data access.
			- **Continuous Access Evaluation (CAE)**: Ensures real-time security and up-to-date access.
			- **Tenant restrictions**: Prevents data exfiltration.
			- **Web Content Filtering**: Controls website access based on categories and domain names.
		- ### **Microsoft Entra Private Access**
		- **Purpose**: Secures access to private corporate resources for users, whether in an office or remotely.
		- **Key Components**:
			- **Quick Access**: A simple setup where private resources are grouped under a container (enterprise application) and linked to conditional access policies.
			- **Global Secure Access app (Per-app Access)**: Provides more granular control by creating multiple containers, each with its own access policies based on user groups, time, or resource type.
		- ### **Security Challenges Addressed by Global Secure Access (SSE)**
		- **Reduced lateral movement**: By avoiding over-permissioned VPNs.
		- **Better perimeter protection**: For internet-based assets.
		- **Remote office security**: Improved service for branch offices.
		- ### **Global Secure Access Dashboard**
		- Provides insights into network traffic and security configurations with visualizations. Key features include:
			- **Snapshot Widget**: Displays summary statistics about network traffic, users, and applications.
			- **Usage Profiling**: Displays traffic patterns over time.
			- **Alerts & Notifications**: Identifies suspicious activities like unhealthy networks or increased external activity.
			- **Cross-Tenant Access**: Shows sign-ins and access data across tenants.
			- **Web Category Filtering**: Displays blocked/allowed web content categories.
			- **Device Status**: Monitors the active/inactive status of deployed devices.
		- ### **Key Points for Exam Success** :
		- Understand the **difference between Microsoft Entra Internet Access** (focus on internet-facing security) and **Microsoft Entra Private Access** (focus on securing private resources).
		- Learn the **features of Zero Trust** and **SSE** concepts.
		- Familiarize with **Conditional Access**, **Continuous Access Evaluation (CAE)**, and **traffic routing policies**.
		- Know the **dashboard components** like usage profiling, alerts, and cross-tenant access.
		  
		  This overview helps you grasp the key functionalities of Microsoft Entra in the context of securing both internet and private resources in a hybrid work environment. Focus on understanding how these components work together to enable secure access and improve network visibility.
	- ^^Describe Microsoft Entra roles and role-based access control (RBAC)^^
		- ### **Role-Based Access Control (RBAC)**
		- **RBAC** is used to manage permissions to Microsoft Entra resources, such as creating user accounts or viewing billing info.
		- **Microsoft Entra RBAC** includes both built-in and custom roles to control access.
		- ### 2.  **Built-in Roles**
		- **Global Administrator**: Full access to all features in Microsoft Entra.
		- **User Administrator**: Manages users and groups, support tickets, and service health.
		- **Billing Administrator**: Manages subscriptions, purchases, and support tickets.
		- These roles cannot be modified and come with fixed permissions.
		- ### 3.  **Custom Roles**
		- Custom roles allow flexibility by letting you select specific permissions from a preset list.
		- **Two-step process** for granting access:
			- Create a custom role definition (choose permissions).
			- Assign the role to users/groups (defining scope—either organization-wide or specific to an object).
		- Custom roles require a **Microsoft Entra ID P1 or P2** license.
		- ### 4.  **Best Practices**
		- Grant the **least privilege** necessary for users to perform their work. For example, assign a **User Administrator** role instead of **Global Administrator** for those who mainly manage users.
		- ### 5.  **Categories of Microsoft Entra Roles**
		- **Microsoft Entra Specific Roles**: Access to manage resources in Microsoft Entra (e.g., User Administrator, Application Administrator).
		- **Service-Specific Roles**: Roles for managing specific Microsoft 365 services like **Exchange Administrator**, **Intune Administrator**, etc.
		- **Cross-Service Roles**: Roles like **Security Administrator** and **Compliance Administrator**, which provide access across multiple services (e.g., security or compliance settings).
		- ### 6.  **Entra RBAC vs Azure RBAC**
		- **Microsoft Entra RBAC**: Controls access to Microsoft Entra resources like users, groups, and applications.
		- **Azure RBAC**: Controls access to Azure resources like virtual machines and storage, using Azure Resource Management.
		- Both systems use RBAC but for different sets of resources, and have separate data stores and access checks.
		- ### Key Takeaways:
		- **RBAC** controls access based on roles.
		- **Built-in roles** are fixed and predefined, while **custom roles** allow for tailored access permissions.
		- Understanding the **scope** of roles (organization-wide vs. object-specific) and assigning **least privilege** are critical concepts for security.
		- The difference between **Microsoft Entra RBAC** and **Azure RBAC** is primarily what resources they control.
		  
		  This breakdown will help you understand how roles and access are managed in Microsoft Entra for the SC-900 exam.
- ## Describe identity protection and governance capabilities of Microsoft Entra
	- ^^Describe Microsoft Entra ID Governance^^
		- ### **Overview of Microsoft Entra ID Governance**
		- It balances security and employee productivity through automated identity and access management.
		- Helps manage **identity lifecycle**, **access lifecycle**, and **privileged access**.
		- ### 2.  **Key Tasks in ID Governance**
		- **Govern the identity lifecycle** (managing user identities and their access across roles).
		- **Govern access lifecycle** (ensuring the right access is granted and adjusted as users progress in their roles).
		- **Secure privileged access** (monitor and restrict access for administrative roles).
		- ### 3.  **Four Key Governance Questions**
		- **Which users should have access to which resources?**
		- **What are those users doing with that access?**
		- **Are there effective organizational controls for managing access?**
		- **Can auditors verify that the controls are working?**
		- ### 4.  **Identity Lifecycle**
		- **Join, Move, Leave Process**:
			- **Join**: A digital identity is created when a new employee joins.
			- **Move**: Access rights change when employees move roles within the organization.
			- **Leave**: When employees leave, their access is revoked, and the identity may be archived for auditing purposes.
		- Automation is key through integration with **HR systems** (like Workday) and **lifecycle workflows** for seamless identity management.
		- ### 5.  **Access Lifecycle**
		- Manages access based on role and responsibility throughout the user's tenure.
		- Key features include:
			- **Dynamic Groups**: Automatically assign users to groups based on attributes (e.g., department).
			- **Entitlement Management**: Allows users to request access to resources like groups, applications, and SharePoint roles.
			- **Access Reviews**: Regular reviews ensure that users still require access.
		- ### 6.  **Privileged Access Lifecycle**
		- Focuses on controlling administrative access to sensitive resources.
		- **Privileged Identity Management (PIM)** helps to minimize and govern the number of privileged users, offering more granular control and monitoring over who has access to critical resources.
		- **Access Rights Lifecycle**: Admin roles evolve over time, from no admin role to gaining and losing specific privileges.
		- ### **Important Exam Tips**
		- Understand how automated processes like **dynamic groups**, **entitlement management**, and **PIM** streamline governance.
		- Know the **identity lifecycle** stages: join, move, leave, and the need for automation at each stage.
		- Focus on **privileged access** and the tools to secure it.
		- Be familiar with how access rights are assigned, modified, and reviewed.
		  
		  These concepts will help you understand how organizations maintain secure, efficient, and scalable access management for users, roles, and privileged accounts.
	- ^^Describe access reviews^^
		- ### Key Concepts:
		- **Microsoft Entra Access Reviews**: Help manage group memberships, access to applications, and role assignments, ensuring that only the right people have access to resources.
			- **Security Risk**: Excessive access rights pose a security risk, especially when people transition between teams or roles.
		- **Microsoft Entra ID**: Enables collaboration with both internal and external users. It supports group membership, guest invitations, cloud app access, and remote work across devices.
		- **Use Cases for Access Reviews**:
			- **Privileged Roles**: Regularly review users with administrative access to ensure only necessary users have privileged access.
			- **Business Critical Data**: Review access to critical resources for compliance, ensuring users can justify continued access.
			- **Policy Exceptions**: Review and maintain a list of exceptions to policies for auditing purposes.
			- **Guest Access**: Group owners should confirm that guests still require access to sensitive content.
		- **Periodic Reviews**: Access reviews can be set to occur at intervals (weekly, monthly, quarterly, annually), with notifications sent to reviewers, who can approve or deny access.
		- **Managing Access**:
			- Users and guests can recertify their access during the review process. Admins track the progress, and access is only modified after the review is complete.
			- **Auto or Manual Changes**: After the review, access can be removed either manually or automatically, except for dynamic or on-premises groups.
		- **Multi-stage Access Reviews**:
			- Allows multiple reviewers to assess access in stages. This is useful for complex workflows, such as requiring multiple attestations for recertification and audit needs.
			- Reduces the number of decisions for each reviewer, streamlining the review process.
		- ### Important Exam Considerations:
		- Access reviews are key for ensuring appropriate access management and meeting compliance requirements.
		- They help track and recertify who has access to critical systems and data, reducing the risk of unauthorized access.
		- You should understand how to configure periodic reviews, manage multi-stage workflows, and apply changes after the review is completed.
		  
		  This information provides a strong foundation for understanding how Microsoft Entra access reviews work and their role in managing user access effectively.
	- ^^Describe entitlement management^^
		- ### **Entitlement Management** :
		- **Purpose**: It automates identity and access lifecycle management at scale, addressing challenges like users not knowing what access they need, difficulty finding approvers, and holding onto access longer than necessary.
		- **Capabilities**:
			- **Access Packages**: Predefined collections of resources users can request access to.
			- **Delegated Access Package Managers**: Non-administrators can create and manage access packages, define policies like who can request access, who approves it, and when it expires.
			- **External User Management**: External users (B2B) are automatically invited into your directory when approved for access, and their accounts are removed when access expires (if no other active assignments remain).
		- ### **Microsoft Entra Terms of Use** :
		- **Purpose**: To ensure users read relevant disclaimers before accessing applications or data. It helps meet legal and compliance requirements.
		- **Use Cases**:
			- Before accessing sensitive data or applications.
			- Periodically to remind users of regulations.
			- Based on specific user attributes (e.g., roles).
			- For all users in the organization.
		- **Features**:
			- **Format**: Terms can be in PDF format, created by admins (e.g., contract documents).
			- **Conditional Access**: Enforced through Conditional Access policies, requiring users to accept terms before accessing an app.
			- Admins can track who accepted or declined the terms.
			  
			  By focusing on these key elements—delegated management of access packages, external user access control, and enforcing terms of use—you're covering critical aspects related to identity governance and compliance for the SC-900 exam.
	- ^^Describe the capabilities of Microsoft Entra Privileged Identity Management^^
		- **PIM Overview:**
		- **Purpose**: PIM is a service in Microsoft Entra ID designed to manage, control, and monitor access to critical resources within Microsoft services (Entra, Azure, Microsoft 365, Intune). It helps reduce risks related to excessive or misused access permissions.
		- **Key Features**:
			- **Just-in-time (JIT)**: Privileged access is granted only when needed.
			- **Time-bound**: Access is limited by start and end dates.
			- **Approval-based**: Requires specific approval to activate privileges.
			- **Visible**: Notifications are sent when privileged roles are activated.
			- **Auditable**: Full access history can be reviewed.
			  
			  **Why Use PIM?**
		- **Security**: Minimizes the risk of unauthorized access by reducing the number of users with elevated privileges.
		- **Control**: Provides oversight of what users are doing with administrative roles, helping prevent accidental or malicious actions.
		  
		  **What You Can Do with PIM**:
		- **Microsoft Entra Roles**: Manage directory roles, including built-in and custom roles.
		- **Azure Roles**: Manage role-based access control (RBAC) roles for Azure resources.
		- **PIM for Groups**: Govern group membership and ownership with just-in-time access for both roles and applications.
		  
		  **General Workflow**:
		- **Assign**: Roles are assigned to users, groups, or service principals. The assignment includes:
			- Members/Owners
			- Scope (limits access to specific resources)
			- Assignment Type (Eligible or Active)
			- Duration (start/end dates or permanent)
		- **Activate**: Users with eligible roles must activate the role before use. Activation includes selecting the duration and providing a reason.
		- **Approve/Deny**: Designated approvers receive notifications when a role request is pending. They can approve or deny the request.
		- **Extend/Renew**: Users can extend or renew a role assignment when it is about to expire or has already expired.
		  
		  **Audit**:
		- **Audit History**: PIM keeps a record of all role assignments and activations for up to 30 days, helping track privileged role usage.
		  
		  **Key Takeaways**:
		- PIM minimizes risk by ensuring that privileged access is only granted when necessary and with proper oversight.
		- The PIM workflow involves role assignment, activation, approval, and auditing to ensure controlled access to sensitive resources.
		  
		  Understanding these components of PIM will help you manage privileged access effectively, which is a key concept for the SC-900 exam.
	- ^^Describe Microsoft Entra ID Protection^^
		- **Overview:**
		  Microsoft Entra ID Protection helps organizations detect, investigate, and remediate identity-based risks for both user and workload identities. It integrates with other security tools like Conditional Access and SIEM for further actions.
		  
		  **Key Components:**
		- **Risk Detection**: Entra ID Protection analyzes trillions of signals daily to detect potential threats. Signals come from various Microsoft services, including Entra ID and consumer services (e.g., Xbox).
		- **Types of Risks**:
			- **Sign-in Risk**: Probability that a sign-in is unauthorized. Examples:
				- Sign-in from an anonymous IP.
				- Unusual travel (sign-ins from distant locations).
				- Unfamiliar sign-in properties.
			- **User Risk**: Probability that a user’s account is compromised. Examples:
				- Leaked credentials.
				- Suspicious sending patterns.
				- User-reported suspicious activity.
		- **Risk Detections**: Only generated when correct credentials are used. Incorrect credentials do not trigger detections.
		  
		  **Risk Actions**:
		- Actions like **multifactor authentication**, **password reset**, or **blocking access** can be triggered based on detected risks.
		  
		  **Investigation**:
		- Key reports for risk analysis:
			- **Risk Detections**: Individual risk events.
			- **Risky Sign-ins**: Reports risky sign-ins based on multiple detections.
			- **Risky Users**: Users with risky sign-ins or detections.
		- For businesses using Microsoft Security Copilot, the **risky users' report** provides additional insights and recommendations for mitigation.
		  
		  **Remediation**:
		- **Automated Remediation**: Enabling risk-based conditional access policies (e.g., requiring MFA or secure password reset).
		- **Manual Remediation**: Admins review and take actions such as dismissing, confirming safety, or confirming compromise.
		  
		  **Export**:
		- Risk data can be exported for further analysis using APIs, Log Analytics, Event Hubs, or integrated into SIEM tools for deeper investigation.
		  
		  **Important for Exam**:
		- Understand the differences between **sign-in risk** and **user risk**.
		- Be familiar with how to **detect, investigate**, and **remediate** identity-based risks.
		- Know the types of actions triggered by risk detections and how **automated vs manual remediation** works.
		- Review the key reports for tracking risks: **Risk Detections**, **Risky Sign-ins**, and **Risky Users**.
	- ^^Describe Microsoft Entra Permissions Management^^
		- Microsoft Entra Permissions Management is a Cloud Infrastructure Entitlement Management (CIEM) product that provides control over permissions in Microsoft Azure, AWS, and GCP. It helps organizations implement **Zero Trust** security, focusing on **least privilege access**, which is critical as organizations adopt **multicloud strategies** and manage increasing complexity in access control. Here’s a summary of the key points for the SC-900 exam:
		- ### Key Concepts:
		- **Zero Trust & Least Privilege**: Ensures users have only the permissions they need, reducing security risks.
		- **Multicloud Strategy**: Permissions management is essential across different cloud platforms (Azure, AWS, GCP).
		- **Permission Complexity**: Managing access in multicloud environments becomes more complex with increasing identities and permissions.
		- **Security Challenges**: IT teams face pressure to maintain secure and compliant access as the number of identities and cloud resources grows.
		- ### Key Features of Permissions Management:
		- **Discover**:
			- Identifies gaps between granted and used permissions.
			- Cross-cloud permissions discovery for AWS, Azure, and GCP.
			- **Permission Creep Index (PCI)**: Measures risk based on unused or excessive permissions.
			- **Permission Usage Analytics**: Provides a multi-dimensional view of permissions risk.
		- **Remediate**:
			- Right-sizes permissions based on usage.
			- Automates the deletion of unused permissions (those unused for 90+ days).
			- **On-demand Permissions**: Grants permissions only as needed and for a limited time.
		- **Monitor**:
			- Detects anomalous activities using **machine learning**-powered alerts.
			- Generates detailed **forensic reports** for investigation and remediation.
		- ### Benefits for Zero Trust Strategy:
		- **Comprehensive Visibility**: Tracks which identity is accessing what, where, and when.
		- **Automated Least Privilege Access**: Ensures only the necessary permissions are granted, reducing risk.
		- **Unified Access Policies**: Enforces consistent security policies across cloud infrastructure.
		  
		  By using the **discover**, **remediate**, and **monitor** phases, organizations can implement a modern Zero Trust security strategy, enhancing the principle of least privilege access across their cloud environments.
		  
		  This approach strengthens an organization's security posture and supports compliance across multicloud infrastructures, which is critical in today's dynamic cloud landscape.
	- ^^Describe Microsoft Entra Verified ID^^
		- **Purpose:**
		  Microsoft Entra Verified ID is a service that automates identity credential verification based on open standards, offering privacy-protected interactions between organizations and users. It addresses the challenges of obtaining and verifying digital credentials, enhancing control over personal data in online transactions.
		  
		  **Why It’s Needed:**
		- **Digital Transactions:** Many online transactions require individuals to provide verifiable identity claims. However, traditional methods of presenting credentials can be cumbersome and lead to privacy issues.
		- **Control of Identity:** Once a digital identity is shared, users often lose control, resulting in unwanted ads or unsolicited emails. Verified ID allows users to control how and when their digital identities are shared.
		- **Cryptographic Security & Privacy:** It ensures that digital identities are expressed in a secure, privacy-compliant, and machine-readable way, enhancing both user and organizational control.
		  
		  **How It Works:**
		- **Issuer:** An organization (e.g., government, employer, university) creates and signs digital credentials, which assert a claim about the user’s identity.
		- **User:** Receives, approves, and stores these credentials in a digital wallet. The user presents the credentials to a verifier when needed.
		- **Verifier:** Requests and verifies the credentials to ensure the claims meet specific requirements (e.g., employer, airline, or mortgage company).
		  
		  **Supporting Components:**
		- **Verifiable Data Registry:** A distributed system (e.g., blockchain) that stores metadata (including public keys) used to verify the authenticity of credentials.
		- **Credential Expiration & Revocation:** Verifiable credentials include fields for expiration or revocation, ensuring that outdated or invalid credentials are handled properly.
		  
		  **Important for SC-900:**
		- Understand the roles of Issuer, User, and Verifier in the process.
		- Know how verifiable credentials are issued, stored, and verified.
		- Be familiar with how the verifiable data registry ensures trust and security.
		- Recognize the importance of cryptographic security, privacy compliance, and control over digital identities.
		- Understand how credentials can be revoked or expire and how this is addressed in the standard.
		  
		  This information is crucial for understanding secure identity management solutions like Microsoft Entra Verified ID in the context of SC-900.
	- ^^Describe Microsoft Entra integration with Microsoft Security Copilot^^
		- **Integration Overview**:
			- Microsoft Entra integrates with Microsoft Security Copilot to provide a seamless experience for security analysts.
			- Businesses using Microsoft Security Copilot with the necessary role permissions can enable the Microsoft Entra plugin to benefit from this integration.
		- **Entra Plugin Features**:
			- When the Entra plugin is enabled, security analysts can view **risk summaries**, **remediation steps**, and **recommended guidance** for each at-risk identity.
			- Analysts can use Copilot to **streamline workflows**, such as creating and issuing user credentials and access rights.
		- **Built-in and Custom Prompts**:
			- Copilot includes **built-in prompts** for Entra capabilities, but analysts can also create their own custom prompts to support specific use cases.
		- **Embedded Experience**:
			- Integration can also be experienced through the **embedded Microsoft Copilot in Microsoft Entra**, offering a more integrated user interface.
		- **Risk Management**:
			- The **risky users' report** in the Microsoft Entra admin center, found under Identity Protection, leverages Copilot to summarize a user's risk level, offer insights, and provide **rapid mitigation recommendations**.
			  
			  Understanding these integrations and features is essential for the SC-900 exam, as it highlights how Microsoft Entra and Copilot work together to improve identity and security management through AI-driven insights.
- ## Describe core infrastructure security services in Azure
	- ^^Describe Azure distributed denial-of-service (DDoS) Protection^^
		- ### Distributed Denial of Service (DDoS) Attacks
		- **DDoS Attacks** aim to overwhelm resources (applications/servers) making them slow or unresponsive for genuine users.
		- **Types of DDoS Attacks**:
			- **Volumetric attacks**: Overwhelm bandwidth with high traffic volume, blocking legitimate traffic.
			- **Protocol attacks**: Exploit weaknesses in Layer 3 (network) and Layer 4 (transport) protocols, draining server resources.
			- **Resource/Application layer attacks**: Target web application packets to disrupt data transmission.
		- ### Azure DDoS Protection
		- Azure DDoS Protection helps **protect applications and servers** by analyzing traffic and mitigating DDoS attacks.
		- **Key Features of Azure DDoS Protection**:
			- **Always-on traffic monitoring**: Monitors traffic 24/7 for DDoS attacks and automatically mitigates them.
			- **Adaptive real-time tuning**: Learns traffic patterns and adjusts profiles for optimal protection.
			- **Telemetry, monitoring, and alerting**: Provides detailed logs through Azure Monitor for analysis and alerts.
		- **Protection Levels**:
			- **Layer 3 and Layer 4 Protection**: Focuses on the network and transport layers.
			- **Two Protection Tiers**:
				- **DDoS Network Protection**: Enhanced protection for Azure resources in virtual networks, automatically tuned for specific Azure resources, and simple to enable.
				- **DDoS IP Protection**: Pay-per-IP model with core protection features but without extras like rapid response support or discounts on Web Application Firewall (WAF).
		- **Why Azure DDoS Protection?**
			- Default infrastructure-level protection may not be enough for most applications, which can be overwhelmed by DDoS attacks despite infrastructure safeguards.
			- **Azure DDoS Protection** provides application-specific monitoring and tuning, offering more tailored protection.
		- ### Additional Protection: Web Application Firewall (WAF)
		- For protection beyond layers 3 and 4 (such as Layer 7, the application layer), you need to use a **Web Application Firewall (WAF)**, which is mentioned as part of the overall protection strategy but is covered later in the module.
		- ### Takeaways for SC-900:
		- Understand the types of DDoS attacks and the Azure DDoS Protection service, including its monitoring, protection layers, and tier options.
		- Be aware of the different tiers of Azure DDoS protection and the importance of application-specific defense for better security beyond basic infrastructure-level protection.
	- ^^Describe Azure Firewall^^
		- ### What is a Firewall?
		- A firewall monitors and controls network traffic based on security rules to protect internal networks from external threats.
		- **Azure Firewall** is a cloud-based, managed service that provides security for Azure resources.
		- ### Deployment of Azure Firewall
		- Azure Firewall can be deployed on any virtual network (VNet), but the best practice is deploying it on a **centralized virtual network**. Other networks route traffic through this central point for easier traffic management.
		- ### Key Features of Azure Firewall
		- **Stateful Firewall**: Tracks active connections and makes decisions based on the traffic's context.
		- **High Availability & Availability Zones**: Ensures minimal downtime and operates across multiple zones for resilience.
		- **Network & Application Level Filtering**: Allows filtering traffic based on IPs, ports, protocols, and application-layer protocols (e.g., HTTP/S).
		- **NAT (Source and Destination)**: Supports:
			- **SNAT**: Translates private IP to public IP for outbound traffic.
			- **DNAT**: Translates public IP to private IP for inbound traffic.
		- **Threat Intelligence**: Integrates with Microsoft's Threat Intelligence to block traffic from known malicious IPs/domains.
		- **Logging & Monitoring**: Tracks firewall activity via Azure Monitor, Log Analytics, or Event Hubs.
		- **Integration with Azure Services**: Works seamlessly with Azure Virtual Networks, Azure Policy, and Security Center.
		- ### SKUs and Integration
		- Azure Firewall comes in **Standard**, **Premium**, and **Basic** SKUs, with varying features.
		- **Security Copilot Integration**: Helps analysts use Azure Firewall logs in Microsoft Security Copilot to detect and investigate malicious traffic using natural language queries.
		- ### Important Considerations:
		- To use **Security Copilot** with Azure Firewall, you need:
			- Structured logs for intrusion detection and threat intelligence.
			- Correct RBAC roles and permissions.
			- Enabled Azure Firewall plugin in Security Copilot.
		- ### Exam Focus:
		- Understand the **centralized deployment model** and its advantages.
		- Familiarize with **key features** like stateful firewall, high availability, filtering, NAT, and threat intelligence.
		- Know how **Security Copilot** integrates with Azure Firewall for detailed traffic analysis and investigations.
		  
		  This covers essential concepts, and you should focus on the features and deployment strategies for effective protection and monitoring in Azure environments.
	- ^^Describe Web Application Firewall (WAF)^^
		- ### **Key Points:**
		- **Web Application Firewall (WAF)**:
			- **Purpose**: WAF provides centralized protection for web applications against common exploits and vulnerabilities.
			- **Benefits**:
				- Simplifies security management by centralizing protection.
				- Improves response time to security threats.
				- Allows patching known vulnerabilities in one place instead of individually securing each web application.
				- Enhances administrators' assurance of protection against threats and intrusions.
		- **Protection Against DDoS Attacks**:
			- **DDoS Protection**: While Azure DDoS Protection safeguards against DDoS attacks at the network and transport layers, Azure WAF protects against **application-layer DDoS attacks**, such as **HTTP Floods**.
			- **Purpose**: These defenses prevent attackers from affecting the availability and performance of your application.
		- **Integration with Microsoft Security Copilot**:
			- **Purpose**: Azure WAF is integrated with **Microsoft Security Copilot** for deeper investigation of security events.
			- **Features**:
				- Investigate WAF logs quickly using natural language prompts and responses.
				- Provides visibility into your environment’s threat landscape, making it easier to identify attack vectors.
			- **Configuration**: The Azure WAF plugin in Security Copilot must be turned on and configured to access these capabilities.
		- **Azure WAF Capabilities**:
			- **Prompts**: Built-in prompts help with investigating WAF logs, but custom prompts can also be entered based on supported capabilities.
		- ### **Important Concepts for SC-900** :
		- Understand how **WAF** functions to protect against vulnerabilities and attacks, particularly at the **application layer**.
		- Recognize the **integration with Microsoft Security Copilot** for enhanced threat investigation and the ability to use **natural language** for analyzing security events.
		- Differentiate between **Azure DDoS Protection** (network/transport layer) and **Azure WAF** (application layer).
	- ^^Describe network segmentation with Azure virtual networks^^
		- Network segmentation involves dividing an organization's network into smaller, isolated sections to enhance security and improve management. In a business context, this means grouping related departments together (e.g., HR, sales, customer service) to foster collaboration while maintaining separation for confidentiality.
		  
		  **Key Points:**
		- **Benefits of Network Segmentation:**
			- Group related assets supporting business operations.
			- Isolate resources to prevent unauthorized access.
			- Enforce governance policies for better control over resources.
		- **Zero Trust Model & Defense in Depth:**
			- **Zero Trust:** "Assume breach" is a principle, emphasizing the need for segmentation to contain attackers and prevent lateral movement within the network.
			- **Defense in Depth:** Network segmentation is part of a multi-layered security strategy to prevent security breaches from spreading across the entire network.
		- **Azure Virtual Network (VNet):**
			- **VNet** is Azure's private network solution, similar to traditional data center networks, but offers benefits like scalability, availability, and isolation.
			- **Segmentation in Azure VNet:** Organizations can create multiple VNets and subnets within a region and subscription. By default, there is no traffic between VNets or from the internet into a VNet unless explicitly configured.
			- **Security Control:** VNets provide network-level containment, enhancing control over how Azure resources interact with each other, the internet, and on-premises networks.
			  
			  **Key Concept for SC-900:** Understand how segmentation in Azure VNets supports security through isolation and governance, and how it aligns with Zero Trust and defense in depth strategies.
	- ^^Describe network security groups (NSGs)^^
		- ### **Overview of NSGs**
		- **NSGs** filter network traffic to and from Azure resources within a virtual network (e.g., Virtual Machines).
		- An NSG consists of **inbound** and **outbound security rules** to define traffic filtering.
		- **Key Fact**: You can only associate one NSG with each subnet or network interface (e.g., VM), but the same NSG can be applied to multiple subnets and network interfaces.
		- ### **How NSGs Work**
		- NSGs are attached to **subnets** or **VM network interfaces** to control inbound and outbound traffic.
		- Example: VM1 (higher access) has an NSG, while VM2 (public-facing) might not need one.
		- ### **NSG Security Rules**
		- NSGs are made up of **inbound** and **outbound security rules** that filter traffic based on:
			- **Source** (IP address, range, service tag, or security group)
			- **Destination**
			- **Protocol** (TCP, UDP, ICMP)
			- **Port range** (specific or range of ports)
			- **Action** (Allow or Deny)
			- **Priority**: Rules are processed in order, with lower numbers having higher priority. Once a match is found, processing stops.
		- ### **Default NSG Rules**  (Cannot be removed, but can be overridden)
		- **AllowVNetInBound**: Allows traffic from the Virtual Network to any destination within the network.
		- **AllowAzureLoadBalancerInBound**: Allows traffic from the Azure Load Balancer to any destination.
		- **DenyAllInBound**: Denies all other inbound traffic.
		- ### **Important Characteristics of NSG Rules**
		- Each rule must have a **unique name**.
		- NSG rules are evaluated in **priority order**.
		- You can specify **source/destination IPs**, **service tags**, and **application security groups** for more efficient rule creation.
		- ### **NSGs vs. Azure Firewall**
		- **NSGs** are for **distributed network layer traffic filtering** (within a virtual network or subnet).
		- **Azure Firewall** provides **centralized, stateful protection** at both network and application levels across different subscriptions and virtual networks.
		- Both work together to provide **defense-in-depth** for Azure resources.
		- ### **Exam Tips** :
		- Understand the difference between **NSGs** (distributed) and **Azure Firewall** (centralized).
		- Familiarize yourself with default rules and how to configure custom rules with specific priorities.
		- Be clear on NSG's relationship with virtual networks, subnets, and network interfaces.
		  
		  This should help in understanding how **NSGs** function and their role in securing Azure resources for the **SC-900** exam!
	- ^^Describe Azure Bastion^^
		- For the SC-900 exam, here are the key points to understand about Azure Bastion and its role in securely accessing virtual machines (VMs):
		- ### **Context**
		- **Scenario**: You have multiple virtual networks with NSGs and Azure Firewalls protecting resources like VMs. To give remote access to developers and data scientists, exposing RDP or SSH ports to the internet would increase security risks by providing entry points for attackers. Azure Bastion solves this problem.
		- ### **Azure Bastion Overview**
		- **What It Is**: Azure Bastion is a platform-managed service that provides secure and seamless RDP (Remote Desktop Protocol) and SSH (Secure Shell) connectivity to VMs **without needing a public IP address** on the VMs.
		- **How It Works**: Azure Bastion is deployed within a virtual network (VNet), and it allows you to connect to VMs in that VNet or peered VNets through the Azure portal using Transport Layer Security (TLS) for encryption. The connection is accessed via an HTML5-based web client, ensuring secure access over corporate firewalls.
		- ### **Key Benefits**
		- **Direct RDP/SSH Access via Azure Portal**: You can initiate RDP/SSH sessions with a single-click experience directly in the Azure portal.
		- **Secure Communication**: The connection is secured using **TLS**, ensuring encrypted traffic and firewall traversal for RDP/SSH.
		- **No Public IP Required**: Azure Bastion eliminates the need for VMs to have a public IP address for RDP/SSH access, reducing the exposure to potential attacks.
		- **No Need for NSG Configuration**: Azure Bastion is a fully managed service, so you don't need to apply specific NSG rules to the VMs or Bastion subnet.
		- **Protection from Port Scanning**: Since VMs do not need to expose RDP/SSH ports to the internet, they are protected from external port scanning attempts.
		- **Automatic Hardening**: Azure Bastion is always kept up to date with security patches, protecting against zero-day exploits without requiring individual VM hardening.
		- ### **Deployment**
		- **Scope**: Azure Bastion is deployed **per virtual network** (VNet), not per subscription/account or VM.
		- **Peering**: It supports virtual network peering, so once deployed, all VMs in the same or peered VNets can access Bastion for secure RDP/SSH access.
		- ### **Different SKU Tiers**
		- Azure Bastion offers different SKU tiers, each providing varying features. The exact features depend on the tier you choose.
		- ### **Exam Focus**
		- **Benefits of Azure Bastion**: Understand how it protects VMs, simplifies remote access without public IPs, and the security advantages it offers over traditional methods (exposing RDP/SSH).
		- **Deployment Model**: It's important to know that Bastion is deployed per VNet and how it supports peering.
		- **Security Features**: Focus on how Bastion ensures secure access, avoids exposing management ports, and protects against external attacks like port scanning.
		  
		  This summary should give you a strong understanding of Azure Bastion for the SC-900 exam, especially regarding security and remote access management.
	- ^^Describe Azure Key Vault^^
		- **Overview**:
		  Azure Key Vault is a cloud service that securely stores and accesses sensitive information, like passwords, API keys, certificates, and cryptographic keys.
		- **Core Features**:
			- **Secrets Management**: Store and control access to secrets like API keys and passwords.
			- **Key Management**: Create and manage encryption keys for data protection.
			- **Certificate Management**: Provision, manage, and deploy SSL/TLS certificates.
		- **Service Tiers**:
			- **Standard Tier**: Uses software-based encryption.
			- **Premium Tier**: Includes Hardware Security Module (HSM)-protected keys.
		- **Why Use Azure Key Vault?**:
			- **Centralized Storage**: Centralizes secrets and keys, preventing accidental leaks and ensuring better control over access.
			- **Secure Access**: Applications access secrets via unique URLs, reducing the need to store sensitive information in code.
			- **Object Identifiers**: URLs like `https://{vault-name}.vault.azure.net/{object-type}/{object-name}/{object-version}` for standard tier or `https://{hsm-name}.managedhsm.azure.net/{object-type}/{object-name}/{object-version}` for HSM.
		- **Security Model**:
			- **Authentication**: Performed using Microsoft Entra (formerly Azure AD).
			- **Authorization**: Managed via Azure RBAC or Key Vault access policies.
			- **Data Privacy**: Microsoft cannot access or extract your data.
		- **Monitoring and Administration**:
			- **Access Monitoring**: Enable logging to track usage and access to Key Vaults.
			- **Replication for High Availability**: Replicates data across regions for disaster recovery.
			- **Automated Tasks**: Automates certificate management tasks, such as renewal.
		- **Simplified Secrets Management**:
			- Azure Key Vault reduces administrative overhead for storing and managing secrets.
			- You can control which applications or users can access specific secrets through access policies and role-based controls.
		- **Segregation of Secrets**:
			- Create a Key Vault per application and restrict access, ensuring that each app only accesses the secrets it needs.
		- ### Summary for SC-900:
		- **Azure Key Vault** centralizes, secures, and manages sensitive data like secrets, keys, and certificates.
		- It uses **authentication and authorization** to securely control access.
		- With **role-based access control (RBAC)** and **Key Vault policies**, you can manage permissions effectively.
		- **High availability** is ensured through replication across regions.
- ## Describe security management capabilities of Azure
	- ^^Describe Microsoft Defender for Cloud^^
		- **Microsoft Defender for Cloud Overview**:
			- **Cloud-Native Application Protection Platform (CNAPP)**: A set of security practices and measures designed to protect cloud applications from cyber threats and vulnerabilities.
			- Defender for Cloud combines three core capabilities:
				- **DevSecOps**: Helps integrate security into the software development process by protecting code management environments and pipelines, and offering insights into the security posture of the development environment.
				- **Cloud Security Posture Management (CSPM)**: Assesses and monitors cloud configurations to ensure resources are secure. It alerts security teams about vulnerabilities and offers actionable insights to prevent breaches.
				- **Cloud Workload Protection Platform (CWPP)**: Protects cloud workloads, such as servers, containers, databases, and storage, from threats. It provides workload-specific security recommendations and real-time alerts on security threats.
		- **Key Features**:
			- **Defender for DevOps**: A service within Defender for Cloud that helps security teams manage DevOps security across multiple pipeline environments.
			- **CSPM**: Automatically alerts IT teams when vulnerabilities are found in cloud systems, helping prioritize actions to secure the environment.
			- **CWPP**: Provides proactive recommendations for securing workloads and real-time alerts when workloads are threatened.
		- **Security Copilot Integration**:
			- Organizations using Microsoft Security Copilot benefit from the integration with Defender for Cloud, allowing them to analyze, summarize, remediate, and delegate recommendations using natural language prompts.
		- **Microsoft Defender XDR**:
			- When Defender for Cloud is enabled, you automatically get access to **Microsoft Defender XDR**—an enterprise defense suite that coordinates detection, prevention, investigation, and response across endpoints, identities, emails, and applications to protect against sophisticated attacks.
			  
			  **Summary**:
			  Defender for Cloud secures cloud and on-premises resources through DevSecOps, CSPM, and CWPP capabilities. It integrates with Microsoft Security Copilot for enhanced threat analysis and remediation, and automatically activates Microsoft Defender XDR for comprehensive protection across your environment.
			  
			  For the exam, focus on understanding these key security pillars and how they work together to improve your organization’s overall security posture.
	- ^^Describe how security policies and initiatives improve cloud security posture^^
		- ### Key Concepts:
		- **Microsoft Defender for Cloud**: Helps manage the security of resources and workloads in both cloud and on-premises environments, aiming to improve security posture. It uses **policy definitions** and **security initiatives**.
		- **Azure Policy Definitions**: These are rules specifying security conditions that need to be controlled. Built-in definitions are available, but custom ones can also be created.
		- **Security Initiatives**: A group of Azure Policy definitions designed to achieve a specific goal. They simplify policy management by grouping related policies together.
		- **Scope of Assignment**: Policies and initiatives can be assigned to various scopes like management groups, subscriptions, resource groups, or individual resources.
		- **Security Recommendations**: Based on the policies, Defender for Cloud provides recommendations to improve security by identifying non-compliant resources.
		- ### Microsoft Cloud Security Benchmark (MCSB):
		- A Microsoft-authored set of security and compliance guidelines that provides best practices for securing workloads, data, and services in Azure and multicloud environments.
		- It’s based on industry standards like **CIS**, **NIST**, and **PCI DSS**.
		- Includes control domains like **network security**, **identity management**, **incident response**, etc.
		- Provides **Azure Guidance** for implementing security measures in Azure, as well as **AWS Guidance** for AWS environments.
		- **MCSB v1**: Lists specific recommendations (e.g., NS-1: network segmentation).
		- ### Defender for Cloud and MCSB:
		- Defender for Cloud assesses your hybrid cloud environment using the MCSB controls and provides compliance status.
		- The **regulatory compliance dashboard** reflects your status against MCSB and other standards.
		- ### Security Recommendations:
		- These are suggestions to remediate non-compliant resources found during assessments.
		- Each recommendation includes:
			- A description of the issue
			- Remediation steps
			- Affected resources
			  
			  Understanding these concepts and their interrelationships will help improve your grasp of cloud security in Azure and prepare you for the SC-900 exam.
	- ^^Describe Cloud Security Posture Management (CSPM)^^
		- ### **Key Concepts:**
		- **Cloud Security Posture Management (CSPM):**
			- CSPM is a core pillar of Microsoft Defender for Cloud that helps improve security by providing **hardening guidance** and **visibility** into your security posture.
			- CSPM enables the identification and remediation of security misconfigurations and weaknesses.
		- **Secure Score:**
			- **Secure Score** is the central feature in Defender for Cloud that reflects your current security posture.
			- It is based on assessments of cross-cloud resources for security issues, with a **higher score indicating lower risk**.
			- All customers get access to Secure Score when they enable Defender for Cloud, which uses the **Microsoft Cloud Security Benchmark (MCSB)** to generate recommendations.
		- **Hardening Recommendations:**
			- Recommendations are based on identified security vulnerabilities and are grouped into **security controls**, which represent related security tasks.
			- To improve your score, you must remediate all the recommendations within a control for a specific resource.
		- **Integration with Microsoft Security Copilot:**
			- For businesses using **Microsoft Security Copilot**, Defender for Cloud embeds Copilot capabilities to:
				- Provide context for recommendations.
				- Assist with understanding the effect of implementing recommendations.
				- Help with remediation or delegating tasks.
		- **Defender CSPM Plan Options:**
			- **Foundational CSPM** (free): Includes **asset discovery**, **continuous assessment**, **security recommendations**, **Microsoft Cloud Security Benchmark compliance**, and **Secure Score**.
			- **Advanced CSPM** (optional, paid): Adds more tools for assessing compliance with various benchmarks, regulatory standards, and custom security policies.
		- ### **Important Exam Focus:**
		- Understand the **Secure Score** and how it reflects your security posture.
		- Learn the concepts of **hardening recommendations** and **security controls**.
		- Be familiar with the **Defender CSPM plans**: the difference between **foundational (free)** and **advanced (paid)** capabilities.
		- Review the role of **Microsoft Security Copilot** in enhancing recommendations.
		  
		  These points are critical for understanding how Microsoft Defender for Cloud helps manage and improve cloud security posture.
	- ^^Describe the enhanced security of Microsoft Defender for Cloud^^
		- ### **Cloud Workload Protection**
		  
		  Cloud workload protection is essential for detecting and resolving threats to resources, workloads, and services in the cloud. Microsoft Defender for Cloud offers this protection through **Defender plans**, tailored for different types of resources in your Azure subscription.
		- ### **Microsoft Defender Plans**
		- **Defender for Servers**: Threat detection and defense for Windows and Linux machines.
		- **Defender for App Service**: Protects applications running on Azure App Service.
		- **Defender for Storage**: Detects harmful activity on Azure Storage accounts.
		- **Defender for SQL**: Secures databases and their data across environments.
		- **Defender for Kubernetes**: Provides security for Kubernetes environments, including workload and runtime protection.
		- **Defender for Container Registries**: Protects Azure Resource Manager-based container registries.
		- **Defender for Key Vault**: Advanced protection for Azure Key Vault.
		- **Defender for Resource Manager**: Monitors resource management operations in your environment.
		- **Defender for DNS**: Additional layer of protection for Azure DNS.
		- **Defender for Open-Source Relational Protections**: Security for open-source relational databases.
		  
		  These plans can be activated independently to offer comprehensive defense across compute, data, and service layers in your cloud environment.
		- ### **Enhanced Security Features**
		  
		  Microsoft Defender plans come with enhanced security features, such as:
		- **Comprehensive EDR**: Includes Microsoft Defender for Endpoint with **Microsoft Defender for Servers**.
		- **Vulnerability Scanning**: Scans for vulnerabilities in virtual machines, container registries, and SQL resources.
		- **Multicloud Security**: Extends protection to AWS and GCP, in addition to Azure.
		- **Hybrid Security**: Provides unified security for on-premises and cloud workloads, allowing continuous assessment and compliance tracking.
		- **Threat Protection Alerts**: Monitors and alerts for incoming attacks and post-breach activity.
		- **Compliance Tracking**: Monitors risk and tracks compliance with standards, including Azure Security Benchmark and industry standards.
		- **Access and Application Controls**: Use machine learning for creating allowlists/blocklists and applying just-in-time access to reduce network attack surface.
		  
		  These features enhance security through capabilities like adaptive controls, threat protection, and policy enforcement.
		- ### **Additional Features**
		- **Threat Protection**: For resources connected to the Azure environment and container security.
		- **Regulatory Compliance Dashboard**: Helps in tracking compliance with standards and regulatory requirements.
		  
		  By understanding these concepts, you'll have a solid foundation for answering questions related to cloud workload protection, security features, and Defender plans in the SC-900 exam.
	- ^^Describe DevOps security management^^
		- **DevOps**:
		- **DevOps Overview**: DevOps combines development (Dev) and operations (Ops) to enhance collaboration and streamline application planning, development, delivery, and operations. This approach enables faster deployment and efficient management of applications across pipelines and production environments.
		- **Security Challenges**: Traditional security methods did not account for the increased attack surface in DevOps environments, such as pipelines and production systems. As hackers target these areas, there is a need for improved security practices tailored to DevOps.
		- **Defender for DevOps**:
			- **Platform**: A service within Defender for Cloud designed to manage security across multi-pipeline environments (e.g., GitHub, Azure DevOps).
			- **Purpose**: Protect applications and resources from code to cloud, with visibility into the security posture of preproduction code.
			- **Key Capabilities**:
				- **Unified Visibility**: Provides a central console for security teams to view and manage the security of DevOps resources across various environments, including code, secrets, and dependency vulnerabilities.
				- **Strengthen Cloud Configurations**: Enables security of **Infrastructure as Code (IaC)** templates to avoid misconfigurations in production environments.
				- **Prioritize Remediation**: Helps prioritize critical vulnerabilities by providing insights from code to cloud. Developers are alerted to issues via **Pull Request annotations** and can be assigned remediation tasks.
		- **Managing Security Across Multi-Pipeline Environments**: Defender for DevOps unifies the security management of multiple pipelines, providing a high-level overview of security findings and allowing security teams to prioritize and remediate issues effectively.
		  
		  In essence, Defender for DevOps helps improve the security of the DevOps lifecycle, from development to deployment, ensuring that security is integrated at every stage.
- ## Describe capabilities of Microsoft Sentinel
	- ^^Define the concepts of security information and event management (SIEM) and security orchestration automated response (SOAR)^^
		- **Security Challenges**: The growing number of remote workers increases the potential for cyberattacks and security breaches, creating the need for robust security solutions.
		- **SIEM (Security Information and Event Management)**:
			- **Purpose**: SIEM tools collect and analyze data across an organization's estate (including infrastructure, software, and resources).
			- **Functionality**: They detect correlations, anomalies, and generate alerts or incidents, helping identify potential security threats.
		- **SOAR (Security Orchestration, Automation, and Response)**:
			- **Purpose**: SOAR tools automate security tasks in response to alerts.
			- **Functionality**: They integrate with SIEM systems to trigger automated workflows that mitigate security issues, enhancing response speed and reducing manual intervention.
		- **Comprehensive Security Approach**: Organizations should use a solution that combines both SIEM and SOAR to enhance threat visibility, automate responses, and improve overall security.
		  
		  In summary, SIEM focuses on collecting and analyzing security data, while SOAR automates responses to detected threats. Together, they provide a comprehensive, proactive security strategy for organizations.
	- ^^Describe threat detection and mitigation capabilities in Microsoft Sentinel^^
		- ### **1.  Microsoft Sentinel Overview:**
		- **Purpose**: Provides intelligent security analytics and threat intelligence for enterprise-wide threat detection, investigation, and response.
		- **Core Functions**: Collect, detect, investigate, and respond to security incidents.
		- ### 2.  **Key Functional Areas:**
		- **Collect**:
			- **Data Sources**: Collect data from users, devices, apps, infrastructure (both on-premises and in the cloud).
			- **Connectors**: Out-of-the-box and custom connectors, supporting various formats like Syslog and REST API.
			- **Data Normalization**: Uses the Advanced Security Information Model (ASIM) to standardize data for easier correlation.
		- **Detect**:
			- **Analytics**: Uses built-in analytic rules to detect threats and create incidents.
			- **MITRE ATT&CK Framework**: Provides mapping of adversary tactics and techniques.
			- **Threat Intelligence**: Integrates threat intelligence sources to help detect malicious activities.
			- **Watchlists**: Customizable lists (e.g., high-value assets, terminated employees) to enhance detection.
		- **Investigate**:
			- **Incidents**: Aggregated alerts for investigation, helping to understand and resolve potential threats.
			- **Hunts**: Enables proactive searches for threats before alerts are triggered, based on the MITRE framework.
			- **Notebooks**: Jupyter notebooks for advanced analytics, visualizations, and integrations outside of Sentinel.
		- **Respond**:
			- **Automation**: Uses **Automation rules** and **Playbooks** (based on Azure Logic Apps) to automate responses to security incidents.
			- **Orchestration**: Simplifies workflows and integrates with external systems (e.g., ServiceNow) for incident resolution.
		- ### 3.  **Security Operations Center (SOC) Support** :
		- Sentinel helps modernize SOCs by offering end-to-end capabilities for data collection, detection, investigation, and rapid response through automated workflows and built-in integrations.
		- ### 4.  **Microsoft Sentinel Content Hub** :
		- **Content**: Includes data connectors, analytics rules, workbooks, playbooks, and more.
		- **Solutions**: Pre-packaged content specific to industry or domain use cases, available for easy deployment.
		- ### 5.  **Integration with Microsoft Defender** :
		- Sentinel can be accessed through the **Azure portal** or the **Microsoft Defender portal**, unifying incident management, advanced hunting, and threat response capabilities.
		- ### Exam Focus:
		- Understand **how Sentinel collects and normalizes data**, **detects threats using analytics and MITRE ATT&CK**, and **automates responses** using playbooks.
		- Familiarize yourself with **integrations and connectors** and how they contribute to an organization’s overall security posture.
		- Learn the **role of automation and orchestration** in accelerating incident response.
		  
		  This should give you a solid understanding of Microsoft Sentinel’s key capabilities for the SC-900 exam.
	- ^^Describe Microsoft Sentinel integration with Microsoft Security Copilot^^
		- **Microsoft Sentinel Integration with Copilot**:
			- For businesses using **Microsoft Security Copilot**, integration with Sentinel is enabled through plugins in the Copilot portal. There are two main plugins:
				- **Microsoft Sentinel (Preview)** plugin.
				- **Natural Language to KQL for Microsoft Sentinel (Preview)** plugin.
		- **Permissions and Configuration**:
			- To use the Sentinel plugin, users must be assigned roles granting access to both Copilot and Sentinel, like **Microsoft Sentinel Reader**.
			- The plugin requires configuring the Sentinel workspace, subscription name, and resource group.
		- **Capabilities of the Sentinel Plugin**:
			- Focused on **incidents** and **workspaces**, with built-in prompts for incident investigation.
			- Includes a **promptbook** for Sentinel incident investigation, which helps generate effective prompts and gather detailed reports (e.g., incidents, alerts, reputation scores, users, and devices).
		- **Natural Language to KQL Plugin**:
			- Converts natural language queries into **KQL (Kusto Query Language)** queries for **threat hunting** in Sentinel. This saves time for security teams by automating the query generation process.
		- **Microsoft Sentinel in Defender**:
			- The integration can be experienced through both a **standalone** and **embedded** experience in the **Defender portal**.
			- **Unified Incidents**: Sentinel and Defender XDR incidents are merged, allowing users to access incident summaries, guided responses, and reports through Copilot in the Defender portal.
			  
			  This integration streamlines incident investigation, query generation, and response management by leveraging natural language and automated tools.
- ## Describe threat protection with Microsoft Defender XDR
	- ^^Describe Microsoft Defender XDR services^^
		- ### **Microsoft Defender XDR Overview**
		- **Microsoft Defender XDR** is a comprehensive security suite that helps protect organizations from advanced cyberattacks.
		- It provides **endpoint, application, email, and identity protection**, allowing admins to assess threats and take automated action to stop attacks.
		- ### **Key Components of Microsoft Defender XDR:**
		- **Microsoft Defender for Endpoint**:
			- Unified platform for **preventive protection**, **post-breach detection**, **automated investigation**, and **response**.
		- **Defender Vulnerability Management**:
			- Provides continuous **asset visibility**, **risk assessments**, and **remediation tools** to prioritize and address critical vulnerabilities.
		- **Microsoft Defender for Office 365**:
			- Protects against malicious threats in **email**, **links (URLs)**, and **collaboration tools** (e.g., Teams, SharePoint).
		- **Microsoft Defender for Identity**:
			- Detects and investigates threats using **Active Directory** signals, identifying compromised identities and insider threats.
		- **Microsoft Defender for Cloud Apps**:
			- Protects **SaaS applications** with deep visibility, strong data controls, and enhanced threat protection.
		- ### **Integration with Other Microsoft Tools:**
		- **Microsoft Defender XDR integrates with Microsoft Security Copilot**, providing advanced insights into threats.
		- It aggregates threat data from **Microsoft Sentinel**, **Microsoft Defender for Cloud**, and **Microsoft Threat Intelligence (TI)** to enhance security workflows like **incident response**, **threat hunting**, and **vulnerability management**.
		- ### **Centralized in the Microsoft Defender Portal** :
		- All solutions are accessible through a **unified security operations platform** (Microsoft Defender portal).
		- This portal centralizes insights from the Defender suite and other Microsoft security products.
		  
		  ---
		  This overview helps highlight the **core components** of Microsoft Defender XDR, its **integrations**, and its role in comprehensive threat protection, which will be important for your **SC-900** certification.
	- ^^Describe Microsoft Defender for Office 365^^
		- Microsoft Defender for Office 365 is a comprehensive security solution that integrates with Office 365 to protect against threats like phishing, malware, and email-based attacks. It's available in two plans: **Plan 1** and **Plan 2**. The key features of Defender for Office 365 are categorized into three main security areas:
		- ### 1.  **Preventing and Detecting Threats**
		- **Anti-malware, Anti-spam, Anti-phishing Policies**: Protects against malicious emails.
		- **Safe Attachments**: Scans email attachments in a virtual environment to detect malware.
		- **Quarantine Policies**: Manages quarantined emails for user review.
		- **Outbound Spam Filtering**: Detects and handles outgoing spam.
		- **Connection Filtering**: Identifies trusted or malicious email servers by IP.
		- **Simulated Attack Training**: Helps users recognize phishing attacks before they happen.
		- **SIEM Integration**: Allows security teams to integrate with Security Information and Event Management (SIEM) systems.
		- ### 2.  **Investigating Threats**
		- **Audit Log Search**: Admins can search activity logs to investigate potential threats.
		- **Message Trace**: Tracks the status of email messages and actions taken on them.
		- **Explorer/Threat Explorer**: Provides real-time detections and allows automated investigation processes for detected threats.
		- **URL Trace**: Investigates domain communications to detect malicious activity.
		- **Campaigns**: Detects coordinated phishing and malware attacks across the organization.
		- **Reports and Threat Trackers**: Helps teams monitor trends and investigate specific threats.
		- ### 3.  **Responding to Threats**
		- **Zero-hour Auto Purge (ZAP)**: Retroactively removes malicious emails from mailboxes.
		- **Automated Investigation and Response (AIR)**: Automates response processes for common threats.
		- **SIEM Integration for Automated Responses**: Provides automatic threat mitigation actions based on detected events.
		- ### **Microsoft Defender Portal**
		- The **Defender Portal** is the central location for managing security across your Microsoft environment.
		- It offers tools for:
			- **Incident Management**: View and remediate security incidents.
			- **Explorer**: Investigate and respond to threats in emails and documents.
			- **Campaigns**: Analyze phishing or malware campaigns.
			- **Attack Simulation Training**: Build user resilience against attacks.
			- **Policies & Rules**: Set security policies for emails and collaboration tools.
		- ### **Important Tools**
		- **Investigation Tools**: Automated investigation, message trace, and threat explorer.
		- **Threat Response**: ZAP and AIR for automatic threat mitigation.
		- **Training Tools**: Attack simulation to improve user awareness.
		  
		  These capabilities are designed to enhance the security posture of organizations by preventing, detecting, investigating, and responding to threats within Microsoft 365 environments.
	- ^^Describe Microsoft Defender for Endpoint^^
		- ### **Overview of Microsoft Defender for Endpoint:**
		- **Purpose:** Protects enterprise networks, including endpoints like laptops, phones, tablets, PCs, routers, and firewalls by preventing, detecting, investigating, and responding to advanced threats.
		- **Key Components:**
			- **Endpoint Behavioral Sensors:** Embedded in Windows 10 and later, these sensors collect and process signals from the operating system.
			- **Cloud Security Analytics:** Processes signals into insights, detections, and recommended responses to threats.
			- **Threat Intelligence:** Detects attacker tools, techniques, and procedures, providing alerts on suspicious activities.
		- ### **Key Features:**
		- **Core Defender Vulnerability Management:**
			- **Risk-based approach** to discovering, assessing, prioritizing, and remediating endpoint vulnerabilities and misconfigurations.
		- **Attack Surface Reduction:**
			- Provides initial defense by ensuring proper configurations and applying exploit mitigations. Includes network and web protection to block malicious IPs, domains, and URLs.
		- **Next-Generation Protection:**
			- Includes heuristic, behavior-based, and real-time antivirus protection, alongside **cloud-delivered protection** for fast detection of emerging threats.
			- Ensures regular updates to Microsoft Defender Antivirus.
		- **Endpoint Detection and Response (EDR):**
			- Detects advanced attacks in near real-time and provides actionable alerts for security analysts to prioritize and respond to breaches.
		- **Automated Investigation and Remediation (AIR):**
			- Uses algorithms to inspect alerts and take immediate action, reducing alert volume and allowing security teams to focus on more complex threats.
		- **Microsoft Secure Score for Devices:**
			- Provides a dynamic assessment of device security, offering insights and actions to improve organizational security.
		- **Microsoft Threat Experts:**
			- A managed service offering proactive threat hunting, prioritization, and additional insights to enhance SOC operations.
		- **Management and APIs:**
			- Offers an API model for automating workflows and integrating with other Microsoft services, including **Microsoft Entra ID** for authentication and authorization.
		- ### **Defender for Endpoint Plans:**
		- **Plan 1 and Plan 2** offer different levels of protection and capabilities (specifics available in the Compare Microsoft Defender for Endpoint plans document).
		- ### **Experience via Microsoft Defender Portal:**
		- **Centralized Management:** The portal provides a hub for security tasks across identities, data, devices, apps, and infrastructure.
		- **Endpoints Node** (in the portal) allows you to manage vulnerabilities, connected applications, APIs, and configuration settings.
		- **Vulnerability Management:** Dashboard for managing device vulnerabilities, tracking weaknesses, and taking remediation actions.
		- ### **Additional Features in the Defender Portal:**
		- **Incidents and Alerts**: Monitoring and alert management for security issues.
		- **API Explorer**: Allows testing and interaction with Defender for Endpoint’s APIs for custom workflows.
		- **Configuration Management**: Helps define endpoint policies and track deployment progress.
		- ### **Takeaways for SC-900:**
		- Microsoft Defender for Endpoint is a **comprehensive solution** for endpoint protection, integrating behavioral sensors, cloud analytics, and threat intelligence to safeguard devices.
		- The portal is central to managing security, with key areas like vulnerability management, connected applications, and configuration management.
		- Understanding **Plan 1 and Plan 2** differences, as well as how to use Defender for Endpoint’s features (vulnerability management, automated investigation, and response) will be essential for the exam.
		  
		  Focus on the integration with other Microsoft Defender solutions and how it fits into broader security management across devices and applications.
	- ^^Describe Microsoft Defender for Cloud Apps^^
		- ### 1.  **Microsoft Defender for Cloud Apps Overview**
		- **Purpose:** Protects SaaS applications and their data across cloud environments.
		- **Challenges:** Protecting SaaS apps becomes difficult as they expand, and employees access them outside corporate perimeters, introducing new risks.
		- **Key Functions:** It goes beyond traditional CASBs to offer advanced features like threat protection and governance.
		- ### 2.  **Key Features of Defender for Cloud Apps**
		- **Cloud Access Security Broker (CASB) Functionality:**
			- Acts as a gatekeeper between users and cloud resources.
			- Features include discovery of cloud app usage, threat protection, information protection, and compliance monitoring.
		- **SaaS Security Posture Management (SSPM):**
			- Helps improve security by recommending actions to address misconfigurations and improve posture, based on industry standards.
			- Integrates with **Microsoft Secure Score** for connected apps.
		- **Advanced Threat Protection:**
			- Part of Microsoft XDR for detecting and responding to attacks across the full attack chain (email, endpoint, identity, app data).
			- Uses **User and Entity Behavior Analysis (UEBA)** and **Adaptive Access Control (AAC)** to mitigate attacks.
		- **App-to-App Protection (App Governance):**
			- Protects OAuth-enabled apps by monitoring permissions and inter-app data exchange.
			- Ensures app hygiene by tracking app usage and credentials.
		- ### 3.  **SaaS Application Discovery and Monitoring**
		- **Discover and Identify SaaS Apps:**
			- Defender for Cloud Apps monitors network traffic to identify apps used by employees.
		- **Evaluate App Security:**
			- It assesses over 90 risk indicators for discovered apps, providing insights into potential security risks.
		- **Manage and Control Usage:**
			- Security teams can set policies to monitor app activity and be alerted to unusual behavior.
		- ### 4.  **Information Protection**
		- **Data Scanning and Protection:**
			- Defender scans SaaS apps for sensitive data, allowing you to track where data is stored and who accesses it.
			- Controls include applying sensitivity labels, blocking downloads to unmanaged devices, and removing external collaborators.
		- **Integration with Microsoft Purview and DLP:**
			- Leverages data classification and data loss protection (DLP) to secure sensitive data.
		- ### 5.  **Integration with Microsoft Defender Portal**
		- **Access Through the Defender Portal:**
			- The Defender portal centralizes monitoring and management of security across identities, data, devices, apps, and infrastructure.
		- **Core Features in the Portal:**
			- **Cloud Discovery**: Identifies cloud app usage.
			- **App Governance**: Manages OAuth apps and credentials.
			- **Policies**: Configures security policies.
			- **Activity and Governance Logs**: Track app activities and security actions.
		- ### Key Takeaways for SC-900:
		- Understand the role of **CASBs**, **SSPM**, and **XDR** in securing SaaS apps.
		- Know how **Defender for Cloud Apps** helps organizations discover, assess, and manage risks in their SaaS environment.
		- Recognize the importance of **app-to-app protection** and OAuth security.
		- Familiarize yourself with the **Defender portal** and its key features for app discovery, governance, and policy configuration.
		  
		  These concepts will help ensure you're well-prepared for questions related to securing SaaS applications and using Microsoft Defender for Cloud Apps on the SC-900 exam.
	- ^^Describe Microsoft Defender for Identity^^
		- ### Overview:
		- **Microsoft Defender for Identity** is a cloud-based security solution that helps detect threats, such as privilege escalation or lateral movement, by analyzing signals from on-premises identity infrastructure servers (domain controllers, Active Directory Federated Services, and Certificate Services).
		- ### Key Features:
		- **Sensors and Data Flow**:
			- Software sensors are installed on on-premises identity servers.
			- Sensors access event logs, parse them, and send relevant information to the cloud service for analysis.
		- **Core Capabilities**:
			- **Prevent breaches**: Proactively assesses identity security posture to identify risks before they are exploited.
			- **Detect threats**: Uses real-time analytics to monitor user activity, permissions, and network behavior for suspicious activities.
			- **Investigate activities**: Provides actionable incident information through clear attack timelines.
			- **Respond to attacks**: Automatically takes action (e.g., disabling compromised accounts) to protect identities.
		- ### Detailed Functionality:
		- **Proactive Security Assessment**:
			- Continuously monitors for sensitive accounts and risky lateral movement paths, reporting issues to help improve security posture.
			- Integration with **Microsoft Secure Score** for deeper insights into security policy improvements.
		- **Threat Detection**:
			- Identifies anomalies in user activities using built-in intelligence, such as failed logins, unauthorized group memberships, and credential compromises.
			- Tracks activities throughout the attack lifecycle:
				- **Reconnaissance**: Rogue users attempting to gain information.
				- **Compromised credentials**: Brute force or failed authentication attempts.
				- **Lateral movements**: Attackers attempting to expand their control within the network.
				- **Domain dominance**: When attackers gain control of Active Directory.
		- **Investigation & Alerts**:
			- Alerts are tailored to focus on the most critical threats.
			- **Attack timeline view** allows security teams to investigate suspicious events quickly, providing insights into user activities, devices, and network resources.
		- **Remediation**:
			- Allows security teams to take direct action, such as:
				- **Disabling users**: Prevents compromised accounts from signing in.
				- **Password reset**: Forces a user to change their password to stop impersonation attempts.
		- ### Interface and Integration:
		- **Microsoft Defender Portal** is used to manage Defender for Identity.
			- The **Dashboard** provides real-time data on identity threat detection and response.
			- The **Health Issues** page alerts users to problems with deployment or sensors.
			- **Tools Page** includes readiness scripts and PowerShell modules for environment configuration.
		- ### Key Takeaways for SC-900:
		- **Defender for Identity** plays a crucial role in hybrid environments by helping to identify, detect, and respond to identity-based threats.
		- It integrates with Microsoft Defender XDR for comprehensive threat detection, covering endpoints, Office 365, and cloud apps.
		- The Defender portal offers a unified interface to monitor, investigate, and manage identity threats.
		  
		  Understanding these points will help you grasp the role of Microsoft Defender for Identity in securing hybrid environments and its integration within the broader Microsoft security ecosystem.
	- ^^Describe Microsoft Defender Vulnerability Management^^
		- ### **Key Functions:**
		- **Continuous Discovery and Monitoring**:
			- Uses built-in and agentless scanners to detect risks even when devices aren't connected to the corporate network.
			- Provides a real-time view of assets like software applications, digital certificates, hardware, and network shares.
			- Examples of assessments include software inventory, browser extension security, digital certificate expiry, and network share configurations.
		- **Risk-based Intelligent Prioritization**:
			- Leverages Microsoft's threat intelligence to prioritize vulnerabilities based on factors like breach likelihood, emerging threats, and the criticality of assets.
			- Helps identify the biggest vulnerabilities, particularly those exploited in the wild, and protects high-value assets.
			- Uses Common Vulnerabilities and Exposures (CVEs) and real-time device assessments to guide remediation.
		- **Remediation and Tracking**:
			- Collaborates with IT and security admins to resolve issues through built-in workflows.
			- Enables actions like creating remediation tasks in Microsoft Intune, blocking vulnerable applications, and tracking remediation progress.
			- Provides alternate mitigations, such as configuration changes, to reduce vulnerability risks.
		- ### **Microsoft Defender Portal** :
		- The **Defender Vulnerability Management** section is under **Endpoints** in the left navigation panel.
		- **Dashboard**: Displays key metrics such as exposure score, top security recommendations, and vulnerability remediation status.
		- **Recommendations**: Lists weaknesses, vulnerabilities, and security insights, along with devices exposed to threats.
		- **Inventories**: Provides an inventory of installed software, vulnerabilities, and threats related to them.
		- **Weaknesses**: Lists CVEs and their associated risks (severity, CVSS score, threat insights).
		- **Event Timeline**: Tracks how new vulnerabilities or exploits impact organizational risk.
		- **Baselines Assessment**: Custom security profiles to monitor endpoints against industry security benchmarks.
		- ### **Important Concepts for the SC-900 Exam** :
		- **Vulnerability Management**: The process of identifying, assessing, prioritizing, and remediating vulnerabilities within an organization's assets.
		- **Exposure Score and Secure Score**: Metrics that help measure the security posture of devices in your organization.
		- **Common Vulnerabilities and Exposures (CVEs)**: Standard identifiers for vulnerabilities and exposures, used in risk prioritization and mitigation.
		- **Remediation Workflows**: Processes for fixing vulnerabilities, including automatic blocking of risky applications and creating tasks in Microsoft Intune.
		  
		  By focusing on these aspects, you'll be better equipped to understand Microsoft Defender Vulnerability Management and how it helps secure an organization’s infrastructure.
	- ^^Describe Microsoft Defender Threat Intelligence (Defender TI)^^
		- ### Key Features of Microsoft Defender Threat Intelligence:
		- **Threat Analytics**:
			- **Purpose**: Helps analysts understand how emerging threats impact their organization's environment.
			- **Reports**: Provide threat analysis, guidance for defense, and data from the organization's network to indicate active threats and protections.
			- **Dashboard**: Displays the most relevant reports, divided into three categories:
				- *Latest threats*: Recently published or updated reports.
				- *High-impact threats*: Those with the most active/resolved alerts.
				- *Highest exposure*: Threats your organization is most exposed to, based on severity and the number of vulnerable devices.
		- **Intel Profiles**:
			- Provides knowledge on threat actors, malicious tools, and vulnerabilities.
			- Continuously updated by Microsoft experts to provide actionable context.
		- **Intel Explorer**:
			- Allows analysts to quickly scan for featured articles and search using keywords, indicators, or CVE IDs.
			- Includes *Vulnerability Articles* linked to CVEs to provide actionable intelligence.
		- **Intel Projects**:
			- Analysts can create projects to organize Indicators of Interest (IOIs) and Indicators of Compromise (IOCs) from investigations.
			- Tracks history, collaborators, and monitoring profiles.
		- **Microsoft Defender Portal**:
			- Defender TI is accessed through the **Threat Intelligence** node in the Microsoft Defender portal.
			- Features accessible include Threat Analytics, Intel Profiles, Intel Explorer, and Projects.
		- **Microsoft Security Copilot Integration**:
			- Integrates with Defender TI to deliver insights on threat activity groups, IOCs, tools, and contextual intelligence.
			- Built-in prompts and custom prompts assist analysts with investigations, threat intelligence enrichment, and incident response.
			- Offers **Vulnerability Impact Assessment** and **Threat Actor Profiles** for specific guidance.
		- ### Important Concepts for the SC-900 Exam:
		- **Threat Intelligence**: The process of gathering, analyzing, and acting upon information about potential and existing threats.
		- **CVE (Common Vulnerabilities and Exposures)**: Standardized identifiers for vulnerabilities that analysts use to correlate threats with specific weaknesses in software or systems.
		- **Indicators of Compromise (IOCs)**: Pieces of evidence that suggest a security breach or malicious activity has occurred.
		- **Collaboration**: The ability to collaborate with fellow users within the Microsoft Defender TI environment to investigate and respond to threats.
		  
		  Understanding these features and how they integrate into Microsoft's broader security ecosystem will be crucial for the SC-900 exam, especially for sections related to threat intelligence and incident response.
	- ^^Describe the Microsoft Defender portal^^
		- ### Unified Security Operations Platform
		- **Microsoft Defender Portal**: A centralized platform for managing security operations, providing tools for prevention, detection, investigation, and response to threats across environments.
		- Combines SIEM, XDR, posture management, and threat intelligence with advanced generative AI.
		- Accessible by roles like Global Administrator, Security Administrator, Security Operator, or Security Reader in Microsoft Entra ID.
		- ### Key Features of Microsoft Defender Portal
		- **Role-Based Access Control**: Users see tailored cards based on their roles. This allows different roles to focus on relevant security tasks.
		- **Customization**: Navigation can be customized to fit individual preferences.
		- **Exposure Management**: Provides a unified view of security posture across assets and workloads, helping to manage attack surfaces and mitigate exposure risks.
		- **Secure Score**: A representation of an organization’s security posture, offering recommendations to improve security and comparing scores with other organizations.
		- ### Investigation & Response
		- **Incidents and Alerts**: Incidents group related alerts, assets, investigations, and evidence for a comprehensive view of an attack. It helps track actions, assets involved, and the full story of the attack.
		- **Advanced Hunting**: A query-based tool (using Kusto Query Language, KQL) to explore up to 30 days of raw data from Microsoft Defender and Microsoft Sentinel, helping detect potential threats.
		- **Actions & Submissions**: Tracks remediation actions and allows admins to submit items (like emails) for Microsoft’s analysis.
		- **Partner Catalog**: Lists third-party services that enhance detection and investigation capabilities.
		- ### Threat Intelligence & Assets
		- **Threat Intelligence**: Provides access to Microsoft Defender Threat Intelligence to stay informed about emerging threats.
		- **Asset Management**: Offers detailed views of protected and discovered assets, including devices and identities, helping to identify at-risk assets.
		- ### Integrations with Other Microsoft Services
		- **Microsoft Sentinel**: Works alongside Defender for incidents and alerts, offering additional features for threat detection.
		- **Microsoft Defender for Identity, Endpoints, Office 365, Cloud Apps**: Specific sections dedicated to securing identities, endpoints, emails, and cloud apps within the organization.
		- ### SOC Optimization & Reporting
		- **SOC Optimization**: Focuses on optimizing security controls and enhancing security outcomes over time.
		- **Reports**: Unified reporting interface that covers different workloads (endpoints, email, cloud apps, etc.).
		- ### Additional Features
		- **Learning Hub**: Access training courses, documentation, and tutorials via Microsoft Learn.
		- **System Configuration**: Manage permissions, service health, and other settings in the portal.
		  
		  For the SC-900 exam, understanding these tools, integrations, and workflows in the Defender portal will be essential for managing security effectively in a Microsoft environment.
	- ^^Describe Copilot integration with Microsoft Defender XDR^^
		- ### 1.  **Standalone Experience**  (via Copilot Portal)
		- **Plugins**: There are two plugins for integration with Microsoft Defender XDR:
			- **Microsoft Defender XDR**: Enables file analysis, incident reporting, guided responses, and security state summaries.
			- **Natural Language to KQL for Microsoft Defender**: Converts natural language queries (e.g., "Give me all devices that signed in in the last 10 minutes") into Kusto Query Language (KQL) queries for threat hunting.
		- **Capabilites**:
			- Analyze files, generate reports, summarize incidents, and list alerts.
			- Pre-built prompts and a promptbook for incident investigation are available.
		- ### 2.  **Embedded Experience**  (within Defender XDR Portal)
		- **Features**:
			- **Incident Summaries**: Automatic overviews of incidents, including timelines and affected assets.
			- **Guided Responses**: AI-driven response actions, including triage, containment, investigation, and remediation, tailored to incidents like phishing, ransomware, etc.
			- **Script Analysis**: Analyze malicious or benign scripts directly within Defender XDR, reducing the need for external tools.
			- **Natural Language to KQL Queries**: Similar to the standalone experience, users can create KQL queries using natural language in advanced hunting.
			- **Incident Reports**: Automatically generate detailed incident reports from multiple data sources, including analyst actions and automated responses.
			- **File Analysis**: Identify suspicious files through AI-powered analysis.
			- **Device and Identity Summaries**: Get security posture and unusual behavior details of devices and identities.
		- ### 3.  **Seamless Transition Between Experiences** :
		- Analysts can transition from the embedded experience to the standalone experience to perform more in-depth investigations.
		- ### Key Takeaways for SC-900:
		- Understand the difference between the **standalone** (through the Copilot portal) and **embedded** (within Defender XDR) experiences.
		- Familiarize yourself with the features such as **incident summaries**, **guided responses**, and **KQL query generation**.
		- Recognize the AI-driven capabilities like script analysis and natural language querying to support security operations.
		  
		  By focusing on these features, you'll better grasp how Security Copilot integrates with Defender XDR to assist security teams in incident investigation and response.
- ## Describe Microsoft Service Trust Portal and privacy principles
	- ^^Describe the Service Trust Portal offerings^^
		- ### 1.  **Overview of the Service Trust Portal**
		- The STP provides resources related to how Microsoft cloud services protect data and help manage compliance.
		- It includes **audit reports**, **whitepapers**, and **guides** created by Microsoft or external auditors.
		- ### 2.  **Accessing the STP**
		- To access certain resources, you need a **Microsoft cloud services account** (via Microsoft Entra) and must agree to the **non-disclosure agreement** for compliance materials.
		- ### 3.  **Content Categories in the STP**
		  
		  The STP is divided into several key sections:
		- **Certifications, Regulations, and Standards**: Provides details on security practices and how Microsoft’s services meet regulatory compliance standards (e.g., ISO/IEC).
		- **Reports, Whitepapers, and Artifacts**: Includes documents on Business Continuity and Disaster Recovery (BCP/DR), Penetration Tests, Privacy and Data Protection, and FAQs.
		- **Industry and Regional Resources**: Contains documents specific to industries (e.g., Financial Services, Healthcare) and regions (e.g., US Government, various regional compliance documents).
		- **Resources for Your Organization**: Offers content based on your organization’s subscription and permissions.
		- ### 4.  **My Library Feature**
		- Users can add relevant documents to their **My Library** for quick access.
		- You can set up **notifications** to stay informed about updates to these documents.
		- ### Key Takeaways for SC-900 Exam:
		- Focus on the **structure of the Service Trust Portal** and its categories (Certifications, Regulations, etc.).
		- Understand the importance of **compliance-related documents** (e.g., audit reports, whitepapers) in managing cloud security.
		- Remember the **access requirements** and features like the My Library and notification settings.
		  
		  Familiarizing yourself with these concepts will help you answer questions related to Microsoft's compliance and security practices on the exam.
	- ^^Describe the privacy principles of Microsoft^^
		- **Control**: Microsoft puts customers in control of their data. You can access, modify, or delete your data anytime, and Microsoft only uses your data with your consent for the services you've selected. They comply with privacy laws and standards.
		- **Transparency**: Microsoft is transparent about data collection and usage. Data is processed according to the customer's agreement, and subcontractors must follow the same privacy rules. A list of approved subprocessors is available through the Service Trust Portal.
		- **Security**: Microsoft ensures data security using strong encryption for both data at rest and in transit. Technologies like Azure Key Vault help secure and manage encryption keys and secrets.
		- **Strong Legal Protections**: Microsoft adheres to local privacy laws and defends privacy as a human right. They don’t allow direct government access to your data without your consent, except when required by law. Requests for customer data are scrutinized, and customers are notified unless legally prohibited.
		- **No Content-Based Targeting**: Microsoft doesn't use customer data for targeted advertising or share it with advertisers. They don't mine email, chat, or personal content for marketing purposes.
		- **Benefits to You**: Data collected by Microsoft is used to improve services, troubleshoot issues, enhance features, and provide personalized experiences.
		  
		  These principles ensure that Microsoft products and services are designed with privacy, security, and compliance in mind, reinforcing trust in their offerings.
	- ^^Describe Microsoft Priva^^
		- **Privacy by Default**: Organizations must adopt a "privacy by default" approach to meet regulations and build customer trust. Microsoft Priva offers comprehensive privacy solutions to streamline privacy operations and mitigate risks across an organization's data landscape.
		- **Key Priva Solutions**:
		- **Subject Rights Requests**: Helps organizations manage requests from individuals (data subjects) to access, review, or manage their personal data.
		- **Privacy Risk Management**: Allows organizations to set policies to identify privacy risks, such as data overexposure, data transfers, and stored data minimization. Policies help remediate issues and ensure data security.
		- **Consent Management**: Provides customizable consent models for managing user consent across regions and platforms. Supports different languages and regions for compliance.
		- **Privacy Assessments**: Automates the discovery and evaluation of personal data usage, helping organizations keep privacy assessments up-to-date and comply with regulations.
		- **Tracker Scanning**: Automates the identification and management of web tracking technologies to ensure compliance with privacy regulations regarding web trackers.
		- **Priva Portal**: A unified portal providing a single-entry point for managing all Priva solutions, including settings, roles, and permissions. This portal simplifies privacy operations and is distinct from the older Microsoft Purview compliance portal.
- ## Describe compliance management capabilities of Microsoft Purview
	- Describe the Microsoft Purview compliance portal
	- Describe Compliance Manager
	- Describe the uses and benefits of compliance score
- ## Describe information protection, data lifecycle management, and data governance capabilities of Microsoft Purview
	- Describe the data classification capabilities
	- Describe the benefits of Content explorer and Activity explorer
	- Describe sensitivity labels and sensitivity label policies
	- Describe data loss prevention (DLP)
	- Describe records management
	- Describe retention policies, retention labels, and retention label policies
	- Describe unified data governance solutions in Microsoft Purview
- ## Describe insider risk, eDiscovery, and audit capabilities in Microsoft Purview
	- Describe insider risk management
	- Describe eDiscovery solutions in Microsoft Purview
	- Describe audit solutions in Microsoft Purview