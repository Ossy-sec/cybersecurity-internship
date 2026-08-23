# Research Report: Social Engineering Attacks

## 1. Introduction

**Social engineering** is the use of deception and psychological manipulation to persuade people to reveal information, provide access, or perform an action that weakens security. Instead of primarily exploiting a technical vulnerability, social engineering exploits human factors such as trust, urgency, fear, curiosity, authority, and the desire to be helpful.

Social engineering is considered one of the most effective attack vectors because it can bypass technical security controls by convincing legitimate users to perform actions themselves. SANS reported in its 2025 Security Awareness Report that **80% of surveyed organizations ranked social engineering as their number-one human-related risk**. The report was based on responses from more than 2,700 security awareness practitioners across more than 70 countries.

CISA also identifies phishing as a form of social engineering in which threat actors impersonate trusted individuals or organizations to obtain sensitive information or network access. Successful phishing can result in data breaches, identity fraud, malware infections, ransomware, and other security incidents.

The effectiveness of social engineering demonstrates that cybersecurity requires more than firewalls, endpoint protection, and encryption. Organizations must also protect the human element through security awareness, strong authentication, verification procedures, and well-defined reporting processes.

---

## 2. Phishing

### 2.1 Definition and How It Works

**Phishing** is a social engineering technique in which an attacker sends a deceptive message designed to persuade a victim to reveal information, click a malicious link, open an attachment, transfer money, or perform another unsafe action.

A typical phishing attack can follow these stages:

1. The attacker identifies or impersonates a trusted person or organization.
2. The attacker creates a convincing message.
3. The message creates urgency, fear, curiosity, or another psychological trigger.
4. The victim is directed to a malicious link, attachment, website, or communication channel.
5. The attacker collects credentials, information, money, or establishes access to the victim's system.

CISA describes phishing as an attack in which a threat actor poses as a trustworthy colleague, acquaintance, or organization and uses email, text messages, or phone calls to persuade victims to provide sensitive information or network access.

### 2.2 Types of Phishing

| **Type** | **Description** |
|---|---|
| **Spear phishing** | A highly targeted phishing attack aimed at a specific individual or small group. The attacker uses information about the target to make the message more convincing. |
| **Whaling** | A form of spear phishing targeting senior executives or other high-value individuals, often involving financial transfers or sensitive information. |
| **Vishing** | Voice phishing conducted through phone calls or other voice communications. Attackers may impersonate IT support, banks, government agencies, or other trusted organizations. |
| **Smishing** | Phishing conducted through SMS or other text messages, commonly using fake delivery notifications, banking alerts, account warnings, or other urgent messages. |

CISA notes that spearphishing by voice can involve attackers impersonating trusted sources and creating urgency or alarm to persuade victims to provide access or perform an action.

### 2.3 Case Study: The 2011 RSA SecurID Breach

In March 2011, attackers targeted RSA Security through spear-phishing emails sent to employees. The emails used a subject related to a staffing plan and included a malicious Excel attachment. Opening the attachment exploited a vulnerability and installed a backdoor on the targeted system.

The attackers used the initial compromise to gain further access and obtain information related to RSA's SecurID authentication system. The incident demonstrated how a carefully crafted phishing message can provide attackers with an initial foothold inside an organization.

The case is particularly important because RSA was itself a major security company. The incident demonstrated that technical security controls cannot completely eliminate the risk created when employees are manipulated into opening malicious content.

### 2.4 Prevention Recommendations

1. **Use email authentication and filtering.** Implement technologies such as SPF, DKIM, and DMARC and use email security controls to detect malicious messages and attachments.

2. **Provide regular security awareness training.** Employees should learn how to identify suspicious messages and should regularly practice reporting simulated phishing attempts.

3. **Use multifactor authentication (MFA).** MFA provides an additional security layer if a password is stolen. Organizations should prefer phishing-resistant MFA where practical. CISA recommends MFA as an important protection against account compromise.

4. **Create an easy reporting process.** Employees should have a simple way to report suspicious emails, messages, and calls to the security team. CISA specifically recommends reporting suspicious communications rather than interacting with them.

---

