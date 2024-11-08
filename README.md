# D FLIP FLOP USING CMOSD FLIP FLOP USING CMOS 130nm Technology
This project simulates the designed D Flip Flop using CMOS circuit to determine its performance characteristics pre layout and post layout
# A Glance at the D Flip Flop IP
CMOS D flip flops are first preference to implement different type of binary counters, shift registers and analog and digital circuit system.The TSPC logic which allows to represent the design of D flip flop with smaller area and lower power consumption as compared to master-slave configuration based D flip flop.Delay flip flops stores whatever input pattern in its D input. So it is helpful to process the data bit by bit to get solutions for complex functions. It is known as Data flip flop since it can store data.
# Block Diagram of the D Flip Flop IP
![image](https://github.com/user-attachments/assets/752271a2-3afd-43b0-987e-4447b96ce367)
# Circuit Diagram of the D Flip Flop 
![image](https://github.com/user-attachments/assets/2e5de739-f3b7-41db-ae60-453ad03eeb97)
# Performance parameters
| Parameter | Description | Min| Type | Max | Unit | Condition |
|--------|--------|--------|--------|--------|--------|--------|
| Propagation Delay | | 16 | 22| 36 | us | T=|
| leakage power |  | 23 | 38 | 52| pW| T= |
| power dissipation | | 8 | 14 | 23 | uW | T=|
|  VDD | Supply Voltage | 1.8 | 5| 12 | V | T=27C |
| leakage current | | 2.8 | 3.6 | 5.3 | uA| T=|
# Open source tools used
# esim
eSim (previously known as Oscad / FreeEDA) is a free/libre and open source EDA tool for circuit design, simulation, analysis and PCB design.
It is an integrated tool built using free/libre and open source software such as KiCad, Ngspice and GHDL.
# ngspice
ngspice is the open source spice simulator for electric and electronic circuits.
http://ngspice.sourceforge.net/
# SkyWater Open Source PDK
The SkyWater Open Source PDK is a collaboration between Google and SkyWater Technology Foundry to provide a fully open source Process Design Kit and related resources, which can be used to create manufacturable designs at SkyWater’s facility.
https://github.com/google/skywater-pdk
# Installing esim 
# For windows
* Download eSim for Windows OS from "https://esim.fossee.in/". Disable the antivirus (if any).
* Now double click on eSim installer and then follow the instruction to install eSim.
* After the installation is completed, please download and add the following file to the esim home directory(FOSSEE\eSim\ folder):  https://github.com/FOSSEE/eSim/blob/master/src/frontEnd/TerminalUi.ui#L6
* Please download and add the following executable to the nghdl folder(FOSSEE\eSim\nghdl\src location):https://drive.google.com/file/d/17MNCCq9cG6A7fnIH-4KMUMY-yb4rW9s4/view?usp=sharing
# Schenatic and Simulation
* open the esim and create a new project.<br>
* create the the schematic of your circuit using the esim_nmos and esim_pmos avaliable in the esim_library.<br>
* connect the components as per the design and annotate it using esim_annotation this gives the names to the each component in the schematic.<br>
* Run the esim_ERC , if there is any error in the circuit it will show and then rectify it. <br>
* create a NET LILST and it is saved in the created new project folder as .cir file. <br>
* copy the net list in the word then rearrange and save the file in the folder where sky_water_fd_pr is saved. <br>
*  sky130 from this link and unzip : https://static.fossee.in/esim/installation-files/sky130_fd_pr.zip <br>
* Save the .cir.out file in the sky_fd_pr folder as .cir file. <br>
* Open with notepad and add the path .lib "models/sky130.lib.spice" tt  at the top.<br>
* Replace with CMOSP, mos_p with sky130_fd_pr__pfet_01v8 and CMOSN, mos_n with  sky130_fd_pr__nfet_01v8. <br>
* To replace an inductor, capacitor, or resistor do it this way for example: L1 out gnd 1m by x1  out gnd mid 0 sky130_fd_pr__ind_03_90.<br>
Note: For more details go to the cells folder in sky_fd_pr. Open the specific component folder which you want to use. Then open the test folder and check the SPICE file. The SPICE file is an example of implementation of that component. You will get to know how to use the component in your ckt.<br>
* Now Run the ckt with ngspice <br>
# Running the ngspice circuit
Step1. Right click on the .cir file. <br>
Step2. Click on Open With <br>
Step3. Browse for the ngspice.<br>
Step4. If ngspice is not present scroll down click on More Apps. <br>
Step5. Go to the FOSSEE folder search for Ngspice. Run it.<br>
# simulation 
The input and oupt waveforms of the D FLIP FLOP using 130nm technology
![dff waveforms](https://github.com/user-attachments/assets/4dbd7891-7e2b-4946-9740-6ce4b71d8412)
progapagation delay
![rise and fall delay](https://github.com/user-attachments/assets/e91a031d-58f0-4028-bf21-44efd11f9305)
rise and fall time dealy 
![rise and fall delay](https://github.com/user-attachments/assets/38c0edf9-3e76-41c9-afdb-f6058c95b975)
# contributors
* karri Nishitha
# acknowledgments
* Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.
* Sumanto kar, Assistant Project Manager, FOSSEE
* Ashok velugoti




