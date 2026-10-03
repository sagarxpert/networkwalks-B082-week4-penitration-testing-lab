
<div align="center">

# 🛡️ NetworkWalks Cybersecurity Internship

## Week 04 — Web Application Penetration Testing

### 🔴 Web Application Security Assessment & Vulnerability Analysis

<p>
  <img src="https://img.shields.io/badge/NetworkWalks-B083-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Week-04-purple?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Assessment-Black--Box-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Overall%20Risk-CRITICAL-red?style=for-the-badge" />
</p>

<p>
  <img src="https://img.shields.io/badge/Web%20Security-Penetration%20Testing-8A2BE2?style=flat-square" />
  <img src="https://img.shields.io/badge/SQL%20Injection-Tested-critical?style=flat-square" />
  <img src="https://img.shields.io/badge/PDF%20Security-Assessed-yellow?style=flat-square" />
  <img src="https://img.shields.io/badge/Data%20Exposure-Identified-red?style=flat-square" />
  <img src="https://img.shields.io/badge/Reporting-Completed-success?style=flat-square" />
</p>

<p>
  <strong>Authorized Educational Penetration Testing • Vulnerability Assessment • Security Reporting</strong>
</p>

</div>

---

# 📌 Assessment Overview

This repository documents my **Week 04 Web Application Penetration Testing & Vulnerability Assessment** completed as part of the **NetworkWalks B082 Cybersecurity Internship**.

The assessment focused on an authorized educational web application environment and followed a structured **black-box penetration-testing methodology** covering reconnaissance, attack-surface analysis, authentication testing, controlled exploitation, data extraction, sensitive-data exposure analysis, risk assessment, and remediation planning.

> ⚠️ **Important:** All testing documented in this repository was performed within the authorized educational/test environment. The target and associated information were provided for cybersecurity training and skill validation.

---

# 🎯 Assessment Objectives

The Week 04 assessment was divided into four major milestones:

| Milestone | Objective | Status |
|---|---|---|
| 🔴 **M1** | Initial Access & Patient Report Retrieval | ✅ Completed |
| 🟠 **M2** | PDF Encryption Recovery & Data Extraction | ✅ Completed |
| 🔴 **M3** | Critical Data Exposure & Database Discovery | ✅ Completed |
| 📋 **M4** | Final Penetration Testing Report | ✅ Completed |

---

# 🧭 Assessment Journey

```text
┌─────────────────────────────────────┐
│       🔎 RECONNAISSANCE             │
│   Attack Surface Identification     │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│       🔐 AUTHENTICATION TESTING     │
│       Patient Portal Analysis       │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│       💉 VULNERABILITY TESTING      │
│          SQL Injection              │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│       🚪 AUTHENTICATION BYPASS      │
│       Restricted Portal Access      │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│       📄 DATA EXTRACTION            │
│       PDF Security Analysis         │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│       🔓 PASSWORD RECOVERY          │
│       Protected PDF Analysis        │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│       🗄️ DATABASE DISCOVERY         │
│       Public Backup Exposure        │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│       📊 RISK ASSESSMENT            │
│       Findings & Impact Analysis    │
└─────────────────┬───────────────────┘
                  │
                  ▼
┌─────────────────────────────────────┐
│       📋 SECURITY REPORTING         │
│       Remediation Recommendations   │
└─────────────────────────────────────┘
````

---

# 🔴 M1 — Initial Access & Patient Report Retrieval

### `MILESTONE 01 | WEB APPLICATION INITIAL ACCESS`

**Focus Areas**

`Reconnaissance` • `Attack Surface Enumeration` • `Authentication Analysis` • `SQL Injection` • `Authentication Bypass` • `Restricted Resource Access` • `Evidence Collection`

## 🔎 Objective

The first milestone focused on analyzing the authorized web application, identifying the patient portal as an important attack surface, testing its authentication mechanism, and validating whether user-controlled input could influence authentication logic.

## 🎯 M1 Objectives

* Conduct reconnaissance against the authorized target
* Identify exposed application entry points
* Analyze the patient portal authentication mechanism
* Analyze user-controlled input
* Identify authentication and input-handling weaknesses
* Validate identified vulnerabilities through controlled testing
* Demonstrate authentication bypass
* Access the restricted patient portal
* Identify designated laboratory reports
* Retrieve the required reports
* Preserve supporting evidence

## 🌐 Target Scope

| Parameter              | Details                    |
| ---------------------- | -------------------------- |
| **Target**             | `medirozahospital.com`     |
| **Assessment Type**    | Black-Box Penetration Test |
| **Application**        | Authorized Web Application |
| **Component**          | Patient Portal             |
| **Authorization**      | Written Authorization      |
| **Testing Scope**      | Target Domain Only         |
| **Social Engineering** | Out of Scope               |
| **Denial of Service**  | Out of Scope               |

---

## 💉 Vulnerability Identified

### SQL Injection — Patient Portal Authentication Bypass

| Attribute              | Result                                                                |
| ---------------------- | --------------------------------------------------------------------- |
| **Finding ID**         | F-001                                                                 |
| **Vulnerability**      | SQL Injection                                                         |
| **Affected Component** | Patient Portal Login                                                  |
| **HTTP Method**        | `POST`                                                                |
| **Endpoint**           | `/patient/login.php`                                                  |
| **Parameter**          | `username`                                                            |
| **Severity**           | 🔴 **Critical**                                                       |
| **Impact**             | Authentication bypass and unauthorized access to restricted resources |

The assessment confirmed that the patient portal authentication functionality was susceptible to SQL injection through a user-controlled authentication parameter.

Controlled exploitation demonstrated that the authentication boundary could be bypassed and the restricted portal could be reached.

### Authentication Flow

```text
Unauthenticated Request
          │
          ▼
   Patient Portal Login
          │
          ▼
   User-Controlled Input
          │
          ▼
      SQL Injection
          │
          ▼
 Authentication Logic Bypassed
          │
          ▼
    HTTP 302 Redirect
          │
          ▼
 /patient/portal.php
          │
          ▼
 Restricted Patient Portal
          │
          ▼
 Patient Report Discovery
          │
          ▼
   Three Reports Retrieved
