# Research Report: The Importance of Patch Management

## 1. Introduction

A **security patch** is a piece of software released by a vendor to fix a known flaw in an operating system, application, firmware, or library — most commonly a security vulnerability that could otherwise be exploited by an attacker. **Patch management** is the organizational process built around applying these fixes consistently and on time.

According to NIST Special Publication 800-40 Revision 4, *Guide to Enterprise Patch Management Planning: Preventive Maintenance for Technology*, enterprise patch management is the process of identifying, prioritizing, acquiring, installing, and verifying the installation of patches, updates, and upgrades throughout an organization. NIST frames patching as a critical component of preventive maintenance for computing technologies — a cost of doing business and a necessary part of what organizations need to do in order to achieve their missions. Preventive maintenance through enterprise patch management helps prevent compromises, data breaches, operational disruptions, and other adverse events.

Patch management is fundamentally a cybersecurity activity because it directly closes the technical gaps that attackers rely on to gain unauthorized access, execute code, or move through a network. It is one part of the broader discipline of **vulnerability management** — the continuous cycle of identifying, evaluating, and remediating security weaknesses across an organization's assets. Vulnerability management is the umbrella process for finding and assessing weaknesses; patch management is one of the primary remediation actions used within that process to fix weaknesses with vendor-supplied updates.

Unpatched systems create security exposure because a known, publicly documented vulnerability — often with proof-of-concept exploit code freely available — remains open on a live system indefinitely. Every day that a patch is available but unapplied is a day an attacker can potentially exploit it. As shown in the WannaCry and Equifax case studies below, some major cybersecurity incidents were preventable because a patch already existed before the attack occurred.

---

## 2. Why Patches Matter

Vulnerabilities move through a predictable lifecycle:

**Vulnerability discovery → Vulnerability disclosure → CVE identification → Severity assessment → Exploit development/use → Patch/remediation → Verification**

Understanding this lifecycle explains why timely patching matters and where organizations most often fall behind.

### Vulnerability Discovery

Vulnerabilities can be discovered by many different parties, each with different incentives:

* **Security researchers** — independent professionals who analyze software for flaws, often publishing findings responsibly to vendors first.
* **Software vendors** — internal engineering and security teams that find issues during code review, testing, or after customer-reported incidents.
* **Penetration testers** — professionals hired to simulate attacks against an organization's systems, uncovering exploitable weaknesses under controlled conditions.
* **Bug bounty researchers** — independent researchers who search for vulnerabilities in exchange for financial rewards offered through formal vendor bug bounty programs.
* **Attackers** — malicious actors who discover vulnerabilities, including zero-days, for the purpose of exploitation rather than disclosure.

The party that discovers a vulnerability first has a major influence on how the rest of the lifecycle unfolds. Responsible disclosure by a researcher gives vendors time to prepare a patch before attackers learn of the flaw, whereas discovery by an attacker can mean exploitation happens before any patch exists.

### CVEs and Vulnerability Identification

**CVE** stands for **Common Vulnerabilities and Exposures**. The CVE system, maintained by the MITRE Corporation in coordination with the U.S. government, assigns a unique identifier, such as `CVE-2017-0144`, to publicly disclosed vulnerabilities.

This catalog gives the security industry — vendors, researchers, scanning tools, and defenders — a shared reference point for a specific vulnerability. CVE identifiers allow vulnerability scanners, patch management tools, threat intelligence feeds, and internal tracking systems to refer to the same issue.

### CVSS Scoring

**CVSS** stands for **Common Vulnerability Scoring System**. It is an open framework used to communicate the technical severity of a vulnerability on a scale of **0.0 to 10.0**.

CVSS provides organizations with a standardized measure of technical severity, including factors such as exploitability and the potential impact on:

* Confidentiality
* Integrity
* Availability

However, CVSS score alone does not determine patch priority. A high CVSS score reflects **technical severity**, not necessarily **organizational risk**.

