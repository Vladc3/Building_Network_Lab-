# Network Plan

## Summary
IP addressing uses private 10.10.X.0/24 ranges for easy scalability and clarity. pfSense is the routing/gateway device inside the lab (WAN behind MikroTik). Windows AD provides internal DNS and DHCP services for VLAN20/30 per plan below.

---

## VLANs & Subnets

| VLAN  | Name       | Subnet          | Gateway      | DHCP Range                    | Notes                            |
|-------|------------|-----------------|--------------|-------------------------------|----------------------------------|
| 10    | Management | 10.10.10.0/24   | 10.10.10.1   | 10.10.10.100–10.10.10.200     | Admin & monitoring devices       |
| 20    | Users      | 10.10.20.0/24   | 10.10.20.1   | 10.10.20.100–10.10.20.220     | Workstations, Kali testing       |
| 30    | Servers    | 10.10.30.0/24   | 10.10.30.1   | DHCP disabled (static IPs)    | AD, DNS, DHCP, SIEM, Web servers |
| 40    | Guests     | 10.10.40.0/24   | 10.10.40.1   | 10.10.40.50–10.10.40.200      | Internet-only; isolated          |

**Notes:** Gateways are pfSense interfaces for each VLAN. AD/DHCP runs on AD01 (VLAN30), except guest/User DHCP which can be served by AD DHCP scopes.

---

## IP Address Allocation (Static)

| Device   | VLAN | IP Address     | Hostname | Role |
|----------|------|----------------|----------|------|
| MikroTik | WAN  | (public or ISP) | MKT01   | Edge router / upstream gateway |
| pfSense  | WAN  | DHCP / public   | PF_WAN  | pfSense WAN (connected to MikroTik) |
| pfSense  | 10   | 10.10.10.1      | PF_MGMT | pfSense gateway (Management) |
| pfSense  | 20   | 10.10.20.1      | PF_USERS| pfSense gateway (Users) |
| pfSense  | 30   | 10.10.30.1      | PF_SERV | pfSense gateway (Servers) |
| pfSense  | 40   | 10.10.40.1      | PF_GUEST| pfSense gateway (Guests) |
| AD01     | 30   | 10.10.30.10     | AD01    | Domain Controller, DNS, DHCP |
| WAZ01    | 30   | 10.10.30.11     | WAZ01   | Wazuh SIEM / Log server |
| WEB01    | 30   | 10.10.30.12     | WEB01   | Internal web server (IIS) |
| MON01    | 10   | 10.10.10.11     | MON01   | Monitoring server / utility |
| ADMIN01  | 10   | DHCP / static   | ADMIN01 | Admin workstation |
| USER01   | 20   | DHCP            | USER01  | Workstation |
| USER02   | 20   | DHCP            | USER02  | Workstation |
| KALI01   | 20   | DHCP / static   | KALI01  | Pen-test machine |
| GUEST01  | 40   | DHCP            | GUEST01 | Guest laptop |
| GUEST02  | 40   | DHCP            | GUEST02 | Guest device |

---
