# Mediroza General Hospital – Web Application Penetration Testing

<p align="center">
  <strong>Black-Box Security Assessment | VAPT | Web Application Security</strong>
</p>

## 📌 Project Overview

This project documents an authorized External Black-Box Web Application Penetration Testing assessment of the Mediroza General Hospital web application, conducted as part of the **NetworkWalks Cybersecurity Internship – Batch B084, Week 4**.

The assessment focused on identifying application security weaknesses, validating potential vulnerabilities, evaluating their impact, and providing practical remediation recommendations.

The testing identified six security findings, including SQL Injection authentication bypass, unauthenticated database backup disclosure, weak PDF password protection, sensitive metadata disclosure, username enumeration, and directory listing.

## 🎯 Assessment Objectives

- Identify vulnerabilities in the web application.
- Evaluate authentication and login security.
- Identify publicly accessible sensitive files and database backups.
- Assess PDF encryption and password security.
- Analyze document metadata for information disclosure.
- Evaluate the security impact of identified vulnerabilities.
- Provide actionable remediation recommendations.

## 📋 Assessment Information

| Parameter | Details |
|---|---|
| Project | Mediroza General Hospital |
| Assessment Type | External Black-Box Web Application Penetration Test |
| Target | `https://medirozahospital.com` |
| Program | NetworkWalks Cybersecurity Internship |
| Batch | B084 |
| Assignment | Week 4 |
| Testing Environment | Kali Linux |
| Browser | Firefox |
| Overall Risk | Critical |

## 🔍 Testing Methodology

The assessment followed a structured penetration-testing approach:

1. **Reconnaissance:** Domain information gathering, web technology fingerprinting, and robots.txt analysis.
2. **Scanning & Enumeration:** Directory discovery and identification of publicly exposed resources.
3. **Authentication Testing:** Login response analysis, username enumeration, and SQL injection validation.
4. **PDF Security Assessment:** PDF encryption inspection, hash extraction, and dictionary-based password testing.
5. **Metadata Analysis:** Extraction and examination of PDF metadata and correlation with exposed database records.
6. **Reporting & Remediation:** Documentation of security findings, risk assessment, and corrective recommendations.

## 🛠️ Tools & Technologies Used

| Tool | Purpose |
|---|---|
| Kali Linux | Penetration testing environment |
| WHOIS | Domain intelligence gathering |
| WhatWeb | Web technology fingerprinting |
| cURL | HTTP request and response analysis |
| Wget | File retrieval |
| Firefox Developer Tools | Manual application testing |
| grep & awk | Database inspection and data correlation |
| NetworkWalks Hash Calculator | PDF hash extraction |
| NetworkWalks Password Cracker | PDF password testing |
| pdf2john | PDF password hash extraction |
| John the Ripper | Offline password security testing |
| RockYou Wordlist | Dictionary-based password auditing |
| qpdf | PDF decryption and security inspection |
| ExifTool | PDF metadata analysis |

## 🚨 Vulnerability Assessment Results

A total of **6 security findings** were identified during the assessment.

| ID | Vulnerability | Severity | CWE |
|---|---|---|---|
| F-01 | SQL Injection – Patient Portal Authentication Bypass | Critical | CWE-89 |
| F-02 | Unauthenticated Database Backup Disclosure | High | CWE-538 |
| F-03 | Weak Password Protection on Patient PDFs | High | CWE-521 |
| F-04 | Sensitive PDF Metadata Disclosure | Medium | CWE-200 |
| F-05 | Username Enumeration | Low | CWE-204 |
| F-06 | Directory Listing on Legacy Directory | Low | CWE-548 |

## 🔬 Technical Findings

### 1. SQL Injection – Authentication Bypass

**Severity: Critical**

- Identified unsafe SQL input handling in the patient login functionality.
- Observed MySQL syntax errors during authentication testing.
- Successfully validated an authentication bypass.
- Confirmed access to protected patient portal functionality.

