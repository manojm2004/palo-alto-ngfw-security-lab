# 🛡️ Palo Alto Networks Next-Generation Firewall (NGFW) Security Lab

Hands-on deployment of a virtual **Palo Alto NGFW (PAN-OS)** in EVE-NG, securing enterprise zone boundaries, enforcing stateful security policies, and translating internal traffic via PAT/Source NAT.

## 📌 Features & Configurations
- **Security Zones:** Segmented into `Trust` (Internal LAN), `Untrust` (Public Gateway / ISP), and `DMZ` (Web & Application Servers).
- **Stateful Security Policies:** 
  - Allow Trust -> Untrust (Web-Browsing, SSL, DNS).
  - Deny Untrust -> Trust (Default drop with logging enabled).
  - Allow Untrust -> DMZ (Strict TCP 443 with App-ID inspection).
- **NAT Architecture:**
  - Dynamic IP and Port (PAT / Overload) for outbound internet egress.
  - Static 1-to-1 Destination NAT (DNAT) mapping external public IP to internal DMZ web server.
- **Monitoring & Logging:** Log forwarding, traffic inspection, and threat identification through PAN-OS CLI and Web GUI.

---
*Created by Manoj M | Network & Security Engineer*