```

---

## 📄 M1 Result

The assessment successfully reached the restricted patient portal and retrieved the three designated laboratory reports for subsequent authorized security analysis.

| Report                 | Status      |
| ---------------------- | ----------- |
| `patient_report_1.pdf` | ✅ Retrieved |
| `patient_report_2.pdf` | ✅ Retrieved |
| `patient_report_3.pdf` | ✅ Retrieved |

### M1 Status

> 🟢 **COMPLETED**

---

# 🟠 M2 — PDF Encryption Recovery & Data Extraction

### `MILESTONE 02 | PROTECTED DOCUMENT ANALYSIS`

**Focus Areas**

`PDF Security Analysis` • `Encryption Identification` • `Password Recovery` • `Document Decryption` • `Data Extraction` • `Evidence Validation`

## 🔐 Objective

M2 focused on evaluating the effectiveness of document-level security applied to the three laboratory reports retrieved during M1.

The assessment identified the PDF protection mechanism and performed authorized password-recovery testing to determine whether the protected documents could be accessed.

---

## 🔍 Encryption Analysis

The reports were identified as using:

| Attribute                | Details                 |
| ------------------------ | ----------------------- |
| **Document Type**        | PDF                     |
| **Security Scheme**      | Adobe Standard Security |
| **Encryption Algorithm** | RC4                     |
| **Key Length**           | 128-bit                 |
| **Protection**           | Password-Based          |
| **Files Assessed**       | 3                       |

---

## 🔓 Password-Recovery Testing

Password-recovery testing was performed against all three retrieved reports using dictionary-based testing.

### Evidence — PDF Password Recovery

**Screenshot 01 — PDF password recovery**

<img width="1600" height="900" alt="WhatsApp Image 2026-09-06 at 8 53 29 PM" src="https://github.com/user-attachments/assets/c5138355-4768-40c9-b2d7-57b60bff624a" />


---

**Screenshot 02 — Multiple PDF password recovery results**

<img width="1600" height="900" alt="2" src="https://github.com/user-attachments/assets/6a6e8fe8-ce13-4386-b5aa-89a2ac0221ad" />


---

### Recovery Results

| File                   | Encryption   | Password Recovery | Decryption  | Status         |
| ---------------------- | ------------ | ----------------- | ----------- | -------------- |
| `patient_report_1.pdf` | ✅ Identified | ✅ Recovered       | ✅ Completed | **Successful** |
| `patient_report_2.pdf` | ✅ Identified | ✅ Recovered       | ✅ Completed | **Successful** |
| `patient_report_3.pdf` | ✅ Identified | ✅ Recovered       | ✅ Completed | **Successful** |

> 🔐 **Security Note:** Password values are intentionally not reproduced in this README. The screenshots demonstrate the password-recovery process and results within the authorized training environment.

---

## 📊 M2 Extraction Result

```text
Encrypted PDF
      │
      ▼
