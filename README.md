# Building_Network_Lab-
Virtual cybersecurity lab on Proxmox with VLANs, pfSense, AD, DNS/DHCP, and Wazuh SIEM. 
EN:
# 🔐 Secure Enterprise Network Lab  

This project is my own **virtual enterprise cybersecurity environment**, built on a **Proxmox server**.  
The goal is to simulate a real corporate infrastructure with segmented VLANs, Active Directory, centralized user management, security features (firewall, IDS/IPS), and monitoring (SIEM).  

The project serves as a personal training lab for the role of a **Network Security Engineer**.  

---

## 🎯 Project Goals
- Build a network infrastructure similar to an enterprise environment.  
- Segment the network using VLANs and implement firewall rules.  
- Deploy centralized user management with Active Directory.  
- Provide core network services (DNS, DHCP, VPN).  
- Monitor events with IDS/IPS and SIEM (Wazuh).  
- Simulate attack scenarios and test detection.  
- Document all configurations and results for a professional portfolio.  

---

## 🛠️ Technologies Used
- **Proxmox VE** – virtualization platform  
- **pfSense** – firewall, VPN, IDS/IPS, VLAN routing  

---

## 🗺️ Network Topology
- **VLAN10 – Management** (infrastructure management, admin PC)  
- **VLAN20 – Users** (user workstations, Windows clients)  
- **VLAN30 – Servers** (AD/DNS/DHCP, web server, SIEM)  
- **WAN** – Internet (via pfSense)  

📌 *Topology diagram is stored in `/docs/topology-diagram.png`.*  

---

## 📂 Repository Structure
<pre>
secure-enterprise-lab/
│
├── README.md                  # Main project overview
│   
├── docs/                      # Documentation
│   │     
│   ├── topology.png            # Network diagram
│   │   
│   ├── topology.md             # Network legend
│   │     
│   └── network-plan.md         # VLANs, IP ranges, DNS, AD layout
│   
├── configs/                    # Exported configurations
│   
├── scripts/                    # Automation scripts
│
├── screenshots/                # Visual proofs
│
└── exports/                    # Logs & reports
    ├── logs/
    └── reports/
</pre>  
---

## 📋 Project Steps
1. Prepare Proxmox and required ISO images.  
2. Install pfSense and configure VLANs and firewall rules.  
3. Deploy Windows Server, configure AD, DNS, and DHCP.  
4. Join clients (Windows + Linux) to VLANs and the domain.  
5. Set up SIEM (Wazuh) and connect log sources.  
6. Perform security testing (scan, brute-force, access control).  
7. Document configurations and results.  

---

## ✅ Test Scenarios
- VLAN segmentation (users cannot access the management VLAN).  
- Client successfully joined to the domain and GPO applied.  
- Successful/failed VPN connection through pfSense.  
- Attack detection (Nmap scan, brute-force) by Suricata + Wazuh.  
- Event logging of user logins and security alerts in SIEM.  

---

## 📊 Deliverables
- Exported configurations (pfSense, DHCP, DNS).  
- Screenshots from AD, GPO, and Wazuh dashboards.  
- Logs and reports from test scenarios.  
- Network diagram.  

---

✍️ **Note:** This project is purely educational and serves as a hands-on training environment for cybersecurity and network security engineering.  

CZ:
# 🔐 Secure Enterprise Network Lab  

Tento projekt je mým vlastním **virtuálním enterprise prostředím pro kybernetickou bezpečnost**, postaveným na **Proxmox serveru**.  
Cílem je simulovat reálnou firemní infrastrukturu s oddělenými VLAN, Active Directory, centrální správou uživatelů, bezpečnostními prvky (firewall, IDS/IPS) a monitoringem (SIEM).  

Projekt slouží jako tréninková laboratoř pro pozici **Network Security Engineer**.  

---

## 🎯 Cíle projektu
- Vybudovat síťovou infrastrukturu podobnou enterprise prostředí.  
- Rozdělit síť pomocí VLAN a nasadit firewallová pravidla.  
- Zavést centrální správu uživatelů přes Active Directory.  
- Poskytovat síťové služby (DNS, DHCP, VPN).  
- Monitorovat události pomocí IDS/IPS a SIEM (Wazuh).  
- Testovat scénáře útoků a jejich detekci.  
- Dokumentovat postup a výsledky pro portfolio.  

---

## 🛠️ Použité technologie
- **Proxmox VE** – virtualizace  
- **pfSense** – firewall, VPN, IDS/IPS, VLAN routing  
- **Windows Server 2022** – Active Directory, DNS, DHCP  
- **Windows 10/11 Client** – připojený do domény  
- **Ubuntu Server** – web server, SSH server  
- **Ubuntu Desktop / Kali Linux** – klienti a testovací stanice  
- **Wazuh** – SIEM a monitoring logů  

---

## 🗺️ Síťová topologie
- **VLAN10 – Management** (správa infrastruktury, admin PC)  
- **VLAN20 – Users** (uživatelské stanice, Windows klienti)  
- **VLAN30 – Servers** (AD/DNS/DHCP, web server, SIEM)  
- **WAN** – Internet (přes pfSense)  

📌 *Diagram topologie je v `/docs/topology-diagram.png`.*  

---

## 📂 Struktura repozitáře

 viz nahoře v EN verzi

---

## 📋 Postup práce
1. Připravit Proxmox a potřebné ISO images.  
2. Nainstalovat pfSense, nakonfigurovat VLAN a firewall.  
3. Přidat Windows Server, nastavit AD, DNS a DHCP.  
4. Připojit klienty (Windows + Linux) do VLAN a domény.  
5. Nasadit SIEM (Wazuh), propojit logy.  
6. Testovat bezpečnostní scénáře (scan, brute-force, přístupová pravidla).  
7. Dokumentovat konfigurace a výsledky.  

---

## ✅ Testovací scénáře
- VLAN segmentace (uživatelé nemají přístup do management VLAN).  
- Přihlášení klienta do domény a aplikace GPO.  
- Úspěšné/selhané VPN připojení přes pfSense.  
- Detekce útoku (Nmap scan, brute-force) pomocí Suricata + Wazuh.  
- Evidence přihlášení uživatelů a security eventů v SIEM.  

---

## 📊 Výstupy
- Exportované konfigurace (pfSense, DHCP, DNS).  
- Screenshoty z AD, GPO a Wazuh dashboardu.  
- Logy a reporty z testovacích scénářů.  
- Síťový diagram.  

---

✍️ **Poznámka:** Projekt je čistě studijní a slouží k tréninku kybernetické bezpečnosti a network security inženýringu.  


