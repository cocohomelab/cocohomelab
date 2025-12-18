### IAM (Identity and Access Management)

IAM (Identity and Access Management) is the framework of policies, processes, and technologies that ensures the right individuals have the right access to the right resources at the right time.

### PAM (Privileged Access Management)

PAM (Privileged Access Management) is a subset of IAM (Identity and Access Management) focused on securing, controlling, and monitoring accounts with elevated privileges—such as admin, root, or service accounts.

` IAM and PAM both integrate with Active Directory. IAM uses AD to manage and authenticate users, while PAM uses AD to secure and control privileged accounts.`

` “IAM and PAM both integrate with Active Directory—IAM manages and authenticates regular users using AD, while PAM secures privileged AD accounts such as Domain Admins with vaulting, monitoring, and just-in-time access.”`

` IAM manages everyday user identities and access like email, VPN, and applications using SSO and MFA. PAM is used for high-risk privileged accounts such as admins, where access is temporary, audited, and credentials are vaulted to prevent misuse or compromise.`

Difference Between IAM and PAM
| IAM                                    | PAM                                                            |
| -------------------------------------- | -------------------------------------------------------------- |
| Manages all identities and access      | Focuses on **privileged accounts**                             |
| Examples: employee login, app accounts | Examples: root, domain admin, DB admin                         |
| General access control                 | Enhanced security controls (vaulting, JIT, session monitoring) |


IAM Examples : Azure AD, Okta, AWS IAM, Google Workspace IAM

PAM Examples : CyberArk, BeyondTrust, Azure PIM,AWS IAM Roles (temporary elevation)

IGA Examples: SailPoint, Saviynt, One Identity

### IGA (Identity Governance and Administration)

IGA (Identity Governance and Administration) is a sub-domain of IAM focused on governing who should have access, why they have it, and proving it is correct over time.

`Think of it as “identity compliance + access oversight.”`

`IGA ensures the right people have the right access for the right reasons—and that access can be reviewed, approved, and audited.`

`If IAM is access, IGA is control and accountability.`

IGA vs IAM vs PAM (Very Important)

| Capability             | IAM | IGA | PAM |
| ---------------------- | --- | --- | --- |
| Authentication (login) | ✅   | ❌   | ❌   |
| SSO / MFA              | ✅   | ❌   | ❌   |
| Provision accounts     | ✅   | ✅   | ❌   |
| Approvals & reviews    | ❌   | ✅   | ❌   |
| Compliance reporting   | ❌   | ✅   | ❌   |
| Privileged accounts    | ❌   | ❌   | ✅   |
| Session recording      | ❌   | ❌   | ✅   |




Troubleshooting

CyberArk
- Check user in Vault & Safe
- Check user in AD group
