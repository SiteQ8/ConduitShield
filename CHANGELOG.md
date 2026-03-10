# Changelog

## [1.0.0] - 2026-03-10

### Initial Release
- Interactive GUI platform with full OT security lifecycle
- Login screen with demo credentials
- Overpass Mono + Overpass typography (industrial aesthetic)
- Amber (#D97706) accent on dark (#111214) background

### Dashboard Features
- **Dashboard:** Security posture, Purdue zone health, real-time alerts
- **Assets:** Passive-discovered inventory (10 demo assets, 7 Purdue levels)
- **Access:** Remote session monitoring, MFA enforcement, default credential alerts
- **Vulnerabilities:** ICS-CERT advisory correlation (6 real CVEs), patch workflow
- **IoT Controls:** Device onboarding, firmware updates, certificate lifecycle
- **Detection:** MITRE ATT&CK for ICS (8 techniques with detection rules)
- **Incidents:** Active cases, OT playbook (Unauthorized PLC Write, 6 steps)
- **Segmentation:** Zone/conduit policy (6 conduits, protocol enforcement)
- **Compliance:** 6 frameworks (IEC 62443, NIST 800-82, NERC CIP, ATT&CK, CIS, CISA)

### Standards Alignment
- ISA/IEC 62443 (zones, conduits, security levels)
- NIST SP 800-82 Rev 3
- NERC CIP v7
- MITRE ATT&CK for ICS v14
- CIS Controls v8.1
- CISA ICS Guidelines 2024
- NIST IoT Cybersecurity (IR 8259)

### Design Philosophy
- Passive-first discovery (no active scanning by default)
- Safety-aware response (no auto-disruption without policy gates)
- OT protocol native (Modbus, DNP3, S7comm, EtherNet/IP, OPC UA, etc.)
- Three operational modes: Discover, Defend, Respond
