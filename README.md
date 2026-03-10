<div align="center">

<img src="docs/screenshots/banner.svg" width="100%" alt="ConduitShield"/>

<br>

[![Live](https://img.shields.io/badge/Live-Dashboard-D97706?style=flat-square)](https://siteq8.github.io/ConduitShield)
[![License](https://img.shields.io/badge/License-MIT-D97706?style=flat-square)](LICENSE)
[![Standards](https://img.shields.io/badge/IEC_62443-Aligned-D97706?style=flat-square)]()
[![NIST](https://img.shields.io/badge/NIST_800--82-Aligned-D97706?style=flat-square)]()
[![ATT&CK](https://img.shields.io/badge/MITRE_ATT%26CK-ICS-D97706?style=flat-square)]()
[![Dashboards](https://img.shields.io/badge/Dashboards-9-D97706?style=flat-square)]()

### Passive-first cybersecurity for OT, ICS, and IIoT

**One platform. Three modes. Nine dashboards.**

[Live Dashboard](https://siteq8.github.io/ConduitShield) · [Features](#features) · [Architecture](#architecture) · [Standards](#standards-alignment) · [Quick Start](#quick-start)

</div>

---

## Why ConduitShield

APIs are the #1 attack vector in IT. In OT, the attack surface is the **protocol layer** — Modbus writes, S7comm uploads, DNP3 commands — where a single unauthorized change can halt a plant or endanger safety.

Most cybersecurity tools are built for IT and retrofitted for OT. They actively scan, ignore zones and conduits, treat the plant like a flat LAN, and have no awareness of operational safety.

ConduitShield is **built for OT from the ground up**:

- **Passive-first** — SPAN/TAP visibility, no active scanning unless explicitly approved during a maintenance window
- **Zones & conduits native** — ISA/IEC 62443 segmentation is a first-class concept, not a report add-on
- **Safety-aware** — response automation never disrupts operations without explicit policy gates
- **OT protocol parsing** — Modbus, DNP3, S7comm, EtherNet/IP, OPC UA, BACnet, IEC 104, MQTT, CoAP
- **Three operational modes** — Discover, Defend, Respond — matching how OT security programs mature

---

## Dashboard Access

| Credential | Username | Password |
|-----------|----------|----------|
| **Admin** | `admin` | `OT@Secure2025` |

**Live:** [https://siteq8.github.io/ConduitShield](https://siteq8.github.io/ConduitShield)

---

## Features

### Three Modes

| Mode | Purpose |
|------|---------|
| **Discover** | Asset inventory, topology mapping, zone/conduit definition, protocol baselining |
| **Defend** | Access control, segmentation enforcement, vulnerability management, IoT lifecycle |
| **Respond** | Detection engineering, incident cases, OT playbooks, evidence preservation |

### Nine Dashboards

| # | Dashboard | Capability |
|---|-----------|------------|
| 1 | **Dashboard** | Security posture overview: 2,461 assets, Purdue Model zone health, real-time alerts, compliance score |
| 2 | **Assets** | Passive-discovered inventory: vendor, model, firmware, protocol, Purdue zone, IP, vulnerability status. 10 asset types across all Purdue levels |
| 3 | **Access** | Remote session monitoring with MFA enforcement, JIT access, session recording. Default credential detection with 3 active alerts |
| 4 | **Vulnerabilities** | Firmware/software correlation against ICS-CERT advisories. 6 real CVEs matched to inventory with CVSS scores, patch status, compensating controls |
| 5 | **IoT Controls** | Device onboarding queue, firmware update tracking with signature verification, certificate lifecycle, secure configuration compliance |
| 6 | **Detection** | MITRE ATT&CK for ICS mapping: 47 techniques covered, 8 detection rules shown with tactic mapping and last-triggered timestamps |
| 7 | **Incidents** | Active incident cases (P1-P4), OT-specific playbook for unauthorized PLC write (6-step: Isolate → Verify → Preserve → Assess → Restore → Report) |
| 8 | **Segmentation** | Zone/conduit policy builder: 12 zones, 34 conduits. Policy enforcement table showing allowed protocols, violations, and breach status per conduit |
| 9 | **Compliance** | Framework compliance: IEC 62443 (68%), NIST 800-82 (75%), NERC CIP (82%), MITRE ATT&CK (84%), CIS v8.1 (74%), CISA (65%). 1,247 total controls |

---

## Architecture

```
ConduitShield Platform
│
├── DISCOVER MODE
│   ├── Passive Network Discovery (SPAN/TAP)
│   ├── Full Asset Inventory (vendor, model, firmware, protocol, zone)
│   ├── Auto-built Topology with Purdue Levels
│   ├── Protocol-aware Parsing (Modbus, DNP3, S7comm, CIP, OPC UA)
│   └── Communication Baselines + Rogue Device Detection
│
├── DEFEND MODE
│   ├── Identity & Access Management (RBAC/ABAC, MFA, JIT)
│   ├── Privileged Access Workflow (session recording, command logging)
│   ├── Default Credential Detection & Forced Replacement
│   ├── Vulnerability Correlation (ICS-CERT, vendor advisories)
│   ├── Patch Workflow (assess → test → schedule → deploy → verify → rollback)
│   ├── Compensating Control Tracking
│   ├── Config Drift Detection & Golden Image Comparison
│   ├── SBOM Ingest & Supply Chain Mapping
│   ├── IoT Onboarding & Secure Configuration
│   ├── Certificate & Key Lifecycle Management
│   ├── Firmware Update Validation (signature, checksum, rollback)
│   ├── Zone/Conduit Policy Builder
│   ├── Segmentation Continuous Validation
│   └── Change Simulation (blast radius preview)
│
├── RESPOND MODE
│   ├── Event Collection (OT sensors, HMIs, SCADA, historians, firewalls)
│   ├── Process-aware Anomaly Detection
│   ├── MITRE ATT&CK for ICS Mapping (47 techniques)
│   ├── Audit Log Storage with Integrity Protection
│   ├── Incident Cases (severity, zones, impact, containment)
│   ├── OT-specific Playbooks
│   ├── Evidence Locker (logs, PCAPs, timelines, chain of custody)
│   ├── Safety-aware Response Gates
│   └── Contact Trees (vendors, operations, legal, responders)
│
└── PLATFORM
    ├── On-premises First (optional hybrid analytics)
    ├── Lightweight Collectors for Plants/Substations
    ├── Store-and-forward for Low-bandwidth Sites
    ├── API-first Integration (SIEM, SOAR, CMDB, IAM)
    └── Multi-site Tenancy (enterprise, MSSP)
```

---

## Standards Alignment

| Standard | Version | Coverage |
|----------|---------|----------|
| **ISA/IEC 62443** | 2018 | Zones/conduits, security levels, system requirements, component requirements |
| **NIST SP 800-82** | Rev 3 | OT security guide — network architecture, access control, monitoring |
| **NERC CIP** | v7 | Critical infrastructure protection for bulk electric systems |
| **MITRE ATT&CK for ICS** | v14 | 47 techniques mapped with detection rules and hunting queries |
| **CIS Controls** | v8.1 | Implementation groups 1-3 mapped to OT context |
| **CISA ICS Guidelines** | 2024 | Secure-by-design, default credential elimination, SBOM |
| **NIST IoT Cybersecurity** | NIST IR 8259 | Device identity, logical access, software update, telemetry |

---

## ICS Protocol Support

| Protocol | Port | Standard | Use Case |
|----------|------|----------|----------|
| Modbus/TCP | 502 | IEC 61158 | PLCs, RTUs, sensors |
| DNP3 | 20000 | IEEE 1815 | Substations, water/wastewater |
| S7comm/S7comm+ | 102 | Siemens | S7-300/400/1200/1500 PLCs |
| EtherNet/IP (CIP) | 44818 | IEC 61158 | Rockwell/Allen-Bradley |
| OPC UA | 4840 | IEC 62541 | HMIs, SCADA, historians |
| BACnet/IP | 47808 | ISO 16484-5 | Building management |
| IEC 60870-5-104 | 2404 | IEC 60870 | Power grid SCADA |
| MQTT | 1883 | ISO/IEC 20922 | IoT sensors, telemetry |
| CoAP | 5683 | RFC 7252 | Constrained IoT devices |
| TriStation | 1502 | Schneider | Safety instrumented systems |
| PROFINET | — | IEC 61158 | Siemens automation |
| Foundation Fieldbus | — | IEC 61158 | Process instrumentation |

---

## OT Incident Playbooks

ConduitShield includes OT-specific playbooks designed around safety and operational continuity:

| Playbook | Key Principle |
|----------|---------------|
| **Unauthorized PLC Write** | Isolate source, verify process state BEFORE any PLC action, compare against golden backup |
| **Ransomware on OT-adjacent** | Sever IT-OT conduit, verify DMZ integrity, check for lateral movement to L2/L1 |
| **Unauthorized Logic Change** | Freeze engineering access, diff current vs golden program, engage vendor if needed |
| **Unsafe Cross-zone Traffic** | Block at conduit firewall, investigate source, verify no process impact before enforcement |
| **Vendor Session Compromise** | Terminate session immediately, audit all changes made, rotate credentials, review logs |
| **Rogue Device Detection** | Port-disable at switch, capture traffic, identify device, assess blast radius |

---

## Quick Start

### Online

**[https://siteq8.github.io/ConduitShield](https://siteq8.github.io/ConduitShield)**

Login: `admin` / `OT@Secure2025`

### Local

```bash
git clone https://github.com/SiteQ8/ConduitShield.git
cd ConduitShield
open docs/index.html
```

---

## What Ships in v1

For v1, the feature set prioritizes **safe, passive capabilities** that deliver value without taking operational risks:

| Feature | Status |
|---------|--------|
| Passive asset discovery & inventory | Demo |
| Topology with Purdue zone mapping | Demo |
| Zone/conduit policy builder | Demo |
| Firmware vulnerability correlation (ICS-CERT) | Demo |
| Secure remote access monitoring | Demo |
| MITRE ATT&CK for ICS detections | Demo |
| Incident cases with OT playbooks | Demo |
| IoT device lifecycle controls | Demo |
| Multi-standard compliance dashboard | Demo |

---

## Red Flags This Tool Avoids

Based on NIST, CISA, and ISA/IEC 62443 guidance, ConduitShield is designed to avoid common OT security tool pitfalls:

| Red Flag | ConduitShield Approach |
|----------|----------------------|
| Active-scan only | Passive-first from SPAN/TAP |
| Relies on default credentials | Detects and forces replacement |
| Weak logging | Full audit trail with integrity protection |
| No patch visibility | Firmware/software version tracking + ICS-CERT correlation |
| Ignores OT safety | Safety-aware response gates, no auto-disruption |
| Flat network assumption | ISA/IEC 62443 zones & conduits as first-class concept |
| Vendor lock-in | API-first, open integration with SIEM/SOAR/CMDB |

---

## License

MIT — see [LICENSE](LICENSE).

---

<div align="center">
  <sub>ConduitShield — Passive-first cybersecurity for OT, ICS, and IIoT</sub><br>
  <sub>ISA/IEC 62443 · NIST SP 800-82 · NERC CIP · MITRE ATT&CK for ICS · CISA</sub><br>
  <sub><a href="https://github.com/SiteQ8">@SiteQ8</a> — Ali AlEnezi</sub>
</div>
