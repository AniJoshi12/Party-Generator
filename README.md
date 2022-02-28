# DESIGN OF EVEN/ODD 4-BIT PARITY GENERATOR USING TWO TRANSISTOR XOR MODULE
This repository presents the design of Parity Generator using 28nm CMOS Technology and tool used is Synopsis Custom Compiler.
# Table Of Content
- [Abstract](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#Abstract)
- [Introduction](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#Introduction)
- [Working](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#Working)
- [Tool Used](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#Tool-Used)
- [CMOS Inverter Gate](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#CMOS-Inverter-Gate)
- [CMOS XOR Gate](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#CMOS-XOR-Gate)
- [Parity Generator](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#Parity-Generator)
- [Parity Generator Testbench Design](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#Parity-Generator-Testbench-Design)
- [Expected Waveform](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#Expected-Waveform)
- [Simulated Waveform](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#Simulated-Waveform)
- [Schematic Netlist](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#Schematic-Netlist)
- [References](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#References)
- [Acknowledgements](https://github.com/AniJoshi12/Party-Generator/blob/main/README.md#Acknowledgements)

# Abstract
In this paper , I am going to design Parity Generator using CMOS technology. MOSFETs are implemented using 28nm technology.
The parity generating method is one of the most widely used error detection techniques for data transmission which is designed
with the help of xor gates. The number of xor gates to be used depends on number of bits whose parity has to be checked.
Generally for N-bits, N-1 Xor gates are needed. So it is important to build xor gate with minimum number of transistors.
Conventionally to design xor gate it requires 8 transistors [If inverted inputs are present] which takes more area, consumes 
more power and delay is also more. So here I am designing xor with the help of 2 transistors [If inverted inputs are present] only 
which leads to decrease area , power consumption and delay.

# Introduction
Parity generator plays an integral part in digital communication for correcting and detecting the error. Now a days majority of 
communication is in digital form. Whenever we transmit the data from one point to another point then noise gets added into the data 
which has been send. Due to this there is chance of miscommunication means data could be changed from 0 to 1 or 1 to 0.
To remove all these changes we add parity bit to the last of the message signal depending on the number of ones in that message. 
If number of ones are odd then to make the even parity we add the 1 at the last of the message signal and add ‘0’ in case of odd 
parity to keep it as it is and vice versa in case of even number of ones.

# Working
Here we are designing 4 bit parity generator so as mentioned number of xor gates required to build this circuit will be 3.
So here we are giving 2 inputs to one xor gate and another 2 inputs to another one. Output of these respected results is
given to the another xor gate which produces even parity bit and if we connect inverter next to it, circuit produces odd parity 
bit. In the upcoming circuit we will see 2 inverters connected after the parity generator which are collectively acting as a buffer circuit.
Buffer circuit is used here to amplify the weak output so that output states will be clearly understandable.
- Truth Table
![IMG20220218174656__01](https://user-images.githubusercontent.com/100522966/156021375-95a4c002-123b-486d-bb41-f6431148d66b.jpg)

- The truth table can be verified with the help of following calculations


![image](https://user-images.githubusercontent.com/100522966/156019591-67a3fc94-c704-463d-94dc-8878aa3cd674.png)

Coming to the CMOS Design , I designed xor gate with the help 
of 2 transistors and for each xor gate there is need of one 
complementary input which is designed with the help of inverters. 
For 4 bit Parity generator there is need of 3 xor circuits and for 
complete xor operation it takes 4 transistors, so total number of 
transistors to design this circuit is 12. 


# Tool Used
- Synopsys Custom Compiler: The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart
of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.

- Synopsys Primewave: PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.

- Synopsys 28nm PDK: The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# CMOS Inverter Gate
![Inverter](https://user-images.githubusercontent.com/100522966/155893158-d4e660bd-86b3-4030-a142-3747dd995419.JPG)

# CMOS XOR Gate
![Xor](https://user-images.githubusercontent.com/100522966/155893190-c46562ef-97d0-49e3-8f29-ba2f571bc662.JPG)

# Parity Generator
![Parity_gene](https://user-images.githubusercontent.com/100522966/156007810-cc253626-0b31-4a6e-8a32-caff9ab709b0.JPG)

# Parity Generator Testbench Design
![Parity_gene_tb](https://user-images.githubusercontent.com/100522966/156007922-3579f5fd-f365-487b-8016-445c631a3551.JPG)

# Combination For Input
- A:
 
![ip A](https://user-images.githubusercontent.com/100522966/156022526-96dee06f-ed3b-485f-948a-1d96c6bfe70a.JPG)

- B:
 
![ip B](https://user-images.githubusercontent.com/100522966/156022547-102831a6-5391-4bdb-85b5-94275114c583.JPG)

- C:
 
![ip C](https://user-images.githubusercontent.com/100522966/156022571-6044901f-200e-46bb-87c2-319e3cc2b596.JPG)

- D:
 
![ip D](https://user-images.githubusercontent.com/100522966/156022588-2464d4ce-24c8-4e56-a09b-f662dae5205d.JPG)


# Expected Waveform
![IMG20220218174033__01](https://user-images.githubusercontent.com/100522966/156008116-5f51fd3f-8820-4725-8ebd-84ab43a0ba35.jpg)

# Simulated Waveform
![Parity_gene_wave](https://user-images.githubusercontent.com/100522966/156008074-c6031885-7147-4c40-846a-244d4950f7dd.JPG)

# Schematic Netlist
The netlist is present here : [Netlist](https://github.com/AniJoshi12/Party-Generator/edit/main/Netlist)
*  Generated for: PrimeSim
*  Design library name: Parity_gene
*  Design cell name: final_tb
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Mon Feb 28 16:01:18 2022

.global gnd!
********************************************************************************
* Library          : cp_lib1
* Cell             : cp_inv
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt cp_inv a vdd vss y
xm0 y a vss vss n105 w=0.1u l=30n nf=1 m=1
xm11 y a vdd vdd p105 w=0.3u l=0.03u nf=1 m=1
.ends cp_inv

********************************************************************************
* Library          : cp_lib1
* Cell             : cp_xor
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt cp_xor a b vdd vss y
xi0 a vdd vss net12 cp_inv
xm5 y b a vdd p105 w=0.1u l=0.03u nf=1 m=1
xm2 y b net12 vss n105 w=0.1u l=30n nf=1 m=1
.ends cp_xor

********************************************************************************
* Library          : Parity_gene
* Cell             : final
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt final a b c d vdd vss y yb
xi2 net15 net14 vdd vss net27 cp_xor
xi1 c d vdd vss net15 cp_xor
xi0 a b vdd vss net14 cp_xor
xi4 yb vdd vss y cp_inv
xi3 net27 vdd vss yb cp_inv
.ends final

********************************************************************************
* Library          : Parity_gene
* Cell             : final_tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi0 a b c d net28 gnd! y yb final
v1 net28 gnd! dc=1.05
v5 d gnd! dc=0 pulse ( 0 1.05 0 1n 1n 1u 2u )
v4 c gnd! dc=0 pulse ( 0 1.05 0 1n 1n 2u 4u )
v3 b gnd! dc=0 pulse ( 0 1.05 0 1n 1n 4u 8u )
v2 a gnd! dc=0 pulse ( 0 1.05 0 1n 1n 8u 16u )
c12 yb gnd! c=0.1p
c6 y gnd! c=0.1p








.tran '1u' '16u' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(a) v(b) v(c) v(d) v(y) v(yb)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end

# Acknowledgements
- [Kunal Ghosh , Co-Founder , VSD Corp. Pvt. Lim.](https://github.com/kunalg123)
- [Synopsys India](https://www.synopsys.com/)
- [Indian Institute Of Technology , Hyderabad ](https://iith.ac.in/)
- Chinmay Panda , IIT Hyderabad
- Sameer Durgoji , NIT Karnataka

# References
[1] Abhishek Shukla , Subodh Wairya, “DESIGN OF ODD-EVEN 
PARITY GENERATOR USING SIX TRANSISTORS XOR-XNOR,” 
IRJET,2019

[2] M.Sai Lakshmi , K.Mahammad Haneef , T.V.Nirmala , Dr.T.Lalith 
Kumar , S.Saleem “6T FA Using 2T EX-OR Gate”, SSRG - IJECE –
Volume 5 Issue 9 – Sep 2018

[3] https://www.electronicshub.org/parity-generator-and-parity-check/

[4] https://old.amu.ac.in/emp/studym/100006525.pdf

# Author
Aniruddha Abhay Joshi , MTech VLSI Design , Vellore Institute Of Technology , Vellore
