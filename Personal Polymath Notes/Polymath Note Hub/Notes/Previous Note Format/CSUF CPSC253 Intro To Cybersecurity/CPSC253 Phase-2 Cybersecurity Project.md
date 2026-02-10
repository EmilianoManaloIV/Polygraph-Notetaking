___
# **ACME Corporation Authentication & Password Policy (NIST-Aligned)**

**Type of Policy:** Administrative  
**Effective Date:** January 2025  
**Last Revised:** January 2025  
**Review Cycle:** Annual (Next Review: January 2026)  
**Policy Owner:** ACME Corporation Cybersecurity  
**Contact:** John Kaset, Governance Risk & Compliance Manager – Cybersecurity  
**Email:** johnkaset@acmecorp.com

---

# **1. Reason for Policy**

This policy establishes the minimum authentication and password requirements for ACME Corporation systems, applications, databases, cloud services, and network devices.  
Its purpose is to:

- Protect access to ACME information systems
    
- Reduce risk of unauthorized access
    
- Comply with **NIST SP 800-63B** authentication standards
    
- Ensure strong authentication, password security, and identity protections
    

---

# **2. Policy Statement**

Authentication to ACME systems must follow NIST-aligned best practices.

## **2.1 Multifactor Authentication (MFA) Requirements**

The following MUST use **MFA** (AAL2 or higher, per NIST SP 800-63B):

- Privileged/administrative accounts
    
- Remote access (VPN, cloud, SaaS, external systems)
    
- All systems containing Sensitive or Regulated Data
    
- Identity Providers (SSO platforms such as Azure AD, Okta)
    
- Cloud-hosted platforms (IaaS, SaaS, PaaS)
    
- Third-party access with ACME credentials
    

## **2.2 Passwordless Authentication**

Where supported, ACME shall prioritize the adoption of **phishing-resistant authenticators** such as:

- **FIDO2/WebAuthn security keys**
    
- Platform authenticators (Windows Hello, Apple Passkeys)
    

(Per NIST SP 800-63B §5.2.5)

## **2.3 Account Responsibility**

ACME users must protect authentication credentials and:

- Must not share passwords
    
- Must not reuse corporate passwords on external sites
    
- Must report compromised accounts immediately
    
- Must use ACME-approved password managers
    

---

# **3. Standards**

## **3.1 General Standards (Applies to All Authentication Factors)**

To align with **NIST SP 800-63B**, ACME enforces:

- Passwords **must never be transmitted in clear text**
    
- No credential may be stored without **salted, hashed protection** using modern KDFs (PBKDF2, bcrypt, scrypt, Argon2)
    
- Passwords must be **screened against known-breached, commonly used, and predictable passwords**
    
- Login systems **must implement throttling/rate-limiting** against failed attempts
    
- Password managers are recommended for all users
    
- Default passwords must be changed before any system becomes operational
    
- Temporary or one-time passwords must be **randomly generated** and changed at first use
    

(Aligned with NIST SP 800-63B §5.1.1.2 and §5.1.2.2)

---

# **4. Single-Factor Password Requirements**

(Used only where MFA is not technically feasible)

All single-factor authentication passwords must:

- Contain **at least 8 characters** (NIST §5.1.1.2)
    
- Have **no maximum length less than 64 characters**
    
- Allow all printable ASCII and Unicode characters
    
- Not require composition rules (NIST discourages complexity rules)
    
- Not require routine expiration (NIST prohibits forced rotation)
    
- Change only if:
    
    - The password is compromised
        
    - The user requests it
        
    - System policy necessitates a reset
        

**Removed: character-class complexity and 365-day expiration per NIST guidance.**

---

# **5. Multifactor Password Requirements**

Where a password is one of the factors in MFA:

- Minimum length: **8 characters**
    
- No composition rules required
    
- No periodic expiration
    
- Must be screened against prohibited password lists
    
- Shall support **passwordless** authentication transitions
    

(NIST SP 800-63B §5.1.1.2)

---

# **6. Mobile Device Authentication Standards**

Mobile devices accessing ACME data must use:

- A password or PIN of **at least 6 digits/characters**, **or**
    
