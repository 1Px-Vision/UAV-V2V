# UAV-Aided Information Diffusion for V2V in Disaster Scenarios

UAV-Aided Information Diffusion for V2V in Disaster Scenarios is a research-oriented project that investigates how unmanned aerial vehicles (UAVs) can support information dissemination when conventional vehicle-to-vehicle (V2V) communication is disrupted by disasters, road blockages, or partitioned traffic groups. The framework combines UAV relaying, edge/cloud coordination, and FPGA-accelerated reaction-diffusion modeling to improve message propagation across disconnected vehicle clusters.

![](https://github.com/1Px-Vision/UAV-V2V/blob/main/UAV_V2V.jpg)

## Overview

In disaster scenarios, direct V2V communication may become unreliable due to damaged infrastructure, blocked roads, network fragmentation, or isolated vehicle groups. This project explores a hybrid architecture where UAVs act as mobile communication assistants, collecting, relaying, and redistributing critical information between non-receiving vehicles and disconnected vehicle groups.

The system integrates three main layers:

- **UAV-assisted communication layer** for aerial collection and delivery of messages.
- **Cluster-FPGA computation layer** for accelerated processing and coordination.
- **Reaction-diffusion modeling layer** for simulating and optimizing information spread dynamics.

This approach is intended for emergency communication, intelligent transportation systems, and resilient cyber-physical mobility networks.

## Motivation

During earthquakes, floods, landslides, fires, or large-scale traffic disruptions, terrestrial communication links may fail or become partially unavailable. In these conditions:

- vehicles may be unable to receive important warnings,
- road disruptions can partition traffic into isolated groups,
- V2V communication alone may not guarantee full message coverage,
- low-latency decision support becomes critical.

By introducing UAVs as adaptive communication bridges, the system aims to extend the communication range, reconnect fragmented vehicle groups, and maintain the diffusion of critical information such as evacuation routes, hazard alerts, and coordination instructions.

## System Architecture

The proposed architecture includes:

1. **Vehicles and V2V communication**  
   Vehicles exchange messages locally through V2V links whenever connectivity is available.

2. **UAV relay layer**  
   UAVs gather information from connected vehicles, move across disrupted areas, and forward messages to isolated vehicles or non-receiving groups.

3. **VPN / network backbone**  
   A secure communication backbone supports exchange between UAV services and remote processing nodes.

4. **Cluster-FPGA platform**  
   A cluster-based FPGA system accelerates the computational tasks related to diffusion modeling, routing support, or real-time decision updates.

5. **Reaction-diffusion model**  
   Information dissemination is modeled as a diffusion process to estimate how messages propagate spatially and temporally under network fragmentation.

## Key Features

- UAV-assisted message delivery in disrupted road scenarios
- Support for disconnected and non-receiving vehicle groups
- V2V information exchange modeling
- FPGA-oriented acceleration for scalable processing
- Reaction-diffusion based information propagation analysis
- Disaster scenario simulation for resilient ITS research
- Modular design for communication, mobility, and computation experiments

## Example Scenario

A typical scenario considered in this project is the following:

- a disaster causes a **road disruption**,
- direct communication between two vehicle groups becomes impossible,
- one UAV collects data from a connected vehicle cluster,
- the UAV moves toward the disconnected region,
- the message is forwarded to non-receiving vehicles,
- a remote Cluster-FPGA platform evaluates diffusion behavior and supports optimized dissemination.

## Repository Structure

A suggested repository structure is shown below:

```bash
UAV-Aided-Information-Diffusion-for-V2V-in-Disaster-Scenarios/
│
├── README.md
├── requirements.txt
├── src/
│   ├── communication/
│   ├── uav/
│   ├── v2v/
│   ├── diffusion_model/
│   ├── fpga_interface/
│   └── simulation/
│
├── configs/
│   ├── disaster_scenarios/
│   ├── network_params/
│   └── uav_profiles/
│
├── data/
│   ├── maps/
│   ├── traffic/
│   └── results/
│
├── docs/
│   ├── architecture.png
│   └── figures/
│
└── examples/
    ├── run_simulation.py
    └── demo_scenario.ipynb