For example, a high-severity vulnerability on an isolated system may represent less immediate risk than a moderately scored vulnerability on an internet-facing system that is actively being exploited.

This is why resources such as CISA's **Known Exploited Vulnerabilities (KEV) Catalog** are useful alongside CVSS. Organizations can consider active exploitation, asset criticality, internet exposure, and business impact when prioritizing vulnerabilities.

### Real-World Example: WannaCry and EternalBlue

In March 2017, Microsoft released **Security Bulletin MS17-010**, which patched a critical flaw in the Windows SMBv1 protocol. This flaw, catalogued as `CVE-2017-0144`, allowed an unauthenticated attacker to send specially crafted packets to a vulnerable Windows system on port 445 and achieve remote code execution with SYSTEM privileges.

The exploit that took advantage of this flaw became known as **EternalBlue**. Microsoft released the security update on March 14, 2017. However, the exploit later became publicly available when the Shadow Brokers leaked it on April 14, 2017.

On May 12, 2017, the **WannaCry** ransomware worm began spreading globally by scanning for and exploiting unpatched systems still vulnerable to EternalBlue.

WannaCry infected more than **230,000 computers across roughly 150 countries**, including organizations such as Spain's Telefónica and the United Kingdom's National Health Service (NHS). In the UK, approximately 80 NHS trusts were disrupted, resulting in cancelled appointments and ambulance diversions.

The critical fact for patch management is timing: when WannaCry hit in May 2017, the MS17-010 patch had already been available for approximately two months.

The incident demonstrates that the existence of a security patch does not provide protection by itself. Organizations must actually deploy and verify the patch.

### Real-World Example: Equifax Breach

On March 7, 2017, the Apache Software Foundation publicly disclosed a critical remote code execution vulnerability in the Apache Struts web framework, identified as `CVE-2017-5638`.

The vulnerability was patched on the same day it was announced. The following day, the Department of Homeland Security contacted Equifax, Experian, and TransUnion to notify them of the vulnerability. On March 9, 2017, an internal email notification was sent to Equifax administrators directing them to apply the Apache patch.

Despite this warning, the patch was not applied to all affected systems. Equifax's information security department ran scans on March 15, 2017, intended to identify systems vulnerable to the Apache Struts issue, but the scans failed to identify the vulnerability.

The flaw remained unpatched until July 29, 2017 — more than four months after the patch was released.

Attackers exploited the unpatched vulnerability and ultimately accessed sensitive information belonging to approximately **143–148 million people**, depending on the source.

Equifax ultimately reached a **$700 million settlement** to resolve federal and state investigations arising from the breach.

The lesson for patch management is that having a patch policy on paper is not the same as verified enforcement. Organizations must confirm that patches have actually been applied and that vulnerable systems are no longer exposed.

---

## 3. Consequences of Not Patching

### Data Breaches

Unpatched, publicly known vulnerabilities give attackers a documented path into a system. As the Equifax case demonstrates, attackers do not necessarily need to discover a new vulnerability themselves. They can monitor public vulnerability disclosures and target organizations that have not applied the corresponding fix.

Once initial access is gained, attackers may move laterally within a network to reach higher-value systems and exfiltrate sensitive data.

### Ransomware Attacks

Unpatched vulnerabilities can provide an initial access or propagation path for ransomware.

WannaCry is a clear example. Its ability to spread as a self-propagating worm depended on vulnerable Windows systems that had not received the MS17-010 patch.

Where the patch had been applied, WannaCry could not exploit the SMBv1 vulnerability to spread to that machine.

This demonstrates that patch management can reduce both the likelihood of compromise and the scale of an attack once it begins.

### Compliance Violations

Failing to maintain an adequate vulnerability and patch management program can contribute to non-compliance with regulatory and contractual security requirements.

Organizations may need to demonstrate that security policies are not only documented but also implemented, monitored, and enforced.

### Financial Penalties

The financial consequences of failing to patch can include:

