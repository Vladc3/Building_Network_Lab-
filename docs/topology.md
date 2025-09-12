| Název        | VLAN        | OS                        | Role / Popis                                                    |
| ------------ | ----------- | ------------------------- | --------------------------------------------------------------- |
| **MikroTik** | WAN         | RouterOS                  | Hraniční router, připojení do WAN, směrování do pfSense         |
| **pfSense**  | 10/20/30/40 | FreeBSD (pfSense)         | Firewall, segmentace VLAN, IDS/IPS, VPN, NAT, pravidla přístupu |
| **ADMIN01**  | VLAN10      | Windows 11 Pro            | Admin PC pro správu serverů a firewallu                         |
| **MON01**    | VLAN10      | Ubuntu 22.04 LTS          | Monitoring/utility server (např. Zabbix/Prometheus)             |
| **USER01**   | VLAN20      | Windows 10 Pro            | Běžný uživatel – pracovní stanice                               |
| **USER02**   | VLAN20      | Windows 10 Pro            | Běžný uživatel – pracovní stanice                               |
| **KALI01**   | VLAN20      | Kali Linux                | Pen-testing klient, bezpečnostní testy                          |
| **AD01**     | VLAN30      | Windows Server 2022       | Active Directory, DNS, DHCP server                              |
| **WAZ01**    | VLAN30      | Ubuntu 22.04 LTS          | Wazuh SIEM server, log management                               |
| **WEB01**    | VLAN30      | Windows Server 2022 (IIS) | Interní web server (intranet/app hosting)                       |
| **GUEST01**  | VLAN40      | Windows/Linux             | Notebook návštěvníka (internet only)                            |

------------------------------------------------------------------------------------------------------------------------------

| Name         | VLAN        | OS                        | Role / Description                                             |
| ------------ | ----------- | ------------------------- | -------------------------------------------------------------- |
| **MikroTik** | WAN         | RouterOS                  | Border router, WAN connection, routing to pfSense              |
| **pfSense**  | 10/20/30/40 | FreeBSD (pfSense)         | Firewall, VLAN segmentation, IDS/IPS, VPN, NAT, access control |
| **ADMIN01**  | VLAN10      | Windows 11 Pro            | Admin PC for managing servers and firewall                     |
| **MON01**    | VLAN10      | Ubuntu 22.04 LTS          | Monitoring/utility server (e.g., Zabbix/Prometheus)            |
| **USER01**   | VLAN20      | Windows 10 Pro            | Standard user – workstation                                    |
| **USER02**   | VLAN20      | Windows 10 Pro            | Standard user – workstation                                    |
| **KALI01**   | VLAN20      | Kali Linux                | Pen-testing client, security testing                           |
| **AD01**     | VLAN30      | Windows Server 2022       | Active Directory, DNS, DHCP server                             |
| **WAZ01**    | VLAN30      | Ubuntu 22.04 LTS          | Wazuh SIEM server, log management                              |
| **WEB01**    | VLAN30      | Windows Server 2022 (IIS) | Internal web server (intranet/app hosting)                     |
| **GUEST01**  | VLAN40      | Windows/Linux             | Guest laptop (internet only)                                   |


