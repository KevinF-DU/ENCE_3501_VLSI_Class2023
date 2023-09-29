# Lab 1: 5-Bit DAC

## Table of Contents
- [Lab Description](#lab-description)
- [General Schematic](#general-schematic)
- [Technology Description](#technology-description)
  - [Fabrication Process](#fabrication-process)
  - [Design Rules](#design-rules)
- [R_Divider Cell](#r_divider-cell)
  - [Electric Schematic](#electric-schematic)
  - [Electric Layout](#electric-layout)
- [5Bit DAC](#5bit-dac)
  - [Electric Schematic (DAC)](#electric-schematic-dac)
  - [Electric Layout (DAC)](#electric-layout-dac)
- [Lab Questions](#lab-questions)

## Lab Description
The goal with this lab is to design a 5-bit R-2R Ladder Digital to Analog Converter (DAC) without an op-amp.

## General Schematic
![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/5bit_DAC_schematic.png)

## Technology Description

### Fabrication Process

For all labs in this class, we are using the ON Semiconductor's C5 process and fabrication through [MOSIS](https://www.themosisservice.com/). This CMOS process has 3 metals layers, 2 poly layers, and a high resistance layer.

You can find more information about the process technology on this [link](https://www.onsemi.com/site/pdf/C5-D.PDF).

For this lab we are interested on the table that contains the device characteristic of resistors.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/resistor_c5_process.png)

### Design Rules

The labs are also using the MOSIS scalable CMOS (SCMOS) submicron design rules [(Link)](https://www.egr.msu.edu/classes/ece410/demlow/files/DRC_rule_scmos.pdf).

Since this lab is about resistors implemented at the well layer, below you have the table with the minimum dimensions for the well width, space and overlap.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/submicron_drc_rules.png)

## R_Divider Cell

This lab will use n-well resistors with a value of 10k Ohms. The technology we are using for the n-well ressitors is 855ohm/sq and a fixed widht of 15. To find the lenght of the resitors the equation below is used.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/IMG_0133.PNG)

### Electric Schematic

Since the DAC is a series of voltage dividers start by building the schematic of one voltage divider.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/r_div_sch.png)


Create a new schematic cell and drag in the voltage divider symbol. Use LTspice comands to simulate the circuit and verify that it works.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/r_div_sim_scm.png)

Giving an input of 5V gives an output of 1.66667V. This is accurate because the voltage out should be 1/3 of the input according to the voltage divider equations.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/r_div_sim_LTSPICE.png)

### Electric Layout

To make the layout follow the same design process of the schematic. Use n-well resistors and adjust them to the correct size. 
Make sure to space the resistors in a serpetine pattern and as close to each other as possible.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/r_div_lay.png)

Like before, to simulate the layout create a new cell and drag the layout symbol into it. Add the same LTpsice command to run the same simulation.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/r_div_sim_lay.png)

The simulation values should match the schematic simulation.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/r_div_lay_LTSPICE.png)

## 5Bit DAC
### Electric Schematic (DAC)

Create a new schematic cell and drag in the voltage divider icon 5 times (5 bits).
Arrange and wire them in series. Lable the inputs and outputs.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/5Bit_DAC_sch.png)

Simulate the DAC to verify that it is working properly. When giving b0 and b1 5V (logic 1) the binary number 00011 is the input of the DAC.
00011 is 3 in decimal so the out put will be .46875

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/IMG_0129.PNG)
![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/5Bit_DAC_sch_LTSPICE.png)

### Electric Layout (DAC)
For the layout, create a new layout cell and drag in the layout symbol 5 times. Place and wire them in series and also keeping them as close as possible.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/5Bit_DAC_lay.png)

Run a DRC and NCC to verify that the schematic and layout are wired correctly and have the same components.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/5Bit_DAC_sch_DRC_NCC.png)

## Lab Questions

- Find and explain how to determine the output resistance of the DAC.
  
Since the DAC is multiple voltage dividers in series you can start from the LSB and calculate the total resistance while moving up the circuit. The output resistance is 10K ohms.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/IMG_0132.PNG)

- Delay driving the load
  - Ground all DAC inputs except B4. Connect B4 to a pulse source (0 to vdd) and show and predict using 0.7RC, the delay the DAC has driving a 10pF load
  - Verify the simulation results match your hand calculation

First you calculate the time constant RC. RC = 100ns. When doing 0.7RC the time for the capacitor to reach 50% charge is around 70ns.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/IMG_0131.PNG)
![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/5Bit_DAC_10pCAP_LTSPICE.png)

- Simulations to verify your design functions correctly
  - Apply different values to the input of the DAC and check if the output has the correct value

Applying the value of 11111, the DAC outputs 4.84375V
![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/5Bit_DAC_11111.png)

Applying the value 01101, the DAC outputs 2.03125V

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/5Bit_DAC_01101.png)

  - Explain what happens if the DAC drives a 10k load

Since the output resistance of the DAC is 10K ohms, adding a load of 10K ohms will act as a voltage divider of 1/2.
The output value of the DAC will be half as much.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab1/images/IMG_0130.PNG)



