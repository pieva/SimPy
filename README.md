# Switch Cascade Simulation

This Python program simulates the behavior of a cascade of switches, where packets flow through a series of switches in a network. The simulation uses the SimPy library to model the discrete-event simulation of packet transmission and processing.

## Overview

The simulation consists of the following components:

1. **Packet Generator**: This component generates packets with specified inter-arrival time and size distributions. It simulates the arrival of packets into the network.

2. **Switch Ports**: There are three switch ports in this simulation, each representing a switch in the cascade. Switch ports receive and process incoming packets. They have a specified bit rate and buffer size limit.

3. **Packet Sink**: The packet sink component collects incoming packets, records arrival times, and calculates packet delays.

4. **Random Brancher**: This element randomly chooses an output port to simulate parallel switches in the cascade.

## Classes Definition

The simulation is implemented using several Python classes, each representing a different component of the network:

- `Packet`: Represents a packet with attributes such as arrival time, size, and identifier.

- `PacketGenerator`: Generates packets with inter-arrival time and size distributions.

- `SwitchPort`: Represents a switch port with a specified bit rate and buffer size limit.

- `PacketSink`: Collects packets, records arrival times, and calculates delays.

- `RandomBrancher`: Chooses an output port randomly for parallel switching.

## Main Simulation

In the main part of the code, the SimPy environment is created, and the network nodes are defined. The packet generator, switch ports, packet sinks, and random brancher are connected to model the cascade. Port monitors are used to track queue sizes over time.

The simulation is run for a specified duration (in this case, 5000 time units).

## Print Statistics

After running the simulation, delay statistics and queue size statistics are calculated and printed. These statistics include average packet delay, maximum delay, minimum delay, and average queue sizes for each switch in the simulation.

## Display Packet Tables

The program also displays packet tables for each switch, showing packet details such as packet ID, size, queue size, arrival time, waiting time, and departure time.

## Dependencies

- SimPy: The simulation is built using the SimPy library for discrete-event simulation. You can install it using pip:

   ```bash
   pip install simpy
   
