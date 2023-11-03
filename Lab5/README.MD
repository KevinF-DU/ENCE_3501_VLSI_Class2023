# Lab 5: Full Adder

## Table of Contents
- [Lab Description](#lab-description)
- [NAND2](#nand2)
  - [NAND2 Schematic](#nand2-schematic)
  - [NAND2 Layout](#nand2-layout)
  - [NAND2 Simulation](#nand2-simulation)
- [NOT](#not)
  - [NOT Schematic](#not-schematic)
  - [NOT Layout](#not-layout)
  - [NOT Simulation](#not-simulation)
- [XOR2](#xor2)
  - [XOR2 Schematic](#xor2-schematic)
  - [XOR2 Layout](#xor2-layout)
  - [XOR2 Simulation](#xor2-simulation)
- [Full Adder](#full-adder)
  - [Full Adder Schematic](#full-adder-schematic)
  - [Full Adder Layout](#full-adder-layout)
  - [Full Adder Simulation](#full-adder-simulation)


## Lab Description
Design a full adder using 6u/2u MOSFETS that implements NAND2, NOT, and XOR2 gates.

## NAND2
First begin with the 2-input NAND gate. All gates will use 6u/2u MOSFTES.

### NAND2 Schematic
Create the schematic and an icon that resembles a 2-input NAND.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/NADN2_sch.png)

### NAND2 Layout
Next create the layout, as shown below.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/NADN2_lay.png)

### NAND2 Simulation
Simulate the gate to ensure that it works properly. Apply all four inputs (00,01,10,11).

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/NADN2_sch_sim.png)
![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/NADN2_sim.png)

## NOT
Next create a NOT gate. Again use 6u/2u MOSFETS.

### NOT Schematic
The schematic consists of only one NMOS and one PMOS.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/NOT_sch.png)

### NOT Layout
The layout will look like the one below.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/NOT_lay.png)

### NOT Simulation
Again simulate the gate using both inputs (0,1).

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/NOT_sch_sim.png)
![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/NOT_sim.png)

## XOR2
The last gate needed is the 2-input XOR gate. It uses two of the previous NOT gate created.

### XOR2 Schematic
Begin by creating the schematic. 

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/XOR2_sch.png)

### XOR2 Layout
For the layout first create a stick diagram in order to properly arrange the inputs.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/stick_diagram.jpg)

This will make creating the layout easier.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/XOR2_lay.png)

## XOR2 Simulation
Simulate all four inputs (00,01,10,11).

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/XOR2_sch_sim.png)
![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/XOR2_sim.png)

## Full Adder
Now utilize the gates to create a full adder.

### Full Adder Schematic
The schematic uses two XOR and three NAND gates.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/full_adder_sch.png)

### Full Adder Layout
Drag in the layouts of the gates to create the full adder. Connect all VCC's and GND's together.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/full_adder_lay.png)

### Full Adder Simulation
Simulate all 8 inputs(000,001,010,011,100,101,110,111).

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/full_adder_sch_sim.png)
![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab5/images/full_adder_sim.png)


There is a glitch when A goes form HIGH to LOW causing Cout and S to be wrong. This is due to the time delay it takes the logic change to affect the entire circuit.
