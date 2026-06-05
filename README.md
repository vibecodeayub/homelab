# Personal Homelab Infrastructure Project

## Overview

This project documents the design, deployment, and management of my personal homelab running on an HP Z440 workstation. The goal of the project was to gain hands-on experience with virtualization, Linux administration, networking, self-hosting, and infrastructure management while providing practical services for real-world use.

The homelab currently hosts a self-managed photo backup platform used by family members, secure remote access services, containerized applications, and a virtualized infrastructure environment.

---

## Hardware

### Host System

* HP Z440 Workstation
* Intel Xeon Processor
* 1TB Hard Disk Drive
* 500GB Samsung SSD
* Gigabit Ethernet Connectivity

---

## Software Stack

### Virtualization

* Proxmox VE

### Operating Systems

* Debian Linux Virtual Machine

### Containerization

* Docker
* Docker Compose
* Portainer

### Networking

* Tailscale VPN
* Secure Remote SSH Access

### Self-Hosted Applications

* Immich (Photo Management and Backup Platform)

---

## Architecture

Internet
│
Tailscale VPN
│
HP Z440 Workstation
│
Proxmox VE
│
Debian Virtual Machine
│
Docker Engine
├── Immich
└── Portainer

---

## Features Implemented

### Virtual Machine Management

* Deployed and configured a Debian Linux virtual machine within Proxmox.
* Allocated storage, memory, and networking resources.
* Created snapshots for rollback and recovery.

### Secure Remote Access

* Configured Tailscale on both the Proxmox host and Debian VM.
* Enabled secure remote access from external networks without exposing services directly to the internet.
* Successfully managed the entire infrastructure remotely from outside the home network.

### Docker Infrastructure

* Installed and configured Docker.
* Managed containers through Portainer.
* Deployed services using Docker Compose.

### Immich Deployment

* Self-hosted photo and video backup platform.
* Created user accounts for family members.
* Enabled secure remote access through Tailscale.
* Provided an alternative to commercial cloud photo storage.

### System Administration

* Linux command-line management.
* Package installation and maintenance.
* Service troubleshooting.
* Network diagnostics and configuration.

---

## Challenges and Troubleshooting

Throughout the project, several issues were encountered and resolved:

### Networking Issues

* Diagnosed missing IPv4 configuration on Debian.
* Restored DHCP functionality.
* Re-established default routing and internet connectivity.

### Docker Deployment Issues

* Resolved image download failures.
* Diagnosed connectivity and repository problems.
* Successfully deployed production containers.

### Proxmox Repository Issues

* Removed enterprise repositories that required a subscription.
* Configured package sources correctly.
* Restored update functionality.

### VPN Routing Conflicts

* Diagnosed internet connectivity problems caused by conflicting VPN software.
* Identified Proton VPN as the source of routing issues.
* Restored normal internet access while maintaining Tailscale connectivity.

### Remote Infrastructure Management

* Verified remote access to Proxmox, Debian, Docker services, and Immich from external networks.
* Successfully managed the homelab from a public library using Tailscale.

---

## Skills Demonstrated

* Linux Administration
* Virtualization
* Proxmox VE
* Docker
* Docker Compose
* Container Management
* SSH
* VPN Technologies
* Network Troubleshooting
* Remote Infrastructure Management
* Self-Hosting
* System Documentation
* Problem Solving
* Technical Troubleshooting

---

## Future Improvements

* Implement automated backups using Restic or BorgBackup.
* Configure dedicated backup storage on additional SSDs.
* Deploy Scrutiny for drive health monitoring.
* Migrate high-performance workloads to SSD storage.
* Deploy additional self-hosted services.
* Implement monitoring and alerting dashboards.
* Improve backup redundancy and disaster recovery planning.

---

## Project Outcome

This project provided practical experience with technologies commonly used in cloud computing, infrastructure engineering, DevOps, and cybersecurity environments. It also delivered a real-world solution for family photo backup and remote access while building foundational skills in systems administration and networking.

The homelab continues to serve as a platform for experimentation, learning, and infrastructure development.
