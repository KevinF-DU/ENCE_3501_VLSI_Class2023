# Lab 1: 5-Bit DAC with PadFrame

## Table of Contents
- [Lab Description](#lab-description)
- [pWell nActive](#pwell-nactive)
  - [pWell nActive Schematic](#pwell-nactive-schematic)
  - [pWell nActive Layout](#pwell-nactive-layout)
- [pActive nWell](#pactive-nwell)
  - [pActvie nWell Schematic](#pactive-nwell-schematic)
  - [pActvie nWell Layout](#pactive-nwell-layout)
- [Pad cell with ESD protection](padcell-with-esd-protection)
  - [Pad with ESD Schematic](#pad-with-esd-schematic)
  - [Pad with ESD Layout](#pad-with-esd-layout) 
  - [Padframe with Buses](#padframe-with-buses)
- [Padframe with NMOS](#padframe-with-nmos)
  - [Padframe with NMOS Schematic](#padframe-with-nmos-schematic)
  - [Padframe with NMOS Layout](#padframe-with-nmos-layout) 

## Lab Description
Design a die that allows connecting an NMOS transistor to the outside world. The
padframe pads should contain a basic ESD protection.


## pWell nActive
First we need to desingn the pWell nActive diode

### pWell nActive Schematic
Begin by creating a schematic for the pWell nActive diode as shown.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab3/images/pWell_sch.png)

### pWell nActive Layout
Next create the layout. Make sure the pWell and nActive are touching but not overlapping.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab3/images/pWell_lay.png)

## pActive nWell
Next we need to desingn the pActive nWell diode.

### pActive nWell Schematic
Like before desing the schematic.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab3/images/nWell_sch.png)

### pActive nWell Layout
Just like the pWell nActive, desing the layout.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab3/images/nWell_lay.png)

## Padcell with ESD Protection
Add the diodes to the padcell in order to have ESD protection from the outside world. Make sure to add the vdd and gnd buses.

### Pad with ESD Schematic
![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab3/images/padESD_sch.png)

### Pad with ESD Layout
![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab3/images/padESD_lay.png)

### Padframe with buses
![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab2/images/DAC_sch.png)

## Padframe with NMOS
The NMOS only has 4 inputs/outputs so only 4 pads are needed. The drawn sizes of the pads are 400 x 400.

### Padframe with NMOS Schematic
Drag the NMOS and Padframe schematics and name the pins acrodingly.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab3/images/final_icESD_sch.png)

### Padframe with NMOS Layout
Drag in the NMOS and PAdframe layouts and wire them like the schematic.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab3/images/final_icESD_lay.png)

