# HackForgeBreakOut - Penetration Testing Report

This repository contains the full penetration testing walkthrough report for the **HackForgeBreakOut** machine (Debian 11 target). 

## 🛠️ Tools & Technologies Used
* **Reconnaissance:** `arp-scan`, `nmap`, `enum4linux`
* **Interception:** Burp Suite Community Edition
* **Exploitation:** Brainfuck Decoding, Bash Reverse Shells, Netcat C2 Channel
* **Privilege Escalation:** Linux Capabilities Exploitation (`cap_dac_read_search` on `tar`)

## 🔑 Key Vulnerabilities Exploited
1. **Information Disclosure:** Plaintext/encoded developer comments in source code leaking user credentials.
2. **Weak Credential Storage:** Insecure storage of legacy backup credentials (`.old_pass.bak`).
3. **Privilege Escalation via Linux Capabilities:** The `tar` utility was misconfigured with `cap_dac_read_search`, allowing an unprivileged user to archive and read sensitive files like `/etc/shadow`.

---
*Note: This assessment was conducted as part of the Cyvero Cyber Security School training curriculum.*
