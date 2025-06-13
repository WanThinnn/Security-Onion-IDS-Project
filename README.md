# Security Onion IDS Project

## Overview

This project implements an Intrusion Detection System (IDS) using Security Onion, a Linux distribution designed for intrusion detection, enterprise security monitoring, and log management. Security Onion is built on Ubuntu and provides a comprehensive platform for network security monitoring and threat detection.

## About Security Onion

Security Onion is a free and open-source platform that combines multiple security tools into a unified solution for network monitoring and analysis. It integrates various components including:

- **Suricata/Snort**: Network Intrusion Detection System (NIDS)
- **Zeek (formerly Bro)**: Network Security Monitor
- **OSSEC**: Host-based Intrusion Detection System (HIDS)
- **Elasticsearch**: Search and analytics engine
- **Logstash**: Data processing pipeline
- **Kibana**: Data visualization platform
- **Wazuh**: Security monitoring platform
- **TheHive**: Security Incident Response Platform
- **Cortex**: Observable Analysis Engine

## Project Objectives

- Implement a comprehensive network monitoring solution
- Deploy and configure Security Onion for intrusion detection
- Monitor network traffic for suspicious activities
- Analyze security events and generate alerts
- Create dashboards for security visualization
- Establish incident response procedures

## System Architecture

The Security Onion deployment consists of several key components:

### Network Layer
- Network sensors for traffic monitoring
- Packet capture and analysis
- Real-time threat detection

### Processing Layer
- Log aggregation and processing
- Event correlation and analysis
- Alert generation and management

### Visualization Layer
- Security dashboards
- Event visualization
- Reporting capabilities

## Features

### Network Monitoring
- Real-time network traffic analysis
- Protocol detection and analysis
- Bandwidth monitoring and alerting

### Intrusion Detection
- Signature-based detection
- Anomaly-based detection
- Behavioral analysis
- Custom rule creation

### Log Management
- Centralized log collection
- Log parsing and normalization
- Long-term log retention
- Search and analysis capabilities

### Security Analytics
- Event correlation
- Threat intelligence integration
- Risk assessment
- Compliance reporting

## Installation and Setup

### System Requirements

**Minimum Requirements:**
- RAM: 8GB (16GB recommended)
- CPU: 4 cores (8 cores recommended)
- Storage: 200GB (1TB recommended for production)
- Network: Multiple network interfaces

**Recommended Requirements:**
- RAM: 32GB or more
- CPU: 8+ cores
- Storage: 2TB+ SSD
- Network: Dedicated monitoring interfaces

### Installation Steps

1. **Download Security Onion ISO**
   - Download the latest Security Onion ISO from the official website
   - Verify the checksum

2. **System Installation**
   - Boot from ISO and follow installation wizard
   - Configure network interfaces
   - Set up user accounts and passwords

3. **Initial Configuration**
   - Run the Setup wizard
   - Configure management and monitoring interfaces
   - Set up sensor deployment

4. **Service Configuration**
   - Configure Elasticsearch cluster
   - Set up Kibana dashboards
   - Configure alert rules

## Configuration

### Network Configuration
- Configure management interface for administration
- Set up monitoring interfaces for packet capture
- Configure network segments and VLANs

### Sensor Configuration
- Deploy sensors at strategic network points
- Configure sensor rules and signatures
- Set up distributed sensor architecture

### Alert Configuration
- Configure alert thresholds
- Set up notification systems
- Create custom detection rules

## Usage

### Accessing the Interface
- Web interface: `https://[management-ip]`
- Default credentials: configured during setup
- Multi-factor authentication recommended

### Monitoring Activities
1. **Dashboard Monitoring**
   - Access main security dashboard
   - Monitor real-time alerts
   - Review network statistics

2. **Alert Investigation**
   - Investigate triggered alerts
   - Analyze packet captures
   - Correlate events across sensors

3. **Threat Hunting**
   - Search historical data
   - Create custom queries
   - Export investigation results

## Dashboards and Visualization

### Main Dashboard
- Network overview and statistics
- Recent alerts and events
- System health monitoring

### Alert Dashboard
- Active alerts and incidents
- Alert trending and analysis
- Geographic threat visualization

### Network Dashboard
- Traffic analysis and patterns
- Protocol distribution
- Bandwidth utilization

## Security Rules and Policies

### Default Rules
- Emerging Threats ruleset
- Snort community rules
- Custom organizational rules

### Rule Management
- Regular rule updates
- Custom rule creation
- Rule testing and validation

### Policy Configuration
- Network segmentation policies
- Access control policies
- Incident response procedures

## Maintenance and Updates

### Regular Maintenance
- System updates and patches
- Rule updates
- Performance monitoring
- Backup procedures

