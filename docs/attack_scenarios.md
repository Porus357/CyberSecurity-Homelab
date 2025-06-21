# Attack Scenarios

This lab demonstrates simulated real-world attacks within a controlled virtual network. Offensive actions were carried out from the ATTACKVLAN to assess detection and response capabilities.

## 🔓 1. MS08-067 Exploitation

* **Exploit Used**: `windows/smb/ms08_067_netapi`
* **Tool**: Metasploit Framework
* **Attacker Machine**: Kali Linux (ATTACKVLAN)
* **Target Machine**: Windows XP/Vista vulnerable system (TARGETVLAN)
* **Outcome**: Remote shell obtained; confirmed unauthenticated remote code execution

## 🔁 2. Lateral Movement

* Performed post-exploitation enumeration
* Scanned other systems in TARGETVLAN using Nmap
* Checked for open SMB shares and attempted credential reuse

## 📈 3. SIEM Detection

Security Onion was deployed to monitor and detect:

* SMB anomalies from ATTACKVLAN to TARGETVLAN
* Exploit signature for `ms08_067`
* Lateral movement patterns

Alerts were visible via the Security Onion dashboard (Hunt/Kibana). This validated the lab’s ability to detect real threat behavior.
