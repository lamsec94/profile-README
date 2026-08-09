# Hi, I'm Lamar Scott (@lamsec94)

Systems and infrastructure professional building and operating a production-grade, enterprise-style environment — used as both a learning platform and a portfolio of real infrastructure work.

---

## What I Run

A two-node Proxmox cluster running VMs and LXC containers across segmented VLANs, managed through OPNsense and documented end-to-end.

| Layer | Stack |
|---|---|
| Virtualization | Proxmox VE — dual-node cluster (su1/su2), PBS backups |
| Networking | OPNsense firewall, 5 VLANs, GS308EP managed switch, Suricata IDS |
| Identity | Active Directory (WS2022 + WS2025 dual-DC) |
| PKI | Enterprise Root CA (ADCS), wildcard *.homelab.local, 14 HTTPS services |
| Monitoring | Suricata IDS on OPNsense, GLPI Agent asset inventory across the fleet |
| Automation | Ansible, SSH pipelining, async patching (23 min to 2 min) |
| DNS | AdGuard Home, conditional forwarding to AD DNS, custom rewrites |
| Access | Nginx Proxy Manager, Tailscale subnet routing, GitHub remote |

---

## Infrastructure Topology
![Infrastructure Topology](./topology.png)

---

## Repositories
| Repo | What's Inside |
|---|---|
| homelab-runbooks | Operational runbooks — incident response, build guides, patching procedures |
| homelab-network-documentation | VLAN design, OPNsense config, switch assignments, network diagrams |
| active-directory-lab | AD OU design, GPOs, PKI/ADCS, dual-DC deployment, PowerShell provisioning |
| homelab-portfolio | Full architecture overview and infrastructure documentation landing page |
| glpi-itsm-deployment | GLPI ITSM platform, LDAP integration, intake forms, asset discovery |

---

## Skills
Linux, Windows Server, Active Directory, Proxmox VE, OPNsense, Ansible, Bash, PowerShell, Docker, PKI / ADCS, VLANs, DNS, Suricata, Git, ITIL

---

## Certifications
- CompTIA A+
- ITIL Foundation
- Google IT Support
- CompTIA Network+ (in progress)

---

## Contact
- Email: scottlamar05@gmail.com
- LinkedIn: linkedin.com/in/lamarscott
