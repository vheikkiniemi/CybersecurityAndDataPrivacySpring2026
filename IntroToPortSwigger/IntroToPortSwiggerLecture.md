# 🔐 Introduction to PortSwigger, OWASP, CWE, CVE & CyBOK

> [!NOTE]
> The material was created with the help of ChatGPT and Copilot.

---

## 🌍 Understanding OWASP, CWE, and CVE

### 💡 Why Are They Important?
Cybersecurity aims to identify, classify, and mitigate vulnerabilities in software and web applications.  
Three key ecosystems work together to achieve this:

| Framework | Purpose | Maintained By |
|------------|----------|---------------|
| [**OWASP**](https://owasp.org/) | Best practices, tools & education for web app security | Global community |
| [**CWE**](https://cwe.mitre.org/) | Standardized list of software weaknesses | MITRE |
| [**CVE**](https://www.cve.org/) | Public catalog of real-world vulnerabilities | MITRE / NIST |

> ⚠️ **Remember:** OWASP tells *what* to protect, CWE tells *why* it fails, and CVE shows *where* it happened.

---

## 🧱 What is OWASP?

**Full Name:** *Open Web Application Security Project*  
**Focus:** Improving the security of software through collaboration and transparency.

### 🔎 Key Resources
- 🧩 [**OWASP Top 10**](https://owasp.org/www-project-top-ten/): The 10 most critical web application security risks.
- 🕵️‍♀️ [**OWASP ZAP**](https://www.zaproxy.org/): Free vulnerability scanner for web apps.
- 📘 [**ASVS**](https://owasp.org/www-project-application-security-verification-standard/): Verification standard for secure development.

**Examples from OWASP Top 10 (2021):**
- 🧱 [**A01: Broken Access Control**](https://owasp.org/Top10/A01_2021-Broken_Access_Control/)  
- 🧬 [**A03: Injection (e.g., SQL Injection, XSS)**](https://owasp.org/Top10/A03_2021-Injection/)

> 💬 *OWASP = Awareness + Education + Tools*

---

## 🧩 What is CWE?

**Full Name:** *Common Weakness Enumeration*  
**Goal:** Provide a structured language for describing weaknesses in software design and implementation.  
**Maintained by:** [MITRE](https://www.mitre.org/)

### 🧠 Example
- **[CWE-79: Cross-Site Scripting (XSS)](https://cwe.mitre.org/data/definitions/79.html)**  
  🔍 *Description:* An application includes untrusted data in a web page without validation.  
  🎯 *Impact:* Attackers can inject malicious scripts into users’ browsers.

> 💡 *CWE = Helps developers understand the root causes behind vulnerabilities.*

---

## 🧬 What is CVE?

**Full Name:** *Common Vulnerabilities and Exposures*  
**Purpose:** Public list of confirmed cybersecurity vulnerabilities.  
**Maintained by:** [MITRE](https://www.mitre.org/)  
**Linked database:** [NVD (National Vulnerability Database)](http://nvd.nist.gov/)  
**CVE database**: [CVEdetails](https://www.cvedetails.com/)

### 🧠 Example
- **[CVE-2022-22965: Spring4Shell](https://www.cve.org/CVERecord?id=CVE-2022-22965)**  
  🔍 *Affected:* Spring Framework versions < 5.3.18 / < 5.2.20  
  🎯 *Impact:* ☠️ Remote Code Execution (RCE)

> 💡 *CVE = The address book of real vulnerabilities.*

---

## 🔗 How OWASP, CWE, and CVE Work Together

| Layer | Focus | Example |
|-------|--------|----------|
| **OWASP** | Defines security principles & top risks | Injection, Broken Access Control |
| **CWE** | Categorizes underlying weaknesses | CWE-89 (SQL Injection) |
| **CVE** | Records real-world vulnerabilities | CVE-2022-41671 |

---

### 🧠 Example: SQL Injection
1. **OWASP:** [A03:2021 – Injection](https://owasp.org/Top10/A03_2021-Injection/)  
2. **CWE:** [CWE-89](https://cwe.mitre.org/data/definitions/89.html) – Improper neutralization of SQL commands  
3. **CVE:** [CVE-2022-41671](https://www.cve.org/CVERecord?id=CVE-2022-41671) – SQL injection exploit in production software

🧰 *Use OWASP ZAP or Burp Suite to detect and mitigate this issue.*

---

### 🌐 Example: Cross-Site Scripting (XSS)
1. **OWASP:** [A07:2021 – Cross-Site Scripting](https://owasp.org/Top10/A07_2021-Identification_and_Authentication_Failures/)  
2. **CWE:** [CWE-79](https://cwe.mitre.org/data/definitions/79.html) – Improper input handling  
3. **CVE:** [CVE-2024-23111](https://www.cve.org/CVERecord?id=CVE-2024-23111)

🛠️ *Mitigation: Always sanitize and escape user input.*

---

## 🧰 Tools & Best Practices

### 🔍 Using OWASP, CWE, and CVE Together
- 🧪 **OWASP Tools:**  
  - Run [ZAP](https://www.zaproxy.org/) scans for vulnerability discovery.  
  - Follow [ASVS](https://owasp.org/www-project-application-security-verification-standard/) for secure design.
- 🧱 **CWE:** Identify the *root cause* of weaknesses in your code.  
- 📡 **CVE:** Monitor [NVD](http://nvd.nist.gov/) regularly to stay updated on vulnerabilities in your stack.

> ✅ *Combine detection (OWASP), diagnosis (CWE), and tracking (CVE) for a strong security posture.*

---

## 🧭 Summary

- **OWASP** → *Best practices and tools*  
- **CWE** → *Weakness classification*  
- **CVE** → *Real-world vulnerability tracking*  

🧩 **Together:** they form the foundation of vulnerability management in modern cybersecurity.

---

# 🧰 Introduction to PortSwigger

## 🚀 What is PortSwigger?

**Founded:** 2006 by *Dafydd Stuttard*  
**Mission:** Empower professionals and developers to secure the web.

### 🏆 Known For
- 🧠 [**Web Security Academy**](https://portswigger.net/web-security): Free, hands-on training platform  
- 🧰 **Burp Suite:** Industry-leading toolkit for penetration testing and vulnerability scanning

---

## 🧩 Burp Suite Editions

| Edition | Description | Use Case |
|----------|--------------|----------|
| 🧾 **Community** | Free version for basic learning | Students & beginners |
| 💼 **Professional** | Full-feature manual testing toolkit | Pentesters |
| 🏢 **Enterprise** | Automated large-scale scanning | Organizations |

**Key Features:**  
- Active and passive scanning  
- Repeater, Intruder, Decoder tools  
- Extensibility via BApp Store plugins  

---

## 📘 Web Security Academy
Interactive labs covering:
- OWASP Top 10
- SQL Injection
- XSS
- CSRF  
…and much more 🔥  

🎓 *Practical, gamified learning environment.*

---

## 🤝 How PortSwigger Connects to OWASP, CWE, and CVE

| Connection | Description |
|-------------|--------------|
| **PortSwigger + OWASP** | Tests OWASP Top 10 vulnerabilities |
| **PortSwigger + CWE** | Maps findings to CWE categories |
| **PortSwigger + CVE** | Identifies CVE-referenced vulnerabilities |
| **All Together** | OWASP → CWE → CVE → PortSwigger tools verify and teach them |

---

### Example: SQL Injection Workflow
1. **OWASP:** A03:2021 Injection  
2. **CWE:** CWE-89  
3. **CVE:** CVE-2024-24141  
4. **PortSwigger:** Burp Suite identifies and reports it.  
   Web Security Academy teaches mitigation techniques.

> 💬 *Burp Suite bridges theory and real-world exploitation.*

---

## 💪 Why PortSwigger Matters

✅ **Security Professionals:** Automate & customize scans  
✅ **Developers:** Learn by doing, find & fix early  
✅ **Organizations:** Scale secure development practices  

> 🧠 *Education meets execution.*

---

## 💼 Portswigger and alternatives

🛠️  **PortSwigger (Burp Suite + Web Security Academy)** = hands-on *tool + guided labs* focused on web application security and pentesting workflows → *how to test and fix* web apps, and for manual/automated testing practice.

* **TryHackMe & similar platforms** = *learning platforms / CTF-style labs* offering structured learning paths across many domains (web, infra, forensics, crypto). Best for onboarding newcomers, gamified practice, and broad blue/red team skill-building.
* Use them together: **TryHackMe for broad skill-building and motivation → PortSwigger for deep, professional web-app testing skills.**

---

### 🧩 TryHackMe — what it is & where it shines

* [**TryHackMe**](https://tryhackme.com/)
* **What:** Guided, browser-accessible “rooms” with learning paths (e.g., Web Fundamentals, Offensive Pentesting, Blue Team, Cloud). Includes small VMs, step-by-step hints, badges and assessments.
* **Strengths:** Beginner-friendly, gamified progression, clear learning paths.
* **Weaknesses:** Labs are not always realistic production web apps; less emphasis on using professional GUIs like Burp until later paths.
* **Cost:** Freemium — many rooms free; subscription unlocks pro rooms, VMs and extra features.

---

### 🔀 Other TryHackMe-style alternatives

* [**Hack The Box (HTB)**](https://www.hackthebox.com/) — more advanced labs and boxes; leaning more to intermediate/advanced learners and realistic boxes; good for CTF-style training and red team practice.
* [**PentesterLab**](https://pentesterlab.com/) — focused web-app exercises with detailed writeups; strong for web-app exploitation learning (commercial, some free content).
* [**CyberSecLabs**](https://www.cyberseclabs.org/) — enterprise training ranges: used for team training and blue/red scenarios; often paid and enterprise-oriented.
* [**OverTheWire**](https://overthewire.org/wargames/) — free community CTFs and VM images for offline practice; excellent for challenge-based learning and lab creation.
* [**Offensive Security Proving Grounds (OSCP labs)**](https://www.offsec.com/products/proving-grounds/) — realistic, professional-level pentest sandbox for exam prep (paid, advanced).

---

## 🔁 Burp Suite alternatives

### **OWASP ZAP (Zed Attack Proxy)**

* Open-source DAST/proxy scanner that’s beginner-friendly, scriptable and widely used in education and CI pipelines. Best if you want a free, community-supported tool for automated and manual testing.
* **Pros:** Free, active community, good automation/scripting.
* **Cons:** Some advanced manual features are weaker than Burp Pro.

---

### **Invicti (formerly Netsparker)**

* Commercial enterprise-grade web & API scanner focusing on high-accuracy, proof-based detection and SDLC/DevSecOps integration — strong for teams that need automated, low-noise scanning at scale.
* **Pros:** Accurate verification, enterprise-scale reporting & triage.
* **Cons:** Commercial cost; heavier than a manual pentest tool.

---

### **Acunetix (by Invicti)**

* Commercial automated web scanner with strong crawling and detection for modern apps (including SPA/API). Good when you want fast automated coverage and developer-friendly remediation reports.
* **Pros:** Strong crawling, developer reports, CI/CD integrations.
* **Cons:** Commercial licensing; can produce false positives depending on use.

---

### **Specialized tools & smaller alternatives**

* **Nikto** — simple webserver scanner (good for labs).
* **Wfuzz / ffuf** — powerful fuzzing for custom exploit discovery.
* **Qualys / Veracode / Checkmarx** — enterprise suites for DAST/SAST where policy & compliance matter. 

---

# 🧩 Introduction to CyBOK

## 🌐 What is CyBOK?
**Full Name:** [Cyber Security Body of Knowledge](https://www.cybok.org/)  
**Purpose:** Provide a unified knowledge framework for cybersecurity.  
**Organized into:**  
- Web & Application Security  
- Software Security  
- Vulnerability Management  

🎯 *Goal: Standardize cybersecurity understanding for education, research, and practice.*

---

## 🧠 CyBOK’s Connection to Others

| Integration | Description |
|--------------|-------------|
| **CyBOK + OWASP** | Promotes OWASP Top 10 integration during secure SDLC |
| **CyBOK + CWE** | Adopts structured software weakness modeling |
| **CyBOK + CVE** | Stresses tracking of real-world vulnerabilities |
| **CyBOK + PortSwigger** | Encourages hands-on labs and active testing |

---

### Example: Cross-Site Scripting (XSS)
1. **CyBOK:** Covered under *Web & Mobile Security → 4.1.5 XSS*  
2. **OWASP:** A07:2021 – Cross-Site Scripting  
3. **CWE:** CWE-79  
4. **CVE:** CVE-2022-46769 – Apache Sling CMS  
5. **PortSwigger:** Labs on discovering and fixing XSS flaws

🧩 *CyBOK = theory, PortSwigger = practice.*

---

## 🧱 Why CyBOK Matters

✨ **Standardization:** Common vocabulary for cybersecurity concepts  
🎓 **Education:** Connects academic theory and hands-on tools  
🔐 **Security Impact:** Helps teams identify, categorize, and mitigate vulnerabilities comprehensively  

---

# 🧾 Final Summary

### 🔁 Bringing It All Together

| Framework | Purpose |
|------------|----------|
| **OWASP** | Defines risks & provides tools |
| **CWE** | Categorizes weaknesses |
| **CVE** | Lists real-world vulnerabilities |
| **PortSwigger** | Detects & teaches mitigation |
| **CyBOK** | Theoretical foundation & knowledge map |

> 🧠 *Together, they form a complete learning and operational ecosystem for web application security.*

---

## 🌟 Takeaway
> 💬 “Security isn’t one tool or one list — it’s a continuous learning process combining awareness, classification, and action.”

🔒 **Use CyBOK + OWASP + CWE + CVE + PortSwigger** →  you get a **holistic cybersecurity mindset** that blends **education, practice, and real-world defense**.

---