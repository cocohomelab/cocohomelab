### IAM (Identity and Access Management)

IAM (Identity and Access Management) is the framework of policies, processes, and technologies that ensures the right individuals have the right access to the right resources at the right time.

#### PAM (Privileged Access Management)

PAM (Privileged Access Management) is a subset of IAM (Identity and Access Management) focused on securing, controlling, and monitoring accounts with elevated privileges—such as admin, root, or service accounts.

` IAM and PAM both integrate with Active Directory. IAM uses AD to manage and authenticate users, while PAM uses AD to secure and control privileged accounts.`

` “IAM and PAM both integrate with Active Directory—IAM manages and authenticates regular users using AD, while PAM secures privileged AD accounts such as Domain Admins with vaulting, monitoring, and just-in-time access.”`


Difference Between IAM and PAM
| IAM                                    | PAM                                                            |
| -------------------------------------- | -------------------------------------------------------------- |
| Manages all identities and access      | Focuses on **privileged accounts**                             |
| Examples: employee login, app accounts | Examples: root, domain admin, DB admin                         |
| General access control                 | Enhanced security controls (vaulting, JIT, session monitoring) |


IAM examples : Azure AD, Okta, AWS IAM, Google Workspace IAM

PAM examples : CyberArk, BeyondTrust, Azure PIM,AWS IAM Roles (temporary elevation)

### IGA (Identity Governance and Administration)


Troubleshooting

CyberArk
- Check user in Vault & Safe
- Check user in AD group