* **Incident response costs** — forensic investigators, security consultants, and legal counsel.
* **Recovery costs** — rebuilding systems, restoring data, and applying deferred patches.
* **Business interruption** — lost revenue and productivity while affected systems are offline.
* **Regulatory penalties** — fines and settlements following security incidents.
* **Legal costs** — defending against lawsuits from affected customers or other parties.
* **Reputation damage** — loss of customer trust and brand value.

### Statistics

* The WannaCry attack resulted in estimated global financial damages ranging from **$4 billion to $8 billion**, according to industry analysis of the 2017 incident.
* UK Department of Health and Social Care estimates placed the initial NHS damages from WannaCry at approximately **$25 million**, with additional costs associated with IT support and system/data restoration.
* Equifax reached a **$700 million settlement** to resolve federal and state investigations following its 2017 breach.
* CISA's **Known Exploited Vulnerabilities Catalog** contains a large and continually growing number of vulnerabilities confirmed to have been exploited in the wild, demonstrating the ongoing importance of tracking and remediating known exploited vulnerabilities.

---

## 4. Patch Management Lifecycle

### 4.1 Discovery

The discovery phase involves building and maintaining a complete, accurate inventory of hardware and software assets across the organization.

This includes identifying:

* All operating systems in use, including version and build information.
* All applications and their installed software versions.
* Systems running outdated, unsupported, or otherwise vulnerable software.

An organization cannot effectively patch assets that it does not know it has.

Unknown or **shadow IT** systems represent a persistent blind spot because they may never enter the patch management process.

### 4.2 Assessment

Once assets are known, the assessment phase determines which vulnerabilities apply to them and how urgently each should be addressed.

This involves:

* Identifying vulnerabilities affecting specific software and versions.
* Reviewing relevant CVE entries.
* Reviewing CVSS severity scores.
* Checking whether vulnerabilities are actively exploited.
* Checking CISA's Known Exploited Vulnerabilities (KEV) Catalog.
* Considering asset criticality.
* Considering internet exposure.
* Considering potential business impact.

These factors should be combined to prioritize vulnerabilities rather than attempting to patch every vulnerability in the order it was published.

### 4.3 Testing

Before deployment to production, patches should be tested to confirm they do not introduce new problems.

Testing includes:

* **Compatibility testing** — confirming that the patch works with the organization's hardware and software configurations.
* **Application testing** — verifying that dependent applications continue to function.
* **Test/staging environments** — applying patches in a non-production environment.
* **Rollback procedures** — having a documented method to revert a patch if necessary.
* **Change management** — formally tracking and approving patch deployments.

### 4.4 Deployment

The deployment phase is where patches are applied to production systems.

Key elements include:

* Applying patches during scheduled maintenance windows.
* Using automated patch deployment tools.
* Having an emergency patching process for critical vulnerabilities.
* Prioritizing critical vulnerabilities ahead of lower-risk vulnerabilities.
* Using phased deployment where appropriate.

Critical vulnerabilities that are actively exploited should have an expedited remediation process rather than waiting for a normal maintenance cycle.

### 4.5 Verification

Patching is not complete until deployment has been verified.

Verification involves:

* Confirming that the patch was successfully installed.
* Checking installed software versions.
* Rescanning systems with vulnerability scanning tools.
* Confirming that the vulnerability has been remediated.
* Recording patch status.
* Investigating systems where the patch failed.

The Equifax breach demonstrates why verification is important. An instruction to patch does not guarantee that the patch was actually applied.

---

## 5. Best Practices: 7-Step Patch Management Checklist

* [ ] **1. Maintain a complete, continuously updated asset inventory.** An organization cannot patch systems it does not know exist. Maintain accurate information about hardware, operating systems, applications, and software versions.

* [ ] **2. Continuously monitor for new vulnerabilities affecting your assets.** Track vendor advisories, the CVE database, and vulnerability databases to identify vulnerabilities affecting systems in the environment.

