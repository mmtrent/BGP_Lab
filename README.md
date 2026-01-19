# BGP Practice Lab: Cisco + Containerlab

A hands-on BGP laboratory environment built using **Containerlab** and **Cisco** virtual images. This repository contains the topology definition and initial configurations for practicing BGP peering, path selection, and attribute manipulation.

## 🚀 Overview
The goal of this project is to simulate a multi-AS environment to master Border Gateway Protocol concepts in a lightweight, containerized environment.

* **Platform:** [Containerlab](https://containerlab.dev/)
* **Nodes:** Cisco IOL 17.15.01
* **Routing Protocols:** BGP (iBGP/eBGP), OSPF/IS-IS (as IGP)

## 🏗️ Topology
The laboratory simulates the following environment:
* **AS 65001:** Core Network utilizing iBGP and Route Reflectors.
* **AS 65002 / 65003:** External Autonomous Systems for eBGP testing and path manipulation.
* **Management:** Out-of-band management network for SSH access to all nodes.

## 🛠️ Getting Started

### Prerequisites
1.  **Docker** installed and running.
2.  **Containerlab** installed.
3.  Cisco node images pre-loaded into your local Docker registry.

### Deployment
To spin up the lab environment:
```bash
sudo containerlab deploy -t bgp_1.clab.yaml