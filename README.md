# Proxmox Virtual Environment for Small-Scale Business Infrastructure

## 📌 Project Overview

This project explores the utilization of **Proxmox Virtual Environment (PVE)** to design, deploy, and optimize IT infrastructure for small-scale businesses. The goal is to provide a cost-effective, secure, and scalable virtualization platform that supports modern networking and cybersecurity practices.

The project combines practical deployment on a **Proxmox VE cluster** with applied research on optimizing resources, security, and scalability for SMEs.

---

## ⚙️ Infrastructure Setup

### Cluster

* **3-node Proxmox VE cluster**
* SDN (Software-Defined Networking) with **Simple Network Zones**
* Shared bridge: `VNet`
* Zone name: `VirtNet`

### Networking

* Management subnet: `10.10.10.0/24`
* DHCP range: `10.10.10.50 - 10.10.10.100`
* Internode and VM/LXC communication configured across nodes

### Services Deployed

* **DHCP server** (running on a VM within Proxmox)
* **Firewall rules** applied at multiple levels (Datacenter, Node, and VM/LXC)

  * Ensuring internode communication
  * Controlling VM traffic flows
  * Providing layered security

---

## 🔐 Security & Cybersecurity Focus

Given the project’s cybersecurity emphasis, several aspects were implemented/tested:

* Layered firewalling for **data center → node → VM** traffic
* Isolation of virtual networks with Proxmox SDN zones
* Controlled DHCP scope for better IP management
* Research on security hardening strategies for Proxmox in production-like environments

---

## 📚 Research Component

This project contributes to academic research under the topic:
**“Utilization of Proxmox VE for Small-Scale Business Infrastructure Optimization.”**

The research focuses on:

* Cost-effective virtualization for SMEs
* Scalability and resource allocation in Proxmox
* Network security and inter-node communication challenges