* [ ] **3. Prioritize vulnerabilities using risk-based criteria, not severity score alone.** Consider CVSS severity, CISA KEV status, active exploitation, asset criticality, and internet exposure.

* [ ] **4. Test patches in a staging environment before production deployment.** Validate compatibility and application functionality and confirm that rollback procedures exist.

* [ ] **5. Deploy patches promptly using defined maintenance and emergency procedures.** Establish acceptable time-to-patch targets and expedited procedures for vulnerabilities under active exploitation.

* [ ] **6. Verify that patches were successfully installed and vulnerabilities are remediated.** Rescan patched systems and compare results with the asset inventory.

* [ ] **7. Continuously monitor and improve the patch management process.** Review patch cycle times, failure rates, and other performance indicators and improve policies, tools, and procedures as the environment changes.

---

## 6. Challenges and How to Overcome Them

### Legacy Systems

Many organizations operate unsupported operating systems or old applications that no longer receive vendor patches. Some systems are tightly connected to other applications, making upgrades difficult because of compatibility limitations, cost, downtime, or re-engineering requirements.

Organizations can reduce the risk through compensating controls such as:

* Network segmentation.
* System isolation.
* Strict firewall rules.
* Enhanced monitoring.
* Virtual patching where appropriate.
* Replacement planning.

Organizations should maintain a roadmap to replace or upgrade unsupported systems rather than allowing them to remain indefinitely.

### Downtime Concerns

Organizations may delay patches because applying them, particularly patches requiring system reboots, can interrupt critical business services.

Organizations can reduce downtime by:

* Scheduling patches during maintenance windows.
* Using phased or rolling deployments.
* Using redundant systems.
* Applying patches during low-usage periods.
* Automating deployment and verification.

### Testing Requirements

Patches can introduce compatibility problems, break application dependencies, or cause operational issues.

Organizations can manage this risk by:

* Using dedicated testing and staging environments.
* Maintaining verified backups.
* Defining rollback procedures.
* Testing application dependencies.
* Using formal change management.

---

## 7. Conclusion

Patch management sits at the intersection of technical execution and organizational discipline. As NIST SP 800-40 Revision 4 frames it, patching should be treated as preventive maintenance for computing technologies and as a necessary part of organizational security.

The WannaCry and Equifax incidents demonstrate that serious security incidents can occur when organizations fail to apply patches that were already available.

A mature patch management program treats each stage of the lifecycle — **discovery, assessment, testing, deployment, and verification** — as essential.

Organizations should use resources such as the CVE database, CVSS, and CISA's KEV Catalog to prioritize vulnerabilities intelligently. Legacy systems, downtime concerns, and testing requirements should be managed through appropriate controls rather than becoming reasons for indefinite patching delays.

Effective patch management is therefore a continuous process of identifying vulnerabilities, prioritizing risk, applying patches, verifying remediation, and improving the process over time.

---

## 8. References

1. Souppaya, M., & Scarfone, K. (2022). *NIST Special Publication 800-40 Revision 4: Guide to Enterprise Patch Management Planning: Preventive Maintenance for Technology.* National Institute of Standards and Technology.
   https://csrc.nist.gov/pubs/sp/800/40/r4/final

2. Cybersecurity and Infrastructure Security Agency (CISA). *Known Exploited Vulnerabilities Catalog.* U.S. Department of Homeland Security.
   https://www.cisa.gov/known-exploited-vulnerabilities-catalog

3. National Vulnerability Database (NVD). *CVE-2017-0144 Detail.*
   https://nvd.nist.gov/vuln/detail/CVE-2017-0144

4. Electronic Privacy Information Center (EPIC). *Equifax Data Breach — Timeline and Analysis.*
   https://archive.epic.org/privacy/data-breach/equifax/

5. The Apache Software Foundation. *Media Alert: The Apache Software Foundation Confirms Equifax Data Breach Due to Failure to Install Patches Provided for Apache Struts Exploit.*
   https://news.apache.org/foundation/entry/media-alert-the-apache-software

---
