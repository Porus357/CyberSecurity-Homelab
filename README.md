Cybersecurity Homelab Project

Completion Date: February 2024Project Type: Hands-on Simulation (No Code)Tools Used: pfSense, Security Onion, Kali Linux, Ubuntu

🔍 Overview

This homelab project was designed to simulate a real-world cybersecurity environment where attacks and defense mechanisms can be practiced safely. The environment includes both offensive and defensive tools configured in a virtualized setup.

🧰 Tools and Setup

pfSense – Used as a virtual firewall/router for network segmentation and traffic control.

Security Onion – Deployed as a SIEM for real-time monitoring and threat detection.

Kali Linux – Offensive attacker machine for carrying out simulated attacks.

Ubuntu – Used both as an administrator and victim system.

📡 Network Topology

![network topology](https://github.com/user-attachments/assets/87b0ad5e-78b3-46e4-8b92-daba0c0911ac)

🛡️ Simulation Scenarios

Detected port scans and suspicious network behavior via Security Onion

Configured firewall rules and VLAN segmentation using pfSense

Demonstrated lateral movement detection

Exploited a vulnerable Windows target using Metasploit's windows/smb/ms08_067_netapi module

🎥 Project Videos

The following video resources are available in the video/ folder:

firewall_configuration.mp4 – pfSense firewall rules and VLAN setup

lab_simulation.mp4 – End-to-end attack simulation and detection demo

📄 Documentation

More details can be found in the docs/ folder:

configuration_notes.md – VLAN layout and pfSense firewall configuration

attack_scenarios.md – Description of attacks, including MS08-067 exploitation

tools_used.md – Toolchain and version information

📌 Key Outcomes

Understood real-world detection mechanisms

Practiced safe exploitation and detection techniques

Built a reusable test lab for continuous practice

🧠 Skills Demonstrated

Network segmentation and hardening

IDS/IPS deployment

Attack simulation and threat detection
