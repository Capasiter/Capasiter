# Lee Austin

### Linux & Cloud Support | Infrastructure Operations | Junior DevOps

I’m an infrastructure-focused IT professional in Blaine, Minnesota, building practical experience across Linux systems, AWS fundamentals, infrastructure automation, Kubernetes, observability, and hardware troubleshooting.

I build repeatable systems, troubleshoot them methodically, document technical decisions, and validate results against live homelab infrastructure.

## Featured Project

### [Homelab Infrastructure Portfolio](https://github.com/Capasiter/homelab-portfolio)

[![Infrastructure Validation](https://github.com/Capasiter/homelab-portfolio/actions/workflows/infrastructure-validation.yml/badge.svg)](https://github.com/Capasiter/homelab-portfolio/actions/workflows/infrastructure-validation.yml)

A versioned infrastructure project built with Proxmox VE, Linux, OpenTofu, Ansible, Kubernetes, and GitHub Actions.

- Provisioned Ubuntu workloads with reusable OpenTofu modules.
- Built an idempotent Ansible Linux baseline with SSH hardening.
- Automated and validated a three-server K3s control plane with embedded etcd.
- Validated a protected Kubernetes rolling update with **148 successful HTTP requests and zero observed failures**.
- Deployed Prometheus, Grafana, Alertmanager, and Blackbox Exporter.
- Captured controlled application-alert firing and recovery evidence.
- Published the completed [v0.6.0 observability release](https://github.com/Capasiter/homelab-portfolio/releases/tag/v0.6.0).
- Confirmed the release through a [successful CI validation run](https://github.com/Capasiter/homelab-portfolio/actions/runs/32668970647).

> **Lab scope:** The three K3s VMs share one Proxmox host. The project documents its lack of an external Kubernetes API load balancer, local-only etcd snapshots, pending restore exercise, and node-local monitoring storage.

## Technical Focus

- **Linux and systems:** Ubuntu, SSH, systemd, networking, service and hardware troubleshooting
- **Cloud:** AWS fundamentals and CLF-C02 certification preparation
- **Automation:** OpenTofu, Ansible, Proxmox VE
- **Containers:** K3s, Kubernetes, containerd, Traefik, Helm
- **Observability:** Prometheus, Grafana, Alertmanager, Blackbox Exporter, PromQL
- **Workflow:** Git, GitHub Actions, CI validation, release management, technical documentation
- **AI operations:** Planning a human-supervised lab experiment using AI agents for log analysis, incident triage, and runbook assistance; infrastructure changes will remain human-reviewed and auditable

## Connect

- [LinkedIn](https://www.linkedin.com/in/leeaustinmn/)
- [Email](mailto:lee.austin.lab@gmail.com)
