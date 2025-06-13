# Security Onion IDS Project

## Overview

Network intrusion detection system implementation using Security Onion - a comprehensive open-source platform for network security monitoring and threat detection.

**Core Components:** Suricata, Zeek, Elasticsearch, Kibana, Wazuh

**System Requirements:** 8GB+ RAM, 4+ cores, 200GB+ storage, 2+ NICs

## Deployment Scenarios

### 1. Standalone Mode with Dual NIC
**Architecture:** Single-node with separated management and monitoring interfaces
- **Use Case:** Small networks, educational environments, testing
- **Benefits:** Simple deployment, cost-effective, isolated traffic
- **Demo:** [Standalone Mode Demo](https://youtu.be/bWiu8lMXAZk?si=wuvnwz9h18eOClaS)

![Standalone Architecture](img/standalone-architecture.png)

### 2. pfSense Firewall Integration
**Architecture:** Security Onion integrated with pfSense for perimeter defense
- **Use Case:** Comprehensive network security, traffic filtering + monitoring
- **Benefits:** Enhanced threat coverage, centralized management, coordinated response
- **Demo:** [pfSense Integration Demo](https://youtu.be/HT8qZro5x00?si=-r-8OZ2qNsrbV93Q)

![pfSense Integration](img/pfsense-integration.png)

### 3. Internal Network Deployment
**Architecture:** Focus on east-west traffic monitoring and lateral movement detection
- **Use Case:** Internal threat monitoring, insider detection, lateral movement
- **Benefits:** Internal traffic analysis, behavior analytics, asset monitoring
- **Demo:** [Internal Network Demo](https://youtu.be/_C9MXBDSYEU?si=vYywR-h7iumJpBQG)

![Internal Network](img/internal-network.png)

## Advanced Solutions

### 1. Cloud-Native SIEM
**Architecture:** Container-based deployment using Docker/Kubernetes
- **Features:** Auto-scaling, multi-region, elastic scalability
- **Platforms:** AWS, Azure, GCP, private cloud
- **Demo:** [Cloud-Native Demo](https://youtu.be/W58uNYq1-xU?si=tZ9231kaI1O2CNko)

![Cloud Deployment](img/cloud-deployment.png)

### 2. Threat Hunting Platform
**Architecture:** Intelligence-driven hunting with external feeds and analytics
- **Features:** IOC/TTP hunting, behavioral analytics, automated execution
- **Capabilities:** APT detection, zero-day identification, supply chain monitoring
- **Demo:** [Threat Hunting Demo](https://youtu.be/oGU8ufvFnPQ?si=wVdn9oKTDtf2mBLm)

![Threat Hunting](img/threat-hunting.png)

## Quick Comparison

| Scenario | Complexity | Cost | Use Case |
|----------|------------|------|----------|
| Standalone | Low | Low | Small Networks |
| pfSense Integration | Medium | Medium | Perimeter Security |
| Internal Network | Medium | Medium | Internal Monitoring |
| Cloud-Native | High | Variable | Enterprise Scale |
| Threat Hunting | High | High | Advanced Security |

## Implementation Steps

1. **Planning:** Assess requirements → Select scenario → Resource planning
2. **Deployment:** Environment setup → Software installation → Configuration
3. **Operation:** 24/7 monitoring → Incident response → Maintenance

## Quick Setup

1. Download Security Onion ISO and verify checksum
2. Install with dual NICs (management + monitoring)
3. Run setup wizard for sensor deployment
4. Configure Elasticsearch cluster and Kibana
5. Access web interface: `https://[management-ip]`

---

**Project Info:**
- Course: NT204.P21.ANTT - Intrusion Detection and Prevention Systems
- Group: G12-A32
- Institution: University of Information Technology (UIT)