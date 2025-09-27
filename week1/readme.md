```
mkdir VLSI
```
```
cd VLSI
```
```
git clone https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git
```
<img width="1024" height="418" alt="Gitclone skyrtl" src="https://github.com/user-attachments/assets/0d9a7fb4-8ff7-45db-b167-33b805390e8b" />

```
iverilog good_mux.v tb_good_mux.v
```
Running the a.out file created
```
./a.out
```
<img width="792" height="72" alt="Running the a out file" src="https://github.com/user-attachments/assets/01b01d47-eb00-4d38-9323-d2d318f88f64" />

```
gtkwave tb_good_mux.vcd
```
The test bench instantiates the DUT to connect with it
Got a GTK Wave
<img width="1853" height="573" alt="GTKWave tb_good_mux" src="https://github.com/user-attachments/assets/a74b0422-473b-47ea-944c-fefeaaad1b86" />

# Synthesis
Inside the VLSI directory, go to verilog_files directory using following command
```
cd verilog_files
```
```
yosys
```
```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog good_mux.v
synth -top good_mux
```
<img width="1865" height="1080" alt="Screenshot from 2025-09-27 17-15-04" src="https://github.com/user-attachments/assets/b84ec61d-c3b4-4599-8941-c33f42dea2e0" />
<img width="635" height="406" alt="Screenshot from 2025-09-27 17-17-55" src="https://github.com/user-attachments/assets/02f359e7-7986-4277-b8f4-ca80e98ac4bc" />

```
abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
```
<img width="845" height="273" alt="Screenshot from 2025-09-27 17-19-51" src="https://github.com/user-attachments/assets/8ba635f0-9c63-4b54-b95f-74872cbad1f8" />

Got a distutils error
<img width="1865" height="449" alt="Distutils Error" src="https://github.com/user-attachments/assets/b91707f2-ba39-49d3-ab4c-2507e1c4247a" />

To rectify the error
```
sudo apt-get update
sudo apt-get install python3-setuptools
```
To verify if graphiz, xdot and distutils installed or not
```
sudo apt install graphviz xdot
python3 -c "import distutils; print(distutils.__file__)"
```
Now to show the gate level circuit
```
show
```
<img width="1856" height="1007" alt="Screenshot from 2025-09-27 17-20-41" src="https://github.com/user-attachments/assets/348a3cc6-ebd4-456b-90bb-c9192db0be9b" />

Getting the netlist
```
write_verilog -noattr good_mux_netlist.v
!gvim good_mux_netlist.v
```
<img width="1251" height="604" alt="Netlist File" src="https://github.com/user-attachments/assets/199b7e4e-7ffb-4f9f-976c-ed3700c4d662" />

```
yosys
```

```
read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
read_verilog multiple_modules.v
synth -top multiple_modules
```

```
show multiple_modules
```
```
write_verilog -noattr multiple_modules_hier.v
!gvim multiple_modules_hier.v
```