Encryption Identification
      │
      ▼
Password-Recovery Testing
      │
      ▼
Password Successfully Recovered
      │
      ▼
PDF Decryption
      │
      ▼
Protected Contents Accessible
      │
      ▼
Authorized Data Analysis
```

### M2 Result Summary

| Objective                               | Result       |
| --------------------------------------- | ------------ |
| Identify PDF encryption mechanism       | ✅ Completed  |
| Determine protection method             | ✅ Completed  |
| Assess document protection              | ✅ Completed  |
| Perform password-recovery testing       | ✅ Completed  |
| Recover passwords for all three reports | ✅ Successful |
| Decrypt all three reports               | ✅ Successful |
| Access protected contents               | ✅ Successful |
| Preserve evidence                       | ✅ Completed  |

### M2 Status

> 🟢 **COMPLETED**

---

# 🔴 M3 — Critical Data Exposure

### `MILESTONE 03 | CONFIDENTIAL DATABASE EXPOSURE`

**Focus Areas**

`Sensitive Resource Discovery` • `Directory Listing` • `Database Backup Exposure` • `Database Enumeration` • `Data Exposure Analysis` • `Evidence Collection`

## 🗄️ Objective

M3 focused on identifying additional sensitive resources exposed by the authorized web application.

During the assessment, a historical SQL database backup was identified inside a publicly accessible `/old/` directory.

---

## 🚨 Exposed Database Backup

```text
/old/mediroza_db_backup_2019.sql
```

| Attribute       | Details                       |
| --------------- | ----------------------------- |
| **File**        | `mediroza_db_backup_2019.sql` |
| **Location**    | `/old/`                       |
| **Database**    | `mediroza_hr`                 |
| **Backup Type** | SQL Database Backup           |
| **Exposure**    | Publicly Accessible           |
| **Severity**    | 🔴 **Critical**               |

---

## 📋 Directory Listing

The historical `/old/` directory was accessible and allowed enumeration of previously deployed resources.

| Finding ID | Vulnerability     | Resource | Severity    |
| ---------- | ----------------- | -------- | ----------- |
| **F-004**  | Directory Listing | `/old/`  | 🟠 **High** |

Directory listing increased the likelihood of discovering obsolete, forgotten, or sensitive application artifacts.

---

## 🖥️ Database Exposure Evidence

**Screenshot 03 — Publicly accessible database backup**

<img width="1600" height="900" alt="week4" src="https://github.com/user-attachments/assets/4cdc20b3-50a7-4955-ad30-fd5fd623977d" />


---

## 🧩 Database Structure

The exposed database contained multiple tables. Two particularly relevant tables were:

```text
staff
shareholders
```

### Staff Table

The exposed structure included fields representing:

```text
id
full_name
job_title
department
email
phone
national_id
monthly_salary_zar
date_joined
```

### Shareholders Table

The exposed structure included:

```text
id
shareholder_name
share_percent
shares_held
share_class
```

---

## 📊 Exposure Summary

### Staff Information

| Data Category    | Exposure   |
| ---------------- | ---------- |
| Employee Names   | 🔴 Exposed |
| Job Titles       | 🔴 Exposed |
| Departments      | 🔴 Exposed |
| Email Addresses  | 🔴 Exposed |
| Phone Numbers    | 🔴 Exposed |
| National IDs     | 🔴 Exposed |
| Monthly Salaries | 🔴 Exposed |
| Joining Dates    | 🔴 Exposed |

### Shareholder Information

| Data Category        | Exposure   |
| -------------------- | ---------- |
| Shareholder Names    | 🔴 Exposed |
| Ownership Percentage | 🔴 Exposed |
| Shares Held          | 🔴 Exposed |
| Share Class          | 🔴 Exposed |

---

## 🔗 Exposure Chain

```text
Public Web Application
          │
          ▼
     `/old/` Directory
          │
          ▼
    Directory Listing
          │
          ▼
mediroza_db_backup_2019.sql
          │
          ▼
      mediroza_hr
          │
      ┌───┴─────────────┐
      ▼                 ▼
    staff          shareholders
      │                 │
      ▼                 ▼
Employee Records    Ownership Data
      │
      ▼
