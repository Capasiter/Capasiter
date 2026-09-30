# Lee Austin

### Linux · Infrastructure Operations · Cloud Support · Junior DevOps

**Build it. Operate it. Test what happens when it breaks.**

I'm an infrastructure-focused IT professional in Blaine, Minnesota, transitioning from manufacturing, field service, and paid computer repair into Linux systems and cloud operations. I build working infrastructure, investigate failures, and document what the evidence proves.

[![Portfolio](https://img.shields.io/badge/Explore-Homelab_Portfolio-2563EB?style=for-the-badge)](https://github.com/Capasiter/homelab-portfolio)
[![LinkedIn](https://img.shields.io/badge/Connect-LinkedIn-0A66C2?style=for-the-badge)](https://www.linkedin.com/in/leeaustinmn/)

## Featured project · Homelab Infrastructure Portfolio

An isolated Kubernetes lab built with **Proxmox, OpenTofu, Ansible, K3s, and GitHub Actions**—with live monitoring, protected application rollouts, off-server backups, and a validated internal API VIP.

[![Infrastructure Validation](https://github.com/Capasiter/homelab-portfolio/actions/workflows/infrastructure-validation.yml/badge.svg)](https://github.com/Capasiter/homelab-portfolio/actions/workflows/infrastructure-validation.yml)

| Build | Operate | Validate |
|:---|:---|:---|
| **3 K3s server VMs**<br>Control plane + embedded etcd | **Prometheus + Grafana**<br>Cluster metrics and application probing | **148 successful HTTP requests**<br>0 observed failures during a protected rollout |
| **Repeatable infrastructure**<br>OpenTofu provisioning + Ansible configuration | **Off-server backups**<br>Checksum verification, protected token, daily scheduling | **API VIP handoff**<br>Ownership moved from server 02 to server 03 |

### Latest released milestone · v0.8 API VIP

On September 19, 2026, I tested a controlled kube-vip leader-pod deletion while probing the Kubernetes API through its stable internal endpoint. VIP ownership moved to another server, the deleted pod was replaced, and all three nodes were Ready afterward. **No failed API probes were recorded**; a zero-downtime bound was not measured.

**[Explore the architecture](https://github.com/Capasiter/homelab-portfolio#architecture)** · **[Read the failover evidence](https://github.com/Capasiter/homelab-portfolio/blob/main/ansible/docs/k3s-api-vip-validation.md)** · **[Browse releases](https://github.com/Capasiter/homelab-portfolio/releases)**

### Current lab work · Argo CD GitOps

On September 27, 2026, I installed Argo CD in the lab and registered WebDemo for manual synchronization. A controlled change from three to four replicas appeared as OutOfSync; after reviewing the diff, I manually reconciled the Deployment and confirmed Synced, Healthy, and 3/3 Ready replicas. This work is merged into `main`; **v0.9.0 has not been released**. [Read the configuration and validation record](https://github.com/Capasiter/homelab-portfolio/blob/main/kubernetes/argocd/README.md).

### Engineering work behind the results

- **Application reliability:** investigated a client-visible timeout during an otherwise successful rollout, added readiness and graceful-drain protections, and retested under HTTP traffic. [Read the lab](https://github.com/Capasiter/homelab-portfolio/blob/main/kubernetes/k8s-learning/README.md).
- **Monitoring:** validated Prometheus targets, Grafana dashboards, and the application alert lifecycle from healthy to firing to recovered. [See the evidence](https://github.com/Capasiter/homelab-portfolio/blob/main/kubernetes/observability/README.md).
- **Backup and recovery:** resolved NFS ownership and checksum-write issues; verified off-server snapshots and token protection. An isolated restore attempt reached snapshot decompression but encountered a K3s reset-path panic. [Read the findings](https://github.com/Capasiter/homelab-portfolio/blob/main/docs/portfolio-history-through-v0.7.md#restore-validation).

> **Lab scope:** The three K3s VMs share one physical Proxmox host. The failover exercise tested pod-level handoff, not physical-host resilience. Full etcd restore remains incomplete, and application volumes remain node-local. The CI badge reports repository checks, not live cluster health.

## Tools I use

| Area | Technologies |
|---|---|
| Linux and systems | Ubuntu, SSH, systemd, networking, service and hardware troubleshooting |
| Infrastructure automation | Proxmox VE, OpenTofu, Ansible, cloud-init, OPNsense |
| Kubernetes | K3s, embedded etcd, kube-vip, containerd, Traefik, Helm |
| Observability | Prometheus, Grafana, Alertmanager, Blackbox Exporter, PromQL |
| Engineering workflow | Git, GitHub Actions, Argo CD manual sync, validation records, versioned releases |

## Building toward

**Next:** Strengthen the Argo CD validation record for v0.9.0; shared application storage and volume-recovery validation.

**Future:** human-supervised AI operations for log analysis, incident triage, and runbook assistance—starting in an isolated sandbox with reviewed, auditable changes.

**Learning:** AWS fundamentals and preparation for AWS Certified Cloud Practitioner (CLF-C02).

The Next and Future items are planned work; AWS certification is a learning goal, not a held credential.

## Connect

I'm interested in Linux support, infrastructure operations, cloud support, and junior DevOps opportunities.

[LinkedIn](https://www.linkedin.com/in/leeaustinmn/) · [Email](mailto:lee.austin.lab@gmail.com) · [Explore the portfolio](https://github.com/Capasiter/homelab-portfolio)
