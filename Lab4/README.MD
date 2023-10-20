# Lab 3: Inverters

## Table of Contents
- [Lab Description](#lab-description)
- [Inverter 1](#inveter-1)
  - [Inverter 1 Schematic](#inveter-1-schematic)
- [Inverter 1 Simulation](#inveter-1-simulation)
  - [Inverter 1 Layout](#inveter-1-layout)
- [Inverter 2](#inveter-1)
  - [Inverter 2 Schematic](#inveter-2-schematic)
  - [Inverter 2 Simulation](#inveter-2-simulation)
  - [Inverter 2 Layout](#inveter-2-layout)
- [Simulation with Load](simulation-with-load)


## Lab Description
Design two inverters with sizes 12u/6u (PMOS) 6u/6u (NMOS), and 
48u/6u (PMOS) 24u/6u (NMOS).

## Inverter 1

### Inverter 1 Schematic
For the first inverter schematic use a PMOS transistor of 12u/6u, and a NMOS transistor of 6u/6u.
Make sure to add the spice model in order to simulate the inverter. Add an icon and exports for input/outputs.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab4/images/inverter_1_sch.png)

### Inverter 1 Simulation
Using the spice command, simulate the inverter. The switching point is lower than vdd/2.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab4/images/inverter_1_sim.png)


### Inverter 1 Layout
For the layout create a PMOS and NMOS transitor like in previous labs, add vdd and ground rail, and add contact for the input/output.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab4/images/inverter_1_lay.png)

## Inverter 2

### Inverter 2 Schematic
Follow the same process of inverter one but change the size to 48u/6u (PMOS) 24u/6u (NMOS).

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab4/images/inverter_2_sch.png)

### Inverter 2 Simulation
Again simulate the inverter using the same spice code.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab4/images/inverter_2_sim.png)

### Inverter 2 Layout
For the layout create 4 PMOS and NMOS transitor using the sizes of inverter 1. The transitors can share sources and drains.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab4/images/inverter_2_lay.png)

## Simulation with Load
To simulate both inverters create a new schematic and bring in the icons for both inverters. Add exports for vin and vouts.
Both inverters will drive a capacitor of 100fF, 1pF, and 10pF.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab4/images/load_test_sch.png)

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab4/images/load_test_sim.png)



