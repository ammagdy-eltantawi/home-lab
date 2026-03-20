# DNS Security Implementation using AdGuard Home (Docker on Raspberry Pi)

## Overview

This project demonstrates the deployment of a DNS-based security control using AdGuard Home on a Raspberry Pi using Docker Compose.

The solution acts as a private DNS resolver that filters traffic, blocks malicious domains, and provides visibility into DNS queries.

---

## Architecture

Client Devices → Raspberry Pi (AdGuard Home) → Internet

All DNS traffic is routed through the Raspberry Pi for filtering and monitoring.

---

## Environment

- Raspberry Pi (Linux)
- Docker Engine
- Docker Compose

---

## Implementation

- Deployed AdGuard Home using Docker Compose
- Configured as the primary DNS server for personal devices
- Enabled DNS filtering using blocklists
- Configured persistent storage using Docker volumes
- Enabled query logging for monitoring

---

## Docker Deployment

The service is containerized using Docker Compose to ensure:

- Portability
- Easy management
- Persistent configuration
- Isolated execution

---

## Security Controls

### DNS Filtering
- Blocks malicious, phishing, and tracking domains

### Network Control
- DNS queries are forced through a controlled resolver (Raspberry Pi)

### Logging and Monitoring
- Query logs provide visibility into DNS requests and behavior

---

## Risks and Mitigation

### Open DNS Exposure
- Mitigation: Restrict access to local network only using firewall rules

### Unencrypted DNS
- Mitigation: Use DNS over HTTPS (DoH) or DNS over TLS (DoT)

### Resource Constraints
- Mitigation: Lightweight containerized deployment on Raspberry Pi

---

## Key Takeaways

- DNS is a critical security enforcement point
- Containerization simplifies deployment and management
- DNS visibility enhances threat detection
- Local DNS control reduces attack surface

---

## Screenshots

### Dashboard
![Dashboard](screenshots/dashboard.png)

### Query Log
![Query Log](screenshots/query-log.png)

### Blocking Statistics
![Blocking](screenshots/blocking-stats.png)

### Settings
![Settings](screenshots/settings.png)

---

## Future Improvements

- Integration with centralized logging or SIEM
- Alerting on suspicious DNS activity
- Remote monitoring dashboard