### 2. Unauthenticated Database Backup Disclosure

**Severity: High**

- Identified a publicly accessible SQL database backup.
- Confirmed that the backup could be retrieved without authentication.
- Identified exposed staff and shareholder records.
- Demonstrated the risk of sensitive organizational information disclosure.

### 3. Weak PDF Password Protection

**Severity: High**

- Inspected encryption settings of three pathology PDF reports.
- Extracted PDF password-auditing hashes.
- Performed dictionary-based password testing.
- Successfully recovered passwords for all three PDF documents.

### 4. Sensitive PDF Metadata Disclosure

**Severity: Medium**

- Extracted author, creator, producer, and comment metadata.
- Identified internal identifiers and software information.
- Discovered a legacy backup-directory reference.
- Correlated an internal identifier with an exposed staff record.

### 5. Username Enumeration

**Severity: Low**

- Tested authentication responses using existing and nonexistent usernames.
- Identified different error messages.
- Confirmed that login responses disclosed username validity.

### 6. Directory Listing

**Severity: Low**

- Identified an accessible legacy directory.
- Observed directory indexing.
- Discovered the exposed SQL database backup through the directory listing.

## 🛡️ Remediation Recommendations

| Finding | Recommended Remediation |
|---|---|
| SQL Injection | Implement parameterized SQL queries, secure authentication logic, and proper input handling. |
| Database Backup Exposure | Remove database backups from public directories and restrict backup storage access. |
| Weak PDF Passwords | Enforce strong, unique document passwords and authenticated user-specific downloads. |
| Metadata Disclosure | Remove unnecessary internal identifiers, comments, and software metadata. |
| Username Enumeration | Implement consistent authentication error messages, rate limiting, and monitoring. |
| Directory Listing | Disable directory indexing and restrict access to legacy directories. |

**Remediation Priority:** Address the critical SQL injection and publicly accessible database backup first, followed by PDF security and information-disclosure vulnerabilities.

## 📚 Key Learning Outcomes

This assessment provided practical exposure to:

- External black-box web application penetration testing.
- Reconnaissance and directory enumeration.
- SQL Injection identification and authentication bypass validation.
- Database backup exposure assessment.
- PDF encryption and password security testing.
- Document metadata extraction and analysis.
- Username enumeration and information disclosure.
- Vulnerability severity classification using CWE references.
- Technical security reporting and remediation planning.

## 📁 Repository Structure

```text
NETWORKWALKSEMMANUEL-B084-Week4-Penetration-Testing/
│
├── screenshots/
│   ├── Photo 1.jpeg
│   ├── Photo 2.jpeg
│   ├── Photo 3.jpeg
│   ├── Photo 4.jpeg
│   ├── Photo 5.jpeg
│   ├── Photo 6.jpeg
│   ├── Photo 7.jpeg
│   ├── Photo 8.jpeg
│   └── README.md
│
├── .gitignore
│
└── README.md
```

## 📝 Conclusion

The assessment demonstrated how multiple web application security weaknesses can combine to increase the risk of unauthorized access and sensitive information exposure.

The most significant findings were SQL Injection in the patient authentication process and the unauthenticated database backup disclosure.

The assessment highlights the importance of secure SQL query handling, strong authentication mechanisms, proper file access controls, document security, and regular vulnerability assessments.

## ⚠️ Disclaimer

This project is documented for educational and cybersecurity training purposes as part of the NetworkWalks Cybersecurity Internship.

Testing was conducted within the assigned and authorized assessment scope. The information presented is intended for security awareness, vulnerability analysis, and remediation purposes.

No patient information, confidential database records, recovered passwords, or sensitive credentials should be published in this repository.

---

**Project Domain:** Web Application Security | VAPT | Black-Box Penetration Testing | Vulnerability Assessment

**Program:** NetworkWalks Cybersecurity Internship – Batch B084, Week 4