Salary + Personnel Data
```

---

## 💥 Security Impact

The exposed database backup represented a **Critical confidentiality failure**.

Potentially exposed categories included:

* Employee personnel information
* Salary information
* Employment information
* Shareholder ownership information
* Internal database structure

The combination of an accessible historical directory and an exposed database backup significantly increased the application's attack surface.

### M3 Status

> 🟢 **COMPLETED**

---

# 📋 M4 — Final Penetration Testing Report

### `MILESTONE 04 | SECURITY ASSESSMENT & REPORTING`

**Focus Areas**

`Executive Summary` • `Scope` • `Methodology` • `Findings` • `Proof of Exploitation` • `Risk Rating` • `Recommendations` • `Remediation`

## 📑 Final Report

The final penetration-testing report consolidates the Week 04 assessment methodology, findings, proof of exploitation, risk assessment, and remediation recommendations.

### 📥 Report

**[📄 View / Download Week 04 Penetration Testing Report](Report/Mediroza_Penetration_Testing_Report.pdf)**

---

# 🚨 Findings Summary

The assessment identified **five security findings** across the authorized web application.

| ID        | Finding                                              | Severity        | Impact                                     | Status      |
| --------- | ---------------------------------------------------- | --------------- | ------------------------------------------ | ----------- |
| **F-001** | SQL Injection — Patient Portal Authentication Bypass | 🔴 **Critical** | Unauthorized patient portal access         | ✅ Confirmed |
| **F-002** | Weak PDF Encryption Passwords                        | 🟠 **High**     | Protected medical information exposure     | ✅ Confirmed |
| **F-003** | Sensitive Database Backup Exposure                   | 🔴 **Critical** | Staff & shareholder information exposure   | ✅ Confirmed |
| **F-004** | Directory Listing — `/old/`                          | 🟠 **High**     | Historical sensitive resource discovery    | ✅ Confirmed |
| **F-005** | Sensitive PDF Metadata                               | 🟡 **Medium**   | Internal deployment information disclosure | ✅ Confirmed |

---

# 📊 Risk Distribution

```text
CRITICAL  ████████████████████  2
HIGH      ████████████████████  2
MEDIUM    ██████████            1
LOW       —                     0
```

### Overall Organizational Risk

# 🔴 CRITICAL

The overall risk was assessed as **Critical** due to the combination of authentication bypass, access to protected information, weak document protection, publicly accessible database resources, and sensitive metadata disclosure.

---

# 🛠️ Tools & Techniques

## 🔧 Tools

<p>
  <img src="https://img.shields.io/badge/curl-CLI-black?style=flat-square&logo=curl" />
  <img src="https://img.shields.io/badge/Python-Analysis-blue?style=flat-square&logo=python" />
  <img src="https://img.shields.io/badge/pypdf-PDF%20Analysis-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/John%20the%20Ripper-Wordlists-red?style=flat-square" />
  <img src="https://img.shields.io/badge/Linux-Security%20Testing-black?style=flat-square&logo=linux" />
</p>

### Techniques Used

* 🔎 Passive & active reconnaissance
* 🌐 Directory enumeration
* 🔐 Authentication analysis
* 💉 Manual SQL injection testing
* 🚪 Controlled authentication-bypass validation
* 📄 PDF security analysis
* 🔓 Dictionary-based password recovery
* 🗄️ Database backup discovery
* 📊 Database structure analysis
* 🧾 Metadata analysis
* 📋 Risk assessment
* 🛠️ Remediation planning

---

# 🧪 Methodology

The assessment followed a structured black-box penetration-testing workflow:

```text
┌──────────────────────┐
│   Reconnaissance     │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ Attack Surface       │
│ Identification       │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ Authentication       │
│ Analysis             │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ Vulnerability        │
│ Identification       │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ Controlled           │
│ Exploitation         │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ Restricted Resource  │
│ Access               │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ Data Extraction      │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ Sensitive Data       │
│ Exposure Analysis     │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ Risk Assessment      │
└──────────┬───────────┘
           ▼
