# RISC-V Reference SoC Tapeout Program VSD

## Tools Installation

### ⚙️ System Requirements
| Resource | Requirement |
|----------|-------------|
| RAM      | 6 GB |
| Storage  | 50 GB HDD |
| OS       | Ubuntu 24.04.3 |
| CPU      | 4 vCPU |

#### <ins>**Yosys**</ins>
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



