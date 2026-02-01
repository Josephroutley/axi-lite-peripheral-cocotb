# AXI4-Lite Peripheral Controller

## Project Overview
This project implements a memory-mapped peripheral compliant with the **AMBA AXI4-Lite** protocol. It serves as a foundational exercise in understanding industry-standard bus protocols used in modern SoCs (System on Chips).

The verification environment is built using **Python (Cocotb)** to simulate a "Master" agent driving traffic to the peripheral.

## Learning Objectives
* **Bus Protocols:** Deep understanding of the AXI Valid/Ready handshake mechanism.
* **Python Scripting:** Using Python for verification (Cocotb) to drive stimulus and check responses.
* **FSM Design:** Handling complex state transitions for Read/Write channels.

## Architecture
* **AXI Slave Interface:** Handles the 5 AXI channels (Write Address, Write Data, Write Response, Read Address, Read Data).
* **Register Map:** Internal configuration registers readable/writable by the bus.
* **Control Logic:** FSM to manage simultaneous read/write requests (or enforce ordering).

## Tools & Tech Stack
* **Language:** Verilog
* **Verification:** Python, Cocotb
* **Simulation:** Verilator / Icarus Verilog

## Roadmap
- [ ] Design AXI-Lite Slave FSM.
- [ ] Implement register file storage.
- [ ] **Verification:** Set up Cocotb testbench.
- [ ] **Verification:** Write Python tests for randomized read/write sequences.
- [ ] **Verification:** Verify protocol compliance (no dropped transactions).
