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

- Vehicles may be unable to receive important warnings,
- Road disruptions can partition traffic into isolated groups,
- V2V communication alone may not guarantee full message coverage,
- Low-latency decision support becomes critical.

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
Edge-AI diffusion-status predictor executed onboard the UAV (and optionally roadside nodes) using a heterogeneous CPU/FPGA pipeline. The core idea is to model the spatio-temporal spread of safety messages (hazards, evacuation routes, blocked roads) as a reaction–diffusion process over the road network and urban space, then learn a fast surrogate that runs in real time from sparse V2V/UAV observations:

![](https://github.com/1Px-Vision/UAV-V2V/blob/main/Reaction_model.jpg)

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

- Disaster causes a **road disruption**,
- Direct communication between two vehicle groups becomes impossible,
- One UAV collects data from a connected vehicle cluster,
- The UAV moves toward the disconnected region,
- The message is forwarded to non-receiving vehicles,
- Remote Cluster-FPGA platform evaluates diffusion behavior and supports optimized dissemination.

## Simulation Agent-driver V2V

![](https://github.com/1Px-Vision/UAV-V2V/blob/main/V2V_weather.jpg)


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
```

## Inputs

Typical inputs for the framework may include:

* Network or map data.
* Vehicle positions and mobility traces.
* UAV initial positions and trajectories.
* Communication range parameters.
* Disruption or blockage locations.
* Message generation events.
* FPGA deployment or acceleration parameters.

## Outputs

Typical outputs may include:

* Information coverage over time.
* Delivery ratio to disconnected vehicles.
* End-to-end dissemination latency.
* UAV trajectory logs.
* Diffusion heatmaps.
* Communication recovery metrics.
* FPGA processing performance statistics.


## Applications

This project is relevant for:

* Disaster response and emergency coordination.
* Intelligent transportation systems.
* Resilient V2X communication.
* UAV-enabled smart mobility.
* Edge/FPGA acceleration for real-time networked systems.
* cyber-physical systems research.
* Research Contributions

### Possible contributions of this project include:

* UAV-assisted strategy for restoring information flow in fragmented V2V environments.
* Reaction-diffusion formulation for message propagation in disaster conditions.
* FPGA-oriented architecture for accelerating communication-aware computation.
* Simulation framework for evaluating communication resilience under road disruptions.