┌──────────────────────┐
│ Remediation          │
│ Recommendations      │
└──────────────────────┘
```

---

# 🛡️ Remediation Highlights

## 🔴 Critical — Immediate Priority

1. Replace dynamic SQL construction with parameterized queries and prepared statements.
2. Validate and constrain user-controlled input.
3. Remove publicly accessible database backups.
4. Disable directory listing on historical directories.
5. Review server logs for access to exposed resources.
6. Rotate potentially exposed credentials and secrets.

## 🟠 High — Short-Term Priority

1. Strengthen document password protection.
2. Re-encrypt sensitive documents.
3. Use strong randomly generated passwords.
4. Move backups outside the web root.
5. Restrict backup access through authentication and authorization.
6. Review historical application artifacts.

## 🟡 Medium — Long-Term Hardening

1. Implement secure software-development practices.
2. Conduct regular source-code and application security reviews.
3. Establish document-security and metadata-sanitization procedures.
4. Implement formal backup-management policies.
5. Integrate security testing into the development lifecycle.

---

# 📸 Evidence Gallery

The repository contains practical evidence supporting the completed assessment milestones.

| Evidence                       | Milestone | Purpose                             |
| ------------------------------ | --------- | ----------------------------------- |
| `week4-m2-pdfcrack-01.png`     | M2        | PDF password-recovery evidence      |
| `week4-m2-pdfcrack-02.png`     | M2        | Multiple PDF recovery results       |
| `week4-m3-database-backup.png` | M3        | Public SQL database backup exposure |

### Evidence Structure

```text
networkwalks-B082-week4-web-pentest/
│
├── README.md
│
├── Report/
│   └── Mediroza_Penetration_Testing_Report.pdf
│
└── evidence/
    ├── week4-m2-pdfcrack-01.png
    ├── week4-m2-pdfcrack-02.png
    └── week4-m3-database-backup.png
```

---

# 🔒 Security & Privacy Notice

This repository documents an **authorized educational penetration-testing exercise**.

The target environment was used for cybersecurity training and skill validation.

Sensitive assessment artifacts such as:

* Original credentials
* Recovered passwords
* Raw database dumps
* Confidential report contents
* Unnecessary personal information

should not be redistributed outside the authorized training context.

Public documentation should focus on **security findings, methodology, sanitized evidence, impact, and remediation**.

---

# ⚖️ Responsible Use

> This project was performed only within an authorized educational/test environment.

The techniques demonstrated in this repository are intended for:

* ✅ Authorized security testing
* ✅ Cybersecurity education
* ✅ Vulnerability validation
* ✅ Defensive security research
* ✅ Security remediation

Unauthorized testing against systems without explicit permission is not permitted.

---

# 📈 Week 04 Learning Outcomes

Through this assessment, I gained practical experience in:

* 🔎 Web application reconnaissance
* 🧭 Attack-surface identification
* 🔐 Authentication security analysis
* 💉 SQL injection validation
* 🚪 Authentication-bypass testing
* 📄 PDF encryption analysis
* 🔓 Password-recovery techniques
* 🗄️ Sensitive database exposure analysis
* 📋 Directory enumeration
* 🧾 Metadata analysis
* 📊 Vulnerability severity assessment
* 🛠️ Security remediation planning
* 📑 Professional penetration-testing reporting

---

# 🏆 Final Assessment Status

```text
╔══════════════════════════════════════════════╗
║              WEEK 04 STATUS                  ║
╠══════════════════════════════════════════════╣
║ M1 — Initial Access             ✅ COMPLETED ║
║ M2 — Data Extraction             ✅ COMPLETED ║
║ M3 — Critical Data Exposure      ✅ COMPLETED ║
║ M4 — Final Security Report       ✅ COMPLETED ║
╠══════════════════════════════════════════════╣
║ Findings Identified                         ║
║                                             ║
║ 🔴 Critical — 2                             ║
║ 🟠 High     — 2                             ║
║ 🟡 Medium   — 1                             ║
╠══════════════════════════════════════════════╣
║ OVERALL RISK: 🔴 CRITICAL                   ║
╚══════════════════════════════════════════════╝
```

---

# 🧠 Final Conclusion

The Week 04 penetration-testing assessment successfully demonstrated the complete lifecycle of a web application security assessment, from reconnaissance and attack-surface identification through controlled exploitation, protected-document analysis, sensitive-data exposure discovery, risk assessment, and remediation planning. The assessment identified critical weaknesses in authentication security and database exposure, along with high-severity document-protection and directory-listing issues and a medium-severity metadata disclosure. All four assigned milestones were successfully completed within the authorized educational scope.

---

<div align="center">

## 🛡️ NetworkWalks B082 — Week 04

### Web Application Penetration Testing & Vulnerability Assessment

**Recon → Exploit → Analyze → Assess → Remediate → Report**

<br>

<img src="https://img.shields.io/badge/Assessment-COMPLETED-success?style=for-the-badge" />
<img src="https://img.shields.io/badge/Risk-CRITICAL-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Milestones-4%2F4-success?style=for-the-badge" />

<br><br>

**Cybersecurity Internship • NetworkWalks • Batch B083F • Week 04**

</div>
