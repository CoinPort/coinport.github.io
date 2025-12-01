**CoinPort Pty Ltd**  
**Cybersecurity Awareness Policy & Procedures**  
**Document Number:** CP-INFOSEC-002  
**Version:** 2.1  
**Effective Date:** 12-Feb-2025  
**Review Date:** 12-Feb-2026

---

### **1.0 POLICY STATEMENT**
CoinPort is committed to protecting the confidentiality, integrity, and availability of its information assets, client data, and financial systems. All employees, contractors, and authorised third parties are responsible for understanding and adhering to cybersecurity best practices to mitigate risks including data breaches, financial fraud, ransomware, and insider threats. Security is a condition of employment.

### **2.0 PURPOSE & SCOPE**
This document establishes mandatory cybersecurity standards and procedures for all personnel. It aligns with the Australian Government’s *Essential Eight* mitigation strategies, the *Privacy Act 1988* (including Notifiable Data Breaches scheme), and the security obligations of our Australian Financial Services Licence (AFSL) and AUSTRAC registration.

---

### **3.0 CORE PRINCIPLES & PROCEDURES**

#### **3.1 Phishing & Social Engineering Defence**
*   **Principle:** Employees are the first line of defence. All personnel must be able to identify and appropriately report attempted social engineering attacks.
*   **Procedures:**
    1.  **Identification:** Be suspicious of unsolicited communications (email, SMS, phone, social media) that:
        *   Create a sense of urgency, fear, or too-good-to-be-true offers.
        *   Request sensitive information, passwords, or 2FA codes.
        *   Contain generic greetings, poor spelling, or suspicious sender addresses (e.g., `support@coinport-support.au`).
        *   Encourage clicking links or opening attachments unexpectedly.
    2.  **Action:**
        *   **DO NOT** click links, open attachments, or provide any information.
        *   **DO** verify the request through a separate, trusted channel (e.g., a known phone number, not the one provided in the email).
        *   **REPORT IMMEDIATELY:** Forward the entire phishing email as an attachment to **phishing@coinport.com.au** or report via the dedicated Slack channel `#cyber-alerts`. For suspicious calls, note details and report immediately to IT.
    3.  **Mandatory Training:** All employees must complete quarterly simulated phishing campaigns. Failure rates above 15% trigger mandatory re-training.

#### **3.2 Password & Authentication Management**
*   **Principle:** Strong, unique passwords combined with Multi-Factor Authentication (MFA) are non-negotiable for preventing unauthorised access.
*   **Procedures:**
    1.  **Password Creation (For systems not using Single Sign-On):**
        *   Minimum **14 characters**.
        *   Must include a mix of uppercase, lowercase, numbers, and special symbols.
        *   Must **NOT** contain dictionary words, personal information, or predictable sequences.
        *   Use a **company-approved password manager** (Bitwarden Enterprise) to generate and store all passwords. **Storing passwords in browsers, spreadsheets, or notes is strictly prohibited.**
    2.  **Password Hygiene:**
        *   **No Reuse:** Passwords must not be reused across CoinPort systems or with personal accounts.
        *   **No Sharing:** Passwords must never be shared. If access must be granted, use approved delegation functions or contact IT.
        *   **Change on Demand:** Passwords must be changed immediately if compromise is suspected.
    3.  **Multi-Factor Authentication (MFA):**
        *   MFA via **YubiKey or Microsoft Authenticator** is **mandatory** for all systems handling client data, administrative functions, or code repositories.
        *   Backup codes must be stored securely in the company password manager.
        *   **SMS-based 2FA is prohibited for internal systems** due to SIM-swap risks.