- Biometrics (facial recognition, fingerprint, etc.) paired with a fallback secret
    
- Modern screen locks (pattern, swipe, passkeys) permitted if device encryption is enabled
    

Biometric authentication must follow NIST rules:

- On-device matching only
    
- Must not be the sole authentication factor for MFA
    
- Must have a backup PIN/password
    

(NIST SP 800-63B §5.2.3)

---
# ✅ **ACME Corporation Cyber Security Policy (NIST-Aligned Update)**

**Type of Policy:** Administrative  
**Effective Date:** January 2025  
**Last Revised:** January 2025  
**Review Cycle:** Annual (Next Review: January 2026)  
**Policy Owner:** ACME Corporation Cybersecurity  
**Contact:** John Kasket, Governance Risk & Compliance Manager – Cyber Security  
**Email:** johnkasket@acmecorp.com

---

# **1. Reason for Policy**

The ACME Corporation Cyber Security Policy establishes the foundational principles for protecting ACME information systems, data, and IT resources. It defines responsibilities for securing infrastructure, enabling cybersecurity governance, and ensuring compliance with:

- NIST Cybersecurity Framework (CSF 2.0)
    
- NIST SP 800-53 Rev. 5 security and privacy controls
    
- Corporate Data Governance and Risk Management Program
    
- Regulatory and contractual security obligations
    

The policy safeguards the confidentiality, integrity, and availability (CIA) of ACME systems.

---

# **2. Policy Statement**

All ACME employees, contractors, and authorized users are responsible for safeguarding the ACME information systems they access. Users must:

- Follow ACME cybersecurity policies, standards, and procedures
    
- Use ACME IT resources in accordance with the Acceptable Use Policy
    
- Keep accounts, passwords, and authentication mechanisms secure
    
- Secure personally owned devices used to access ACME resources (“BYOD”)
    

ACME employees may grant temporary guest access to IT resources only through ACME-approved processes. Individuals providing guest access are responsible for ensuring:

- Guests follow ACME policies
    
- The access is appropriate for the intended purpose
    
- The access is removed when no longer required
    

Unauthorized access or misuse is prohibited.

---

# **3. Research Computing & Security Exceptions**

ACME recognizes that cybersecurity research sometimes requires the use of specialized, high-risk tools, including malware, exploit frameworks, or systems intentionally configured outside standard security controls.

To support research while protecting ACME systems:

- Researchers must operate such environments **in isolated, controlled, and approved research networks**, separate from production systems
    
- A documented risk assessment is required (aligned with NIST RA-3 / PM-9)
    
- Researchers are fully accountable for their actions and any resulting impact
    
- Any malicious code handling must follow ACME’s **High-Risk Computing Environment Standard**
    

---

# **4. Network Management**

The Office of Information Technology (OIT) is responsible for planning, implementing, securing, and managing all ACME networks, including wired, wireless, and cloud networking infrastructure.

## **4.1 Restrictions on Network Appliances**

No networking device may be deployed without **prior written approval** from OIT or a designated IT lead. Restricted devices include:

- Routers
    
- Switches
    
- Hubs
    
- Wireless access points
    
- Voice over IP (VoIP) network components
    
- Intrusion detection systems (IDS)
    
- Intrusion prevention systems (IPS)
    
- VPN solutions
    
- Consumer-grade networking equipment
    
- Any device that routes, inspects, proxies, tunnels, or broadcasts network traffic
    

This aligns with NIST **CM-7 (Least Functionality)** and **PM-11 (Mission/Business Process Definition)**.

## **4.2 Logging Requirements**

Units deploying approved appliances must:

- Capture system and network logs
    
- Retain logs for **a minimum of 365 days**
    
- Ensure logs meet ACME audit logging standards (aligned with **AU-2, AU-6, AU-12**)
    

---

# **5. System Administration**

## **5.1 Designated Administrators**

Every ACME-owned or ACME-managed IT resource—including servers, cloud services, virtual machines, applications, and endpoints—must have a designated system administrator.

- Administrators may be members of ACME’s technical support teams or approved technical personnel
    
- Responsibilities must be documented and acknowledged
    
- Administrators are accountable for maintaining system security and compliance
    

