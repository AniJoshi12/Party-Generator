# DESIGN OF EVEN/ODD 4-BIT PARITY GENERATOR USING TWO TRANSISTOR XOR MODULE
This repository presents the design of Parity Generator using 28nm CMOS Technology alongwith Synopsis Custom Compiler.
# Table Of Content
- [Abstract](https://github.com/aniJoshi12/Parity-Generator/blob/main/Abstract)
2.  Introduction

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

# Tool Used
- Synopsys Custom Compiler: The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart
of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.

- Synopsys Primewave: PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.

- Synopsys 28nm PDK: The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# CMOS Inverter Gate
![Inverter](https://user-images.githubusercontent.com/100522966/155893158-d4e660bd-86b3-4030-a142-3747dd995419.JPG)

# CMOS XOR Gate
![Xor](https://user-images.githubusercontent.com/100522966/155893190-c46562ef-97d0-49e3-8f29-ba2f571bc662.JPG)


