# Cybersecurity Homelab

> Status: Planning

A segmented virtual lab for practicing defensive security, infrastructure hardening, centralized logging, detection engineering, and incident response in an isolated environment.

## Goals

- Build a reproducible security lab using personally owned systems and test data.
- Practice network segmentation, identity management, endpoint telemetry, and secure administration.
- Forward Windows, Linux, and network logs to a central analysis platform.
- Generate controlled test activity and document detections and response steps.
- Produce portfolio-quality diagrams, screenshots, and technical write-ups without exposing secrets.

## Planned architecture

| Zone | Planned systems | Purpose |
|---|---|---|
| Management | Administrator workstation or jump host | Restricted administration |
| User | Windows client | Endpoint and identity testing |
| Server | Windows Server and Linux server | Directory, application, and system telemetry |
| Security | SIEM/log platform | Collection, search, dashboards, and alerts |
| Test | Security testing VM | Authorized simulations inside the lab |
| Network | Virtual firewall/router | Segmentation, filtering, and traffic visibility |

The final architecture diagram will be added to `docs/architecture/`.

## Project phases

- [ ] Document hardware, hypervisor, and network requirements.
- [ ] Create isolated virtual networks and firewall rules.
- [ ] Deploy Windows and Linux systems from clean images.
- [ ] Configure identity, least-privilege accounts, and secure remote administration.
- [ ] Enable endpoint, authentication, DNS, firewall, and system logging.
- [ ] Deploy the central log platform and validate ingestion.
- [ ] Create baseline dashboards and alert-health checks.
- [ ] Run safe simulations and collect evidence.
- [ ] Document containment, recovery, and lessons learned.
- [ ] Publish sanitized diagrams and final results.

## Planned repository structure

```text
.
├── README.md
├── docs/
│   ├── architecture/
│   ├── build-notes/
│   └── lessons-learned/
├── configs/
│   ├── firewall/
│   ├── linux/
│   └── windows/
├── detections/
├── simulations/
└── evidence/
```

## Evidence to publish

- Network and data-flow diagrams
- Sanitized configuration excerpts
- Log-source inventory and validation results
- Dashboard and alert screenshots
- Detection test cases and observed events
- Troubleshooting notes and lessons learned

## Success criteria

The lab is successful when all expected systems are isolated from production networks, required telemetry reaches the analysis platform, at least five controlled scenarios generate explainable alerts, and the environment can be rebuilt from the documentation.

## Safety

This project is for systems I own or am explicitly authorized to test. Simulations will remain isolated from employer, customer, and public infrastructure. Credentials, private addresses, company data, and unsanitized logs will never be committed.

## References

- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
- [MITRE ATT&CK](https://attack.mitre.org/)