## **5.2 Administrative Responsibilities**

System administrators must:

- Follow ACME’s System Administration Responsibilities Standard (aligned with NIST PL-2, CM-2, CM-6, SI-2)
    
- Apply security updates and patches in accordance with ACME Patch Management Standards
    
- Maintain system availability, backups, and disaster recovery readiness
    
- Grant access using least privilege and role-based access control (RBAC)
    
- Ensure that systems are accessible to Cybersecurity and technical support teams for monitoring and incident response, unless prohibited by law or regulation
    

Negligent management resulting in unauthorized access or data exposure may result in removal of system administration privileges and disciplinary action.

---

# **6. Scope**

This policy applies to:

- All ACME Corporation employees, contractors, third-party users, and temporary users
    
- All ACME IT Resources, including:
    
    - Endpoints
        
    - Servers
        
    - Cloud platforms
        
    - Virtual machines
        
    - Mobile devices
        
    - Applications
        
    - Research computing environments
        
    - Network infrastructure
        

---

# **7. Policy Terms**

**Endpoint**  
Laptops, desktops, workstations, group access workstations, USB drives, personal network-attached storage, or similar client devices.

**ACME IT Resources**  
All ACME-owned, ACME-provisioned, or ACME-funded computing devices, systems, applications, networks, cloud environments, and storage platforms.

---

# **8. Procedures**

---

## **8.1 Reporting a Security Incident**

Any user who suspects a security incident must immediately report it to:

- Their system administrator or unit technical lead **and/or**
    
- The ACME Cyber Security team (preferred and direct channel)
    

System administrators and technical leads must report suspected incidents, including:

- Compromised or suspicious user accounts
    
- Exposure or suspected exposure of Category 3 sensitive data
    
- A server or system infected with malware
    
- Multiple endpoint malware infections (3+)
    
- Any abnormal system behavior indicating intrusion
    
- Any event meeting the criteria of a "cybersecurity incident" under ACME policy
    

This aligns with NIST **IR-4 (Incident Handling)** and **IR-6 (Incident Reporting)**.

ACME Cyber Security will triage, investigate, and respond to incidents per the Incident Response Plan.

---

# **9. Responsibilities**

## **Chief Information Security Officer (CISO)**

The CISO (or designee) is responsible for:

- Overseeing the ACME Cybersecurity Program
    
- Implementing controls aligned to NIST CSF and SP 800-53
    
- Leading cybersecurity incident response
    
- Ensuring policy enforcement, reporting, and awareness training
    
- Maintaining the cybersecurity risk management program
    

---

# **10. Enforcement**

Violations of this policy may result in:

- Loss of system or network access
    
- Removal of administrative privileges
    
- Disciplinary action, up to and including termination
    
- Civil and/or criminal penalties for malicious or negligent actions
    

To report unethical behavior or policy violations, users may contact ACME’s confidential Ethics Hotline.

---

# **Appendix A – NIST References Incorporated**

### **NIST Cybersecurity Framework (CSF 2.0)**

Identify, Protect, Detect, Respond, Recover functions.

### **NIST SP 800-53 Rev. 5 Security Controls**

- **AC-1, AC-3, AC-6:** Access control, least privilege
    
- **AU-2, AU-6, AU-12:** Audit logging & monitoring
    
- **CM-2, CM-6, CM-7:** Configuration management
    
- **IR-4, IR-6:** Incident response & reporting
    
- **PL-2, PM-9:** Planning & risk management
    
- **RA-3:** Risk assessments
    
- **SI-2:** Patch & vulnerability management
    

### **NIST SP 800-171 (for contractor systems)**

### **NIST Zero Trust Architecture (SP 800-207)**
# **7. Service & Privileged Account Requirements**

## **7.1 Service Accounts**

Service accounts must:

- Use **32+ character** randomly generated passwords
    
- Be stored in a **credential vault**
    
- Have **non-interactive** login disabled
    
- Use **no shared** credentials across systems
    
- Be reviewed quarterly
    

## **7.2 Privileged Accounts**

Must:

- Use MFA at AAL2 or AAL3
    
- Use password lengths of **15+ characters**
    
- Never be shared
    
- Use separate admin and standard accounts
    