## 3. Pretexting

### 3.1 Definition

**Pretexting** is a social engineering technique in which an attacker creates a believable false scenario to persuade a target to provide information, grant access, or perform an action.

The attacker may impersonate:

- IT support
- A manager
- A company executive
- A supplier
- A bank employee
- A government official
- A coworker

### 3.2 How Attackers Build a False Scenario

A successful pretexting attack often involves research before direct interaction.

The attacker may collect information from:

- Company websites
- Social media
- LinkedIn
- Public employee directories
- Job descriptions
- Previous data breaches
- Public company announcements

The attacker then uses these details to make the false identity and story appear legitimate.

For example, an attacker may impersonate an IT employee and claim that a user's account requires urgent verification. The attacker may already know the employee's name, department, manager, and internal terminology, making the request more convincing.

The objective is to establish enough trust that the victim performs the requested action without independently verifying it.

### 3.3 Case Study: The July 2020 Twitter Hack

In July 2020, attackers conducted a coordinated social engineering attack against Twitter employees. According to a U.S. Department of Justice filing referencing Twitter's own statement, attackers successfully targeted employees who had access to internal systems and tools.

The attackers used employee information and impersonation techniques to convince targeted staff members to provide access. They ultimately gained access to internal tools and compromised approximately 130 high-profile Twitter accounts.

The compromised accounts included accounts belonging to prominent individuals and organizations. Attackers used the accounts to promote a cryptocurrency scam.

The incident demonstrated that even organizations with strong technical security controls can be compromised when attackers successfully manipulate employees with privileged access.

### 3.4 Prevention Measures

1. **Require independent verification for sensitive requests.** Employees should verify unusual requests through a trusted communication channel rather than using contact information provided by the requester.

2. **Limit unnecessary public information.** Organizations should reduce the amount of sensitive employee and internal information publicly available to attackers.

3. **Use role-based access and dual approval.** Sensitive actions such as account resets, administrative changes, and financial transfers should require appropriate authorization and, where practical, approval from more than one person.

---

## 4. Baiting

### 4.1 Physical and Digital Baiting

**Baiting** is a social engineering technique in which an attacker offers something attractive or interesting to persuade a victim to perform an unsafe action.

Baiting relies heavily on:

- Curiosity
- Greed
- Desire for free content
- Desire to help others
- Interest in unexpected opportunities

### 4.2 Physical Baiting

Physical baiting commonly involves leaving an infected removable device, such as a USB drive, where a target is likely to find it.

The device may have a tempting label such as:

- "Salary Information"
- "Confidential"
- "Employee Records"
- "Important Documents"

The objective is to make the victim connect the device to a computer and open its contents.

### 4.3 Digital Baiting

Digital baiting uses attractive online content to persuade users to download or execute something malicious.

Examples include:

- Fake software
- Pirated applications
- Fake job offers
- Fake documents
- Malicious advertisements
- Fake prizes
- Fake updates

### 4.4 Case Study: USB Drop Experiment and Stuxnet

A controlled USB-drop experiment conducted by security researchers found that **48% of people interacted with USB drives that had been intentionally left in public locations**. The experiment demonstrated how curiosity and the desire to identify or return a lost device can encourage risky behavior.

A more serious real-world example is **Stuxnet**, the highly sophisticated malware discovered in 2010. Stuxnet is widely associated with the use of removable media as part of its propagation into isolated environments.

These examples demonstrate why removable media can represent a security risk even in environments where network access is heavily restricted.

### 4.5 Prevention Measures

1. **Restrict removable media.** Organizations should use endpoint controls to restrict unauthorized USB devices and scan approved removable media for malicious content.

2. **Train employees not to use unknown devices.** Employees should be instructed to give unidentified USB drives and other removable media to IT or security staff rather than connecting them to organizational systems.

3. **Restrict software installation and downloads.** Users should not have unnecessary administrative privileges, and organizations should use application controls and web filtering to reduce malicious downloads.

---

## 5. Quid Pro Quo

**Quid pro quo** is a social engineering technique in which an attacker offers a service, benefit, or reward in exchange for information or access.