#### **3.3 Secure Data Handling & Classification**
*   **Principle:** Data must be protected according to its sensitivity. Unauthorised disclosure of client or proprietary data constitutes a serious breach.
*   **Procedures:**
    1.  **Data Classification:** All data must be treated as per its classification:
        *   **PUBLIC:** Information on the public website.
        *   **INTERNAL:** Non-sensitive operational data (e.g., internal memos).
        *   **CONFIDENTIAL:** Business plans, employee data.
        *   **RESTRICTED:** **Client Personal Identifiable Information (PII), financial data, private keys, wallet addresses, transaction histories, source code.**
    2.  **Handling RESTRICTED Data:**
        *   **At Rest:** Must be encrypted using company-approved solutions (AES-256).
        *   **In Transit:** Must use TLS 1.2+ encryption (e.g., HTTPS, VPN).
        *   **Storage:** Must only reside on approved, secured company systems (e.g., encrypted drives, designated cloud storage). **Local storage on personal devices or unauthorised cloud services (e.g., personal Google Drive) is prohibited.**
        *   **Disposal:** Digital data must be securely erased. Physical documents must be cross-shredded via designated secure bins.
    3.  **Device Security:**
        *   **Company-Issued Devices:** Must have disk encryption enabled, auto-lock after 5 minutes, and run approved endpoint protection.
        *   **BYOD (Approved Roles Only):** Requires a formal agreement and installation of a Mobile Device Management (MDM) profile to enforce security policies.
        *   **USB Devices:** Use of unauthorised USB storage devices is blocked. Approved encrypted USBs require management approval.

#### **3.4 Insider Threat Awareness**
*   **Principle:** Threats can originate from within, whether malicious or unintentional. Vigilance and a culture of reporting are critical.
*   **Procedures:**
    1.  **Recognise Potential Indicators:** Report concerns if a colleague exhibits:
        *   Attempts to access data or systems not required for their role.
        *   Unexplained financial stress or disgruntled behaviour combined with data access.
        *   Unauthorised use of storage media or attempts to bypass security controls.
        *   Downloading large volumes of sensitive data without business justification.
    2.  **Clear Desk/Clear Screen Policy:**
        *   Lock all workstations (Windows + L) when leaving your desk.
        *   Secure physical RESTRICTED documents in locked drawers overnight.
    3.  **Reporting Obligation:**
        *   Employees must report suspicious internal activity **without fear of reprisal** to their manager, the **CCO**, or via the anonymous **Whistleblower hotline**.
        *   Reports are treated confidentially and investigated by the **Security & Integrity Committee** (CCO, Head of IT, HR Director).

#### **3.5 Incident Response & Reporting**
*   **Principle:** Rapid containment and reporting minimise damage and regulatory impact.
*   **Procedures:**
    1.  **If you suspect a breach (e.g., clicked a phishing link, lost a device, data exposed):**
        *   **IMMEDIATELY** contact the **IT Security Team** via the 24/7 emergency line (**[Internal Phone Number]**) or the `#cyber-incident` Slack channel.
        *   **DO NOT** attempt to investigate or remediate the issue yourself.
    2.  The IT Security Team will initiate the **Incident Response Plan**, which includes containment, eradication, recovery, and notification per the *Notifiable Data Breaches* scheme if required.

---

### **4.0 ROLES & RESPONSIBILITIES**
*   **All Personnel:** Adhere to this policy, complete mandatory training, and report security incidents.
*   **Line Managers:** Enforce policy within teams, model secure behaviour, and escalate concerns.
*   **IT Security Team:** Implement technical controls, monitor threats, conduct training simulations, and lead incident response.
*   **Chief Compliance Officer (CCO):** Overall accountability for cybersecurity governance and regulatory reporting.
*   **Human Resources:** Ensure policy adherence is part of performance reviews and disciplinary processes.

---

### **5.0 TRAINING & COMPLIANCE**
*   All new employees must complete **Cybersecurity Induction Training** before receiving system access.
*   **Annual refresher training** and **quarterly phishing simulations** are mandatory for all staff.
*   Compliance with this policy is a condition of ongoing employment. Violations may result in disciplinary action, up to and including termination, and may have legal or regulatory consequences.

---

### **6.0 POLICY REVIEW**
This policy is reviewed annually by the IT Security Team and CCO to adapt to the evolving threat landscape and regulatory changes.

---

**Approvals:**

Chief Technology Officer: Peter Cooney    Date: 12-Feb-2025

Chief Compliance Officer: Kent Kingsley    Date: 12-Feb-2025