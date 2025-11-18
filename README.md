## Detection Rules

| Rule Name | Platform | MITRE ATT&CK | Severity |
|-----------|----------|--------------|----------|
| Credential Dumping via Registry | Windows | T1003.002 | High |
| Remote System Discovery | Windows | T1018 | Medium |
| Root SSH to AKS Nodes | Linux/Cloud | T1078.004 | High |

## Lab Components

**On-Premises Environment**
- Two Windows VMs on VMware
- Elastic agents deployed on both endpoints
- MISP threat intelligence integration
- Slack alerting configured

**Cloud Environment**
- Azure Kubernetes Service cluster
- Linux VM on Azure
- Elastic agents on all nodes

**Automation**
- GitHub Actions pipeline for rule deployment
- Automated Sigma to Elastic rule conversion

## Attack Simulation

Used Atomic Red Team to test detection coverage for:
- Credential dumping via registry access
- Network reconnaissance 
- Container escape attempts
- Unauthorized node access

## Technologies

- Elastic Stack (Elasticsearch, Kibana)
- Azure (AKS, Virtual Machines)
- VMware Workstation
- MISP
- Slack
- Atomic Red Team
- GitHub Actions

## License

MIT