(NIST SP 800-63B §4.2 & §5.1.2)

---

# **8. Scope**

This policy applies to:

- All ACME employees, contractors, partners, and third-party users
    
- All ACME endpoints (computers, servers, mobile devices, IoT)
    
- All applications (on-premises, cloud, SaaS)
    
- All identity providers (SSO, federation, cloud identity)
    
- Any system requiring a unique login
    

Aligned to NIST SP 800-63B (AAL), SP 800-63C (FAL).

---

# **9. Definitions**

(Updated to NIST language)

**Memorized Secret (Password)** – A text or numeric string used as a single authentication factor.  
**Authenticator** – A device, token, or factor used to prove identity.  
**Multifactor Authentication (MFA)** – Authentication using two or more distinct factors.  
**Phishing-Resistant Authenticator** – Security keys, FIDO2, WebAuthn, or equivalent.  
**Biometric** – Fingerprint, face scan, or other biometric trait used per NIST requirements.

---

# **10. Enforcement**

Violations of this policy may result in:

- Revocation of system access
    
- Mandatory security training
    
- Disciplinary action up to termination
    
- Legal actions where applicable
    

Systems may enforce technical controls to ensure compliance.

---

# **Appendix A – NIST References Used**

- **NIST SP 800-63B §5.1.1.2 – Memorized Secrets**
    
- **NIST SP 800-63B §5.1.2.2 – Throttling and Rate Limiting**
    
- **NIST SP 800-63B §5.2.3 – Biometric Requirements**
    
- **NIST SP 800-63B §4.2 – Authentication Assurance Levels**
    
- **NIST SP 800-63C – Federation Requirements**
    
- **NIST SP 800-63 – Digital Identity Guidelines**
---
# ✅ **ACME Corporation Data Privacy & Access Policy (NIST-Aligned Update)**

**Type of Policy:** Administrative  
**Effective Date:** January 2025  
**Last Revised:** January 2025  
**Review Cycle:** Annual (Next Review: January 2026)  
**Policy Owner:** ACME Corporation Cybersecurity  
**Contact:** John Kaset, Governance Risk & Compliance Manager  
**Email:** johnkaset@acmecorp.com

---

# **1. Reason for Policy**

ACME Corporation provides information technology resources to support business operations and the mission of the organization. ACME is committed to protecting the privacy of employees and contractors while also complying with legal, regulatory, and operational requirements.

This policy establishes:

- Standards for accessing employee/contractor data
    
- Requirements for respecting reasonable privacy expectations
    
- NIST-aligned governance for handling electronic communications and files
    
- Auditability, authorization, and minimum-access safeguards
    

This aligns with the **NIST Privacy Framework (Govern-P, Control-P, Protect-P)** and **NIST SP 800-53 Rev. 5 (AR-2, AR-4, AC-6, AU-12, DI-1, IP-1)**.

---

# **2. Policy Statement**

ACME Corporation’s IT resources are provided primarily for business use. Limited personal use is permitted in accordance with the ACME Acceptable Use Policy. However, **personal communications and files stored or transmitted on ACME systems may be accessed by the Corporation only under established, approved circumstances**.

ACME Corporation:

- Respects employee and contractor privacy expectations
    
- Limits access to electronic information to specific authorized purposes
    
- Requires all access to be **logged, approved, reviewed, and justified**
    
- Enforces NIST-aligned minimum necessary/least privilege standards
    

All electronic information that resides on or transits ACME systems is subject to access for legitimate business, operational, legal, or security purposes, including:

1. Compliance with legal orders and regulatory requirements
    
2. Investigating suspected violations of law or policy
    
3. Security monitoring, threat detection, and incident response
    
4. Diagnosing and resolving system or network issues
    
5. Addressing emergencies impacting safety, security, or operations
    
6. Accessing data belonging to employees who are terminated, deceased, incapacitated, or unavailable
    
7. Complying with verified requests from HR on behalf of authorized representatives
    
8. Research or analytics where data is properly anonymized or pseudonymized
    

These uses align with NIST SP 800-53 privacy controls: **AR-3, AR-4, IP-1, DI-1, DM-1, AC-6, AU-6, IR-4**.

