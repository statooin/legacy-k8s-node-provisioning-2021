# Legacy K8s Node Provisioning (2021 Archive)

[⚠️STATUS: ARCHIVAL / HISTORICAL REFERENCE]

## Overview
This repository contains a collection of baseline shell automation scripts used in 2021 for rapid provisioning of local Kubernetes development environments. It serves as a historical record of early node initialization workflows before the full transition to modern Infrastructure-as-Code (IaC) and Immutable Infrastructure standards.

As a **Senior SRE with 10+ years of experience**, I maintain this repository to demonstrate the evolution of infrastructure automation-from imperative shell scripting to declarative, policy-driven orchestration used in 2026.

## Repository Structure
The project consists of specialized scripts for Debian-based distributions:

* `docker_install.sh`: Automates the installation of the Docker engine, container runtime, and related security keyrings. It includes user-group permission management for non-root execution.
* `minikube_kubectl_install.sh`: Handles the lifecycle setup of local cluster orchestration tools (`minikube`) and the Kubernetes command-line interface (`kubectl`).

## Modern Context (2026 Perspective)
While these scripts were highly effective for rapid prototyping and local sandbox environments in 2021, my current architectural standards for production-grade environments have evolved significantly:

1.  **IaC Maturity:** I have transitioned from Shell to **Terraform** and **Ansible** for consistent, idempotent state management.
2.  **Security Baseline:** In modern workflows, I implement **eBPF-based monitoring (Cilium)** and **Zero Trust networking** right at the node provisioning stage.
3.  **Image Factory:** Instead of on-the-fly installation scripts, I prioritize **Packer** to create specialized, hardened AMIs/Images, reducing boot time and attack surfaces.

---
*This repository is part of my public laboratory where I archive fundamental concepts that paved the way for advanced SRE and Security practices.*
