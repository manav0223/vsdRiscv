# RISC-V Reference SoC Tapeout Program VSD

<div align="center">

[![RISC-V](https://img.shields.io/badge/RISC--V-SoC%20Tapeout-blue?style=for-the-badge&logo=riscv)](https://riscv.org/)
[![VSD](https://img.shields.io/badge/VSD-Program-orange?style=for-the-badge)](https://vsdiat.vlsisystemdesign.com/)
![Participants](https://img.shields.io/badge/Participants-3500+-success?style=for-the-badge)
![India](https://img.shields.io/badge/Made%20in-India-saffron?style=for-the-badge)

</div>

# Program Overview
The RISC-V Reference SoC Tapeout Program, conducted by VSD (VLSI System Design), provides hands-on experience in designing, simulating, and synthesizing a RISC-V based System-on-Chip. Participants learn the complete open-source ASIC flow starting from RTL design to GDSII tapeout.

# Focus Areas:
1. Understanding the RISC-V ISA architecture
2. RTL design & functional verification
3. Logic synthesis using Yosys
4. RTL-to-GDSII flow with open-source tools
5. Post-synthesis verification with GTKWave

# Why it matters: 
This program brings together 3500+ participants from across the world, democratizing chip design,and enabling students and engineers to be part of the Made-in-India silicon ecosystem.


## Tools Installation

### ⚙️ System Requirements
| Resource | Requirement |
|----------|-------------|
| RAM      | 6 GB |
| Storage  | 50 GB HDD |
| OS       | Ubuntu 24.04.3 |
| CPU      | 4 vCPU |
Each tool below is required for a different stage of the RTL-to-GDS flow, making the setup essential.

#### <ins>**Yosys**</ins>
Yosys is used to convert Verilog RTL into a gate-level netlist. It is a key step in preparing the design for backend layout and timing verification.
```
$ sudo apt-get update
$ sudo apt install git                 
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ git submodule update --init --recursive
$ sudo apt install make               # If make is not installed
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make
```
<img width="514" height="673" alt="make install successful" src="https://github.com/user-attachments/assets/755940f6-056f-4a69-a508-6b5cbe379ab1" />
```
$ sudo make install
```
<img width="902" height="229" alt="yosys install" src="https://github.com/user-attachments/assets/7f55a86c-506b-4c14-ae99-6d4b7d6dce04" />

```
$ yosys
```
<img width="830" height="185" alt="Yosys" src="https://github.com/user-attachments/assets/0b3c22a4-664e-438e-aa88-78a03789dd28" />

#### <ins>**Iverilog**</ins>
Icarus Verilog is used for Verilog simulation and functional testing. With it, you can verify the correctness of your RTL before synthesis.
```
$ sudo apt-get update
$ sudo apt-get install iverilog
```
<img width="1022" height="421" alt="IVerilog Installation" src="https://github.com/user-attachments/assets/c5cf5cbb-dfb1-49a9-abe7-a146a080efbb" />
<img width="1022" height="671" alt="iVerilog Installed" src="https://github.com/user-attachments/assets/f625d767-04aa-4921-9aed-abf3749ee650" />

#### <ins>**GTKWave**</ins>
```
$ sudo apt-get update
$ sudo apt install gtkwave
```
<img width="1005" height="767" alt="gtkwave" src="https://github.com/user-attachments/assets/0d809fcf-1f91-40af-af16-d8337017a17d" />
<img width="1087" height="845" alt="gtkwave_2" src="https://github.com/user-attachments/assets/533bea38-039d-4672-b164-5a043cc6b04d" />