### Health Monitoring
- Service status monitoring
- Resource utilization tracking
- Log rotation management
- Database maintenance

## Troubleshooting

### Common Issues
- Network connectivity problems
- Service startup failures
- Performance degradation
- Storage space issues

### Log Analysis
- System logs location: `/var/log/`
- Service-specific logs
- Debug mode activation

## Performance Optimization

### Hardware Optimization
- Memory allocation tuning
- CPU optimization
- Storage performance
- Network interface optimization

### Software Optimization
- Elasticsearch tuning
- Logstash pipeline optimization
- Rule optimization
- Data retention policies

## Security Considerations

### Access Control
- Role-based access control
- Multi-factor authentication
- SSL/TLS encryption
- Network segmentation

### Data Protection
- Encrypted communications
- Secure key management
- Data backup strategies
- Compliance requirements

## Documentation

### Additional Resources
- Official Security Onion documentation
- Community forums and support
- Training materials
- Best practices guides

### Project Documentation
- `/docs/` - Project documentation
- `/slide/` - Presentation materials
- Configuration files and scripts

## Contributing

This project is developed as part of the NT204 - Intrusion Detection and Prevention Systems course. Contributors should follow established security practices and documentation standards.

## License

This project follows the licensing terms of the Security Onion platform and associated tools. Please refer to individual component licenses for specific terms.

## Support and Contact

For technical support and questions:
- Course: NT204.P21.ANTT
- Group: G12-A32
- Institution: University of Information Technology (UIT)

## Acknowledgments

Special thanks to the Security Onion development team and the open-source security community for providing comprehensive tools for network security monitoring and intrusion detection.

## Implementation Scenarios

This project demonstrates multiple deployment scenarios for Security Onion, each tailored to different network environments and security requirements.

### 4.1. Scenario 1: Standalone Mode with Dual NIC (Separate Management & Monitoring)

This scenario implements Security Onion in standalone mode using two network interface cards (NICs) - one dedicated for management traffic and another for monitoring network traffic.

**Architecture Overview:**
- **Management Interface**: Handles administrative access and system management
- **Monitoring Interface**: Captures and analyzes network traffic in promiscuous mode
- **Deployment Model**: Single-node deployment suitable for small to medium environments

**Key Features:**
- Isolated management and monitoring traffic
- Enhanced security through network segregation
- Simplified deployment and maintenance
- Cost-effective solution for smaller networks

**Use Cases:**
- Small business network monitoring
- Educational environments
- Testing and development scenarios
- Branch office security monitoring

