# Hi, I'm Lamar Scott (@lamsec94)

Systems and infrastructure professional building and operating a production-grade, enterprise-style environment — used as both a learning platform and a portfolio of real infrastructure work.

---

## What I Run

A two-node Proxmox cluster running VMs and LXC containers across segmented VLANs, managed through OPNsense and documented end-to-end.

| Layer | Stack |
|---|---|
| Virtualization | Proxmox VE — dual-node cluster (su1/su2), PBS backups |
| Networking | OPNsense firewall, 5 VLANs, GS308EP managed switch, Suricata IDS |
| Identity | Active Directory — dual domain controller, Windows Server 2025, all FSMO roles consolidated |
| PKI | Enterprise Root CA (ADCS), wildcard certificate, 15 HTTPS services |
| Monitoring | Suricata IDS on OPNsense, GLPI Agent asset inventory across the fleet |
| Automation | Ansible — 12 hosts, 6 inventory groups, SSH pipelining and async patching (23 min to 2 min) |
| DNS | AdGuard Home, conditional forwarding to AD DNS, custom rewrites |
| Access | Nginx Proxy Manager, Tailscale subnet routing, GitHub remote |

---

## Infrastructure Topology

![Infrastructure Topology](./topology.png)

---

## Recent Work

Migrated an Enterprise Root CA between domain controllers with verified key continuity, then rebuilt and re-promoted the source domain controller on licensed media.

The problem being solved was architectural rather than operational: Active Directory replicates between domain controllers, but a Certificate Authority does not. That made a permanent, non-replicating role dependent on a single host — and the migration had to be sequenced so the only copy of the CA key was never on a machine about to be wiped. Verified by thumbprint and serial match rather than by service status, so every previously issued certificate remained trusted with no client-side changes.

Write-up: [certificate-authority.md](https://github.com/lamsec94/active-directory-lab/blob/main/docs/certificate-authority.md)

---

## Repositories

| Repo | What's Inside |
|---|---|
| [Portfolio](https://github.com/lamsec94/Portfolio) | Full architecture overview and infrastructure documentation landing page |
| [active-directory-lab](https://github.com/lamsec94/active-directory-lab) | AD OU design, GPOs, PKI/ADCS and CA migration, dual-DC deployment, PowerShell provisioning |
| [Network-documentation](https://github.com/lamsec94/Network-documentation) | VLAN design, OPNsense config, DNS architecture, firewall policy |
| [Glpi-itsm-deployment](https://github.com/lamsec94/Glpi-itsm-deployment) | GLPI ITSM platform, LDAP integration, intake forms, asset discovery |
| [Runbooks](https://github.com/lamsec94/Runbooks) | Operational runbooks — incident response, build guides, patching procedures |

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
