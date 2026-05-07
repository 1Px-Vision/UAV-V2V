# V2V Agent-Driver Traffic Simulation

This project implements a **V2V-enabled agent-driver simulation** for intelligent traffic supervision and collision avoidance. The application models a leader vehicle driving on a multi-lane road under different traffic, congestion, crash, and weather conditions. The leader car uses information from nearby vehicles, UAV/drone supervision, and a DQN-based agent to improve driving decisions.

![](https://github.com/1Px-Vision/UAV-V2V/blob/main/V2V_weather.jpg)

## Main Features

- Multi-lane road traffic simulation
- Statistical vehicle generation
- V2V information exchange between connected vehicles
- UAV/drone-assisted traffic supervision
- Weather-aware driving conditions: clear, rain, fog, and storm
- Traffic congestion and crash-event modeling
- Leader-car decision making using a Deep Q-Network agent
- Safety shield for lane changes and speed control
- GIF export for visual analysis

## Application Goal

The objective of this simulator is to evaluate how **V2V communication and an intelligent agent-driver** can improve road safety and traffic efficiency. The leader car receives information about vehicle density, lane risk, crashes, and congestion. Based on this information, the DQN agent selects actions such as maintaining speed, slowing down, accelerating, or changing lanes.

## Agent-Driver Actions

![](https://github.com/1Px-Vision/UAV-V2V/blob/main/Weather_V2V_Traffic_2_V1.mp4)

The DQN agent controls the leader vehicle using five high-level actions:

```text
KEEP
SLOW
FAST
LANE_LEFT
LANE_RIGHT

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