**Video Demonstration:** [Standalone Mode with Dual NIC Demo](https://youtu.be/bWiu8lMXAZk?si=wuvnwz9h18eOClaS)

![Standalone Mode Architecture](img/standalone-architecture.png)

### 4.2. Scenario 2: Security Onion Integration with Firewall (pfSense)

This scenario demonstrates the integration of Security Onion with pfSense firewall to create a comprehensive network security solution combining perimeter defense with intrusion detection.

**Architecture Overview:**
- **pfSense Firewall**: Provides perimeter security and traffic filtering
- **Security Onion**: Monitors internal network traffic and detects intrusions
- **Traffic Mirroring**: pfSense mirrors traffic to Security Onion for analysis
- **Unified Management**: Centralized security monitoring and alerting

**Key Features:**
- Integrated firewall and IDS capabilities
- Real-time threat detection and prevention
- Comprehensive network visibility
- Coordinated security response

**Benefits:**
- Enhanced threat detection coverage
- Reduced security gaps
- Centralized security management
- Improved incident response capabilities

**Video Demonstration:** [Security Onion with pfSense Integration Demo](https://youtu.be/HT8qZro5x00?si=-r-8OZ2qNsrbV93Q)

![pfSense Integration Architecture](img/pfsense-integration.png)

### 4.3. Scenario 3: Internal Network Deployment with Security Onion

This scenario focuses on deploying Security Onion within an internal network environment to monitor east-west traffic and detect lateral movement attacks.

**Architecture Overview:**
- **Internal Network Monitoring**: Focuses on intra-network communications
- **Segment-based Deployment**: Monitors critical network segments
- **Lateral Movement Detection**: Identifies suspicious internal activities
- **Insider Threat Monitoring**: Detects malicious insider activities

**Key Features:**
- Internal traffic analysis
- Lateral movement detection
- User behavior analytics
- Asset discovery and monitoring

**Monitoring Capabilities:**
- Inter-VLAN communications
- Server-to-server communications
- Workstation activities
- Privileged account monitoring

**Video Demonstration:** [Internal Network Deployment Demo](https://youtu.be/_C9MXBDSYEU?si=vYywR-h7iumJpBQG)

![Internal Network Architecture](img/internal-network.png)

## Advanced Solutions

### 5.1. Solution 1: Cloud-Native Security Onion Deployment (Cloud-Native SIEM)

This solution demonstrates deploying Security Onion in cloud environments, leveraging cloud-native technologies for scalable and resilient security monitoring.

**Cloud Architecture:**
- **Container-based Deployment**: Using Docker and Kubernetes
- **Auto-scaling Capabilities**: Dynamic resource allocation based on load
- **Multi-region Deployment**: Distributed monitoring across geographic regions
- **Cloud Storage Integration**: Leveraging cloud storage for log retention

**Key Features:**
- **Elastic Scalability**: Automatic scaling based on traffic volume
- **High Availability**: Multi-zone deployment for fault tolerance
- **Cost Optimization**: Pay-per-use model with resource optimization
- **Global Monitoring**: Worldwide threat detection capabilities

**Cloud Platforms Supported:**
- Amazon Web Services (AWS)
- Microsoft Azure
- Google Cloud Platform (GCP)
- Private cloud environments

**Benefits:**
- Reduced infrastructure costs
- Improved scalability and flexibility
- Enhanced disaster recovery capabilities
- Global threat intelligence sharing

**Video Demonstration:** [Cloud-Native Security Onion Demo](https://youtu.be/W58uNYq1-xU?si=tZ9231kaI1O2CNko)

![Cloud Deployment Architecture](img/cloud-deployment.png)

### 5.2. Solution 2: Threat Hunting with Security Onion & Threat Intelligence

This solution focuses on proactive threat hunting capabilities using Security Onion integrated with external threat intelligence feeds and advanced analytics.

**Threat Hunting Framework:**
- **Intelligence-Driven Hunting**: Using IOCs and TTPs from threat intelligence
- **Behavioral Analytics**: Identifying anomalous patterns and behaviors
- **Hypothesis-Based Hunting**: Structured approach to threat discovery
- **Automated Hunt Execution**: Scheduled and triggered hunt operations

**Key Components:**
- **Threat Intelligence Integration**: MISP, STIX/TAXII, commercial feeds
- **Advanced Analytics**: Machine learning and statistical analysis
- **Hunt Platforms**: Jupyter notebooks and custom hunt tools
- **Collaboration Tools**: Hunt documentation and knowledge sharing

**Hunting Capabilities:**
- **APT Detection**: Advanced persistent threat identification
- **Zero-day Exploitation**: Novel attack pattern detection
- **Supply Chain Attacks**: Third-party compromise detection
- **Living-off-the-Land**: Legitimate tool abuse detection

**Intelligence Sources:**
- Commercial threat intelligence feeds
- Open source intelligence (OSINT)
- Industry sharing platforms
- Government threat advisories

**Hunting Methodologies:**
- Structured threat hunting process
- Hypothesis generation and testing
- Evidence collection and analysis
- Hunt result documentation

**Video Demonstration:** [Threat Hunting with Security Onion Demo](https://youtu.be/oGU8ufvFnPQ?si=wVdn9oKTDtf2mBLm)

![Threat Hunting Workflow](img/threat-hunting.png)

## Scenario Comparison

| Aspect | Standalone Mode | pfSense Integration | Internal Network | Cloud-Native | Threat Hunting |
|--------|----------------|-------------------|------------------|--------------|----------------|
| **Complexity** | Low | Medium | Medium | High | High |
| **Cost** | Low | Medium | Medium | Variable | High |
| **Scalability** | Limited | Medium | Medium | High | High |
| **Use Case** | Small Networks | Perimeter Security | Internal Monitoring | Enterprise | Advanced Security |
| **Maintenance** | Easy | Medium | Medium | Automated | Complex |

## Implementation Guidelines

### Planning Phase
1. **Requirements Analysis**: Assess network size, traffic volume, and security requirements
2. **Architecture Design**: Select appropriate scenario based on organizational needs
3. **Resource Planning**: Determine hardware, software, and personnel requirements
4. **Timeline Development**: Create implementation schedule with milestones

### Deployment Phase
1. **Environment Preparation**: Set up infrastructure and network configurations
2. **Software Installation**: Deploy Security Onion according to selected scenario
3. **Configuration Management**: Apply security policies and monitoring rules
4. **Testing and Validation**: Verify functionality and performance

### Operational Phase
1. **Monitoring and Alerting**: Implement 24/7 security monitoring
2. **Incident Response**: Establish procedures for security event handling
3. **Maintenance and Updates**: Regular system maintenance and updates
4. **Continuous Improvement**: Ongoing optimization and enhancement