# vsftpd 2.3.4 Security Assessment

A controlled cybersecurity lab assessment of the known backdoor vulnerability associated with **vsftpd 2.3.4** on an intentionally vulnerable **Metasploitable 2** system.

The project demonstrates the process of identifying a vulnerable service, validating the vulnerability in an isolated lab environment, documenting the resulting access, analyzing the security impact, and providing remediation recommendations.

## 🎯 Objectives

* Identify exposed services on the target system
* Detect the vulnerable `vsftpd 2.3.4` FTP service
* Analyze the identified vulnerability
* Validate the vulnerability in an authorized lab environment
* Document proof-of-concept evidence
* Verify the resulting access
* Analyze potential security impact
* Provide remediation recommendations

## 🧪 Lab Environment

| Component          | Details              |
| ------------------ | -------------------- |
| Target             | Metasploitable 2     |
| Tester             | Kali Linux           |
| Environment        | Isolated Virtual Lab |
| Vulnerable Service | FTP                  |
| Service Version    | vsftpd 2.3.4         |
| Port               | TCP/21               |

## 🔍 Assessment Methodology

The assessment followed this workflow:

```text
Host Discovery
      ↓
Service Enumeration
      ↓
Version Identification
      ↓
Vulnerability Identification
      ↓
Proof of Concept
      ↓
Access Verification
      ↓
Impact Analysis
      ↓
Remediation
```

## 🛠️ Tools Used

* Kali Linux
* Nmap
* Metasploit Framework
* Metasploitable 2

## 🔎 Service Enumeration

The target was scanned to identify exposed services and determine the versions running on the system.

Example command:

```bash
nmap -sS -sV <TARGET_IP>
```

The assessment identified FTP running on TCP port 21 and reported the `vsftpd 2.3.4` service.

## 🚨 Vulnerability

### vsftpd 2.3.4 Backdoor

The identified service is associated with a known backdoor vulnerability that can allow unauthorized command execution under vulnerable conditions.

**Severity:** Critical

**Affected Service:** FTP

**Affected Port:** TCP/21

## 🧪 Proof of Concept

The vulnerability was validated in the isolated Metasploitable 2 laboratory environment using the Metasploit Framework.

The evidence directory contains screenshots documenting:

1. Service enumeration
2. Exploit identification
3. Exploit configuration
4. Exploitation result
5. Access verification

## 🔓 Access Verification

Following successful exploitation, access was verified using appropriate system commands.

Example verification:

```bash
whoami
id
hostname
```

The output was documented as evidence of the access obtained during the authorized laboratory assessment.

## ⚠️ Security Impact

If a vulnerable service of this type were exposed in a real production environment, successful exploitation could potentially result in:

* Unauthorized command execution
* System compromise
* Modification or deletion of files
* Installation of malicious software
* Sensitive data exposure
* Further attacks against other systems

## 🛡️ Remediation Recommendations

* Upgrade vulnerable software to a secure supported version
* Apply security patches
* Disable FTP if it is not required
* Replace FTP with more secure alternatives such as SFTP
* Restrict access to FTP using firewall rules
* Allow access only from trusted systems where required
* Continuously monitor exposed services
* Perform regular vulnerability assessments

## 📸 Evidence

Evidence collected during the authorized lab assessment is available in:

```text
evidence/
```

The screenshots demonstrate the vulnerability identification, exploitation process, and access verification.

## 📁 Repository Structure

```text
vsftpd-234-security-assessment/
│
├── README.md
│
├── documentation/
│   └── vulnerability-report.md
│
├── evidence/
│   ├── 01-nmap-enumeration.png
│   ├── 02-metasploit-search.png
│   ├── 03-exploit-configuration.png
│   ├── 04-exploitation-result.png
│   └── 05-access-verification.png
│
└── scans/
    └── nmap-scan.txt
```

## 📄 Detailed Report

For the complete assessment, methodology, findings, impact analysis, and remediation recommendations, see:

`documentation/vulnerability-report.md`

## ⚠️ Disclaimer

This project was performed exclusively in an authorized and isolated cybersecurity laboratory environment using an intentionally vulnerable system.

Do not attempt to exploit systems or services without explicit authorization.

## 👤 Author

**Aditya Kashinath Bagade**

Cybersecurity Student | SOC / Security Enthusiast