---

# **3. Scope**

This policy governs **all access to files, communications, logs, or data** transmitted on or stored within ACME Corporation’s:

- Information Technology Resources
    
- Cloud platforms
    
- Third-party hosted systems
    
- Collaboration and messaging tools
    
- Storage, backup, and archival systems
    
- Network infrastructure
    

Unauthorized users who store or transmit data via ACME systems **have no expectation of privacy**, consistent with NIST **Authority to Collect (AR-2)** and **Data Minimization (DM-1)** principles.

---

# **4. Definitions**

**Information Technology Resources (IT Resources)**  
Computers, networks, cloud applications, mobile devices, storage, collaboration systems, messaging platforms, communication tools, and any infrastructure owned or managed by ACME Corporation.

**Access**  
Viewing, retrieving, copying, transferring, disclosing, monitoring, or interacting with electronic data.

**Personally Identifiable Information (PII)**  
Information that can identify, contact, or locate an individual, as defined in **NIST SP 800-122**.

**Minimum Necessary / Least Privilege**  
Only the smallest amount of access required to perform an authorized business purpose (NIST SP 800-53 AC-6).

---

# **5. Procedures**

---

## **5.1 Login Banner Requirement**

Where technically possible, all ACME systems (excluding personal endpoints and mobile devices) must display a **standard Terms of Use security banner** prior to authentication:

---

### **TERMS OF USE**

This information technology resource is the property of ACME Corporation and is for authorized use only. All activities are monitored and logged. Any files or communications on this system may be accessed, audited, or disclosed to authorized personnel for operational, security, administrative, or legal purposes as outlined in corporate policy. Use of this system indicates acknowledgment of these terms.

---

This fulfills NIST SP 800-53 **AC-8 (System Use Notification)**.

---

## **5.2 Requests for Access to Employee/Contractor Data**

All requests to access electronic information **must**:

- Be submitted in writing
    
- Provide a specific business, legal, or security justification
    
- Follow the standardized Access Request Workflow
    

### **Required Authorization Path**

1. **Requester** submits the request with justification
    
2. **Chief Information Officer (CIO)** or officially designated delegate **must approve**
    
3. Cybersecurity logs, fulfills, and records the access action
    
4. HR and Legal are consulted when required
    
5. Access must be:
    
    - Logged
        
    - Time-bound
        
    - Limited to minimum necessary data
        
    - Reviewed upon completion
        

Department-level approval **is not permitted** without CIO oversight.

This aligns with NIST SP 800-53:

- **AR-4 (Privacy Monitoring and Auditing)**
    
- **AC-6 (Least Privilege)**
    
- **AU-2/AU-12 (Audit Logging)**
    
- **AR-8 (Accounting of Disclosures)**
    

---

## **5.3 Logging & Audit Requirements**

All access performed under this policy must be:

- Logged in immutable audit trails
    
- Retained according to ACME’s record retention policy
    
- Periodically reviewed by Cybersecurity and Internal Audit
    

Per NIST:

- **AU-6, AU-12, AR-4, IR-4**
    

---

## **5.4 Data Minimization & Protection Requirements**

When accessing files or communications:

- Only data **necessary** for the approved purpose may be accessed
    
- PII must be protected as required by **NIST SP 800-122 and SP 800-53 DM-1**
    
- Data must not be disclosed beyond authorized personnel
    

---

# **6. Enforcement**

Failure to comply with this policy may result in:

- Revocation of IT access
    
- Disciplinary actions up to termination
    
- Civil or criminal liability
    
- Reporting obligations where required by law
    

All enforcement actions must follow HR, Legal, and Cybersecurity guidelines.

---

# **Appendix A – NIST References Incorporated**

**NIST Privacy Framework**

- Govern-P, Control-P, Protect-P
    

**NIST SP 800-53 Rev. 5 Privacy & Security Controls**

- AR-2, AR-3, AR-4, AR-8
    
- AC-6, AC-8
    
- AU-2, AU-6, AU-12
    
- DM-1, DI-1
    
- IP-1, SE-1
    

**NIST SP 800-122: Guide to Protecting PII**  
**NIST SP 800-171: Protecting CUI**