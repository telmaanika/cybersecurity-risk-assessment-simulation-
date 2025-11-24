This project simulates a full cybersecurity risk assessment for a fictional telehealth startup.  
The company provides virtual consultations, remote patient monitoring, and prescription management.  
Because it handles Protected Health Information (PHI), it must comply with HIPAA and maintain strong cybersecurity practices.

The goal of this project is to identify risks, analyze system architecture, evaluate threats, and recommend security controls aligned with HIPAA, NIST CSF, and CIS standards.

---

## Project Overview

A telehealth startup relies heavily on cloud infrastructure, remote access, video conferencing systems, and digital prescriptions.  
This increases cybersecurity risk due to:

- Remote workforce  
- Cloud-based data storage  
- PHI transmitted over the internet  
- Third-party teleconferencing services  
- Mobile device access  
- Rapid scaling typical of startups  

This project includes:

1. System Description & Architecture Map
2. Threat Model (STRIDE)
3. Risk Register (CSV + Table)
4. HIPAA/GRC Control Mapping
5. Security Recommendations

**My Notes:**  
I chose a telehealth company because it combines healthcare and technology, which helps me understand HIPAA requirements and modern cybersecurity risks like cloud exposure.

## Technologies / Frameworks Used

| Category | Tools / Standards |
|----------|------------------|
| Architecture | Cloud apps, mobile devices, APIs |
| Risk Frameworks | NIST CSF, CIS Controls, HIPAA Security Rule |
| Analysis Models | STRIDE, impact-likelihood scoring |
| Documentation | CSV, Markdown |

---

## System Architecture (Simplified)
Patients → Mobile App → API Gateway → Cloud App Server → Encrypted Database (PHI)
→ Telehealth Video Platform (3rd party)
Employees → Laptops (remote)
Admins → Cloud Console

Key assets:
- Patient PHI  
- Appointment records  
- Video call data  
- Prescription info  
- User accounts  
- Billing information  


## Threat Model (STRIDE)

| STRIDE Category | Example Threat in Telehealth |
|-----------------|------------------------------|
| **Spoofing** | Fake patient or provider accounts |
| **Tampering** | Altered prescriptions or medical notes |
| **Repudiation** | Disputes over telehealth actions |
| **Information Disclosure** | PHI leaked through unsecured video platform |
| **Denial of Service** | Telehealth platform outage |
| **Elevation of Privilege** | Hackers gaining admin rights in cloud |

**My Notes:**  
STRIDE helped me think like an attacker and identify how a telehealth system could be compromised.

---

## Risk Register (CSV Included)

RiskID,Asset,Threat,Impact,Likelihood,Score,Current Controls,Recommended Controls
1,PHI Data,Unauthorized Access,High,Medium,15,MFA for employees,Zero Trust + device verification
2,API Gateway,DDOS Attack,High,Medium,15,Basic firewall,WAF + rate limiting
3,Video Platform,Data Leakage,High,High,20,Vendor contract,Business Associate Agreement + encryption
4,Mobile App,Account Takeover,Medium,High,12,Password login,Add MFA + device binding
5,Cloud Database,Data Breach,Critical,Medium,20,Encrypted storage,Key rotation + logging monitoring
6,Remote Workforce,Phishing Attacks,Medium,High,12,Email filter,Security awareness training

Scoring method:
Impact (1–5) × Likelihood (1–5) = Score (max 25)

HIPAA & NIST CSF Control Mapping
Area	HIPAA Relevance	Control Recommendation
Access Control	HIPAA 164.312(a)	MFA, least privilege, RBAC
Audit Controls	HIPAA 164.312(b)	Cloud logging, SIEM
Transmission Security	HIPAA 164.312(e)	TLS 1.2+, VPN tunnels
Integrity	HIPAA 164.312(c)	Hashing, validated APIs
Person/Entity Authentication	HIPAA 164.312(d)	Provider identity verification

*NIST CSF Categories Included:*
ID.AM (Asset Management)
PR.AC (Identity Control)
aPR.DS (Data Security)
DE.CM (Monitoring)
qWRS.MI (Mitigation)

**Security Recommendations Summary**
-Implement Zero Trust Access
-Device verificationZSSSSSSS
-Behavioral analytics
-Upgrade Logging & Monitoring
-Cloud logs

SOC tool integrations
Encrypt All Communication ZX                                                                                 ```
End-to-end video conferencing
Encrypted PHI transmission
Vendor Risk Management

BAAs for telehealth partners
Phishing & User Training
Monthly security awareness training

My Notes:
Writing recommendations helped me understand how to prioritize controls based on risk.

Project Files
cybersecurity-risk-assessment-healthcare/
│
├─ README.md
├─ risk_register.csv
├─ architecture_overview.md
└─ controls_mapping.md

Personal Reflection
This project helped me understand healthcare risks, HIPAA Security Rule standards, and how telehealth companies must handle cloud security and PHI protection.
It also helped me practice GRC tasks such as risk scoring, control mapping, and vendor management.

Author
Telma Anika
Email: tellyannika@gmail.com