For example, an attacker may impersonate IT support and claim to be fixing a technical problem. The attacker may then ask the employee to provide credentials or install remote-access software.

It differs from baiting because the attacker offers a direct service or benefit rather than simply placing an attractive object or file in front of the victim.

### Prevention

Organizations should:

- Train employees never to provide passwords or credentials in response to unsolicited support requests.
- Establish clear and trusted IT support channels.
- Require employees to independently verify the identity of support personnel.
- Prevent unauthorized remote-access software installation.

---

## 6. Comparison Table

| **Attack Type** | **Primary Target** | **Psychological Lever Exploited** | **Best Countermeasure** |
|---|---|---|---|
| **Phishing** | Employees with access to email, systems, or financial information | Urgency, authority, fear, curiosity | Email security + awareness training + MFA |
| **Pretexting** | Employees who can provide information or grant access | Trust, authority, familiarity | Independent verification + least privilege |
| **Baiting** | Employees with access to devices or the internet | Curiosity, greed, desire to help | Removable-media controls + security awareness |
| **Quid Pro Quo** | Employees who can provide information or technical access | Reciprocity and desire to receive assistance | Trusted support channels + identity verification |

---

## 7. Organisational Recommendations: 5-Point Employee Security Awareness Training Checklist

- [ ] **1. Provide recurring security awareness training.** Training should cover phishing, spear phishing, whaling, vishing, smishing, pretexting, baiting, and other relevant social engineering techniques.

- [ ] **2. Conduct regular simulated attacks.** Organizations should use controlled phishing simulations and other authorized exercises to measure employee behavior and improve awareness.

- [ ] **3. Establish a fast reporting mechanism.** Employees should have a simple way to report suspicious emails, messages, calls, and other activities.

- [ ] **4. Teach verification habits.** Employees should independently verify unusual requests involving credentials, financial transfers, account changes, sensitive data, or system access.

- [ ] **5. Tailor training according to job role and risk.** Finance, HR, IT support, executives, and administrators should receive additional training relevant to the attacks most likely to target their responsibilities.

Security awareness should be continuous rather than a one-time activity. CISA recommends phishing awareness, reporting suspicious activity, strong passwords, MFA, and secure software practices as important defenses.

---

## 8. Conclusion

Social engineering attacks demonstrate that cybersecurity is not only a technical problem. Attackers can bypass strong technical controls by manipulating legitimate users into providing information, granting access, or performing unsafe actions.

**Phishing, pretexting, and baiting** use different techniques but share the same fundamental objective: manipulating human behavior to achieve an attacker's goal.

Organizations should therefore combine employee awareness with technical and administrative controls. Security awareness training, phishing simulations, MFA, email security, independent verification, least-privilege access, removable-media controls, and clear reporting procedures can significantly reduce the likelihood and impact of successful social engineering attacks.

A strong security culture should make secure behavior the normal response to suspicious requests rather than relying only on employees to recognize every possible deception.

---

## 9. References

1. **Cybersecurity and Infrastructure Security Agency (CISA).** *Phishing.* U.S. Department of Homeland Security.  
   https://www.cisa.gov/sites/default/files/publications/phishing-infographic-508c.pdf

2. **Cybersecurity and Infrastructure Security Agency (CISA).** *Phishing — Simple Tips.*  
   https://www.cisa.gov/sites/default/files/publications/Phishing%20General%20Security%20Postcard_6.24.2021_508cV2.pdf

3. **SANS Institute.** *Security Awareness Report 2025: Embedding a Strong Security Culture.*  
   https://www.sans.org/press/announcements/security-awareness-report-2025/

4. **SANS Institute.** *Methods for Understanding and Reducing Social Engineering Attacks.*  
   https://www.sans.org/white-papers/36972/

5. **U.S. Department of Justice.** *Complaint regarding the July 2020 Twitter hack.*  
   https://www.justice.gov/

6. **SANS Institute.** *Top Three Ways Cyber Attackers Target You.*  
   https://www.sans.org/newsletters/ouch/top-ways-attackers-target-you/

---

**Report compiled for cybersecurity internship / portfolio submission purposes.**