# 🔐 Cybersecurity Internship Projects

> **Cybersecurity Analyst Internship Portfolio**
>
> A collection of cybersecurity research, vulnerability assessment, web security, and practical security projects completed during my cybersecurity internship.

---

## 👨‍💻 About This Repository

This repository contains my work completed as part of my **Cybersecurity Analyst Internship**.

The projects demonstrate my understanding of cybersecurity through a combination of:

- 🔎 Security research
- 🛡️ Vulnerability analysis
- 🌐 Web application security
- 🔐 Security assessment
- 📊 Risk analysis
- 🧪 Practical cybersecurity exercises
- 📝 Technical documentation

The goal of this repository is to demonstrate both **theoretical knowledge and practical cybersecurity skills**.

---

# 📂 Projects

| # | Project | Type | Status |
|---|---|---|---|
| **1** | The Importance of Patch Management | 🔎 Research | ✅ Completed |
| **2** | Nikto Web Vulnerability Scanning | 🧪 Practical | ✅ Completed |
| **3** | SQL Injection Exploitation | 🧪 Practical | ✅ Completed |

---

# 📌 Project 1 — The Importance of Patch Management

### 🔎 Research Project

This project examines the importance of patch management and explains why unpatched systems remain a significant cybersecurity risk.

### Topics Covered

- Patch management fundamentals
- Vulnerability management lifecycle
- CVE identification
- CVSS scoring
- Vulnerability discovery
- Vulnerability assessment
- Patch testing
- Patch deployment
- Patch verification
- Risk-based patch prioritization
- Legacy systems
- Downtime concerns
- Patch testing challenges

### 🌍 Real-World Case Studies

#### WannaCry / EternalBlue

- `CVE-2017-0144`
- Microsoft MS17-010
- Windows SMBv1
- Ransomware propagation
- Failure to apply an available security patch

#### Equifax Breach

- `CVE-2017-5638`
- Apache Struts
- Failure to apply a security update
- Vulnerability scanning failure
- Large-scale data exposure

### 🛠️ Technologies / Resources

- Markdown
- GitHub
- CVE
- CVSS
- CISA KEV Catalog
- NIST SP 800-40
- Vulnerability management concepts

### 📄 Report

➡️ **[Read the Patch Management Research Report](./patch_management_report.md)**

---

# 📌 Project 2 — Nikto Web Vulnerability Scanning

### 🧪 Practical Security Assessment

This project demonstrates the use of **Nikto** to perform an automated vulnerability scan against a locally hosted DVWA web application.

The objective was to identify common web server security issues, analyze the scanner output, categorize findings, and provide remediation recommendations.

### 🔍 Activities Performed

- Installed and verified Nikto
- Configured a local DVWA test environment
- Performed a basic Nikto scan
- Saved scan results to a text file
- Analyzed reported security issues
- Categorized findings by severity
- Documented remediation recommendations
- Captured screenshots of the scanning process
- Documented Nikto's limitations
- Compared Nikto with Nmap

### 🛡️ Findings Included

The scan identified issues including:

- Missing `X-Content-Type-Options`
- Missing `Content-Security-Policy`
- Missing `Strict-Transport-Security`
- Missing `Permissions-Policy`
- Missing `Referrer-Policy`
- Exposed login/admin functionality
- Deprecated `X-Frame-Options` configuration

### 🛠️ Technologies / Tools

- Kali Linux
- Nikto
- Nginx
- DVWA
- Linux terminal
- Web security testing
- Markdown
- Git & GitHub

### 📄 Project

➡️ **[Open the Nikto Vulnerability Scanning Project](./nikto-vulnerability-scanning/)**

---

# 📌 Project 3 — SQL Injection Exploitation

### 🧪 Practical Web Application Security

This project demonstrates controlled SQL Injection testing against **DVWA running locally**.

The exercise progressed from a baseline request to SQL Injection testing and database table enumeration.

### 🔍 Activities Performed

- Configured DVWA with Medium security
- Established a normal baseline request
- Tested SQL Injection behavior
- Demonstrated Boolean-based SQL Injection
- Retrieved multiple database records
- Enumerated database table names
- Attempted column enumeration
- Intercepted and inspected HTTP requests using Burp Suite
- Documented successful and unsuccessful tests
- Created a shell script documenting the exploitation process
- Developed remediation recommendations

### 💥 SQL Injection Results

The Boolean SQL Injection test:

```text
1 OR 1=1
