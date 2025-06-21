Configuration Notes

🧱 Network Design

This lab simulates a segmented network using pfSense with the following virtual LANs (VLANs):

SECURITYMANAGEMENTVLAN – Hosts administrative systems and Security Onion SIEM

TARGETVLAN – Contains vulnerable machines for exploitation

ATTACKVLAN – Houses attacker tools and offensive VMs

WAN – Simulates external access

🔧 pfSense Configuration

Interfaces & Subnets

Each VLAN was configured with its own subnet and mapped to virtual interfaces:

SECURITYMANAGEMENTVLAN: 192.168.10.0/24

TARGETVLAN: 192.168.20.0/24

ATTACKVLAN: 192.168.30.0/24

WAN: DHCP or NAT-connected interface for simulated internet

Firewall Rules (Screenshots in /images/)

WAN

Default allow rule for external communication.

SECURITYMANAGEMENTVLAN

Anti-lockout rule

Allows access to HTTP (80), HTTPS (443), DNS (53)

Blocks inbound traffic from other VLANs

TARGETVLAN

Allows HTTP, HTTPS, DNS

Explicitly blocks traffic from TARGETVLAN to SECURITYMANAGEMENTVLAN

ATTACKVLAN

Allows outbound traffic to TARGETVLAN

Blocks outbound traffic to SECURITYMANAGEMENTVLAN

🧠 Design Principles

Network segmentation was used to simulate a real corporate network where attackers are isolated.

Firewall rules were tightly controlled to limit lateral movement.

SIEM visibility was ensured by routing all VLAN traffic through Security Onion in SECURITYMANAGEMENTVLAN.