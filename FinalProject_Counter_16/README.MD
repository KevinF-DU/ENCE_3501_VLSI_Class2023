# Lab 6: DC-to-DC Charge Pump

## Table of Contents
- [Lab Description](#lab-description)
- [NAND2](#nand2)
  - [NAND2 Schematic](#nand2-schematic)
  - [NAND2 Simulation](#nand2-simulation)
- [NOT](#not)
  - [NOT Schematic](#not-schematic)
  - [NOT Simulation](#not-simulation)
- [Ring Oscillator](#ring-oscillator)
  - [Ring Oscillator Schematic](#ring-oscillator-schematic)
  - [Ring Oscillator Simulation](#ring-oscillator-simulation)
- [3 Stage Charge Pump](#3-stage-charge-pump)
  - [3 Stage Charge Pump Schematic](#3-stage-charge-pump-schematic)
  - [3 Stage Charge Pump Simulation](3-stage-charge-pump-simulation)
- [Regulator](#regulator)
  - [Regulator Schematic](#regulator-schematic)
  - [Regulator Simulation](#regulator-simulation)
-[DC-to-DC Charge Pump](#dc-to-dc-charge-pump)
  - [DC-to-DC Charge Pump Schematic](#dc-to-dc-charge-pump-schematic)
  - [DC-to-DC Charge Pump Simulation](#dc-to-dc-charge-pump-simulation)


## Lab Description
The goal of this lab is to build a DC-to-DC Charge Pump regulator. The charge
pump should output 2V and drive a 2 MΩ resistor.

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

## Ring Oscillator
The ring oscillator will utilize the NAND and NOT gates.

### Ring Oscillator Schematic
Connect an even number of NOT gates in series with a NAND gate. One input of the NAND is the enable, the other is the feedback from the NOT gates.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab6/Images/osc_sch.png)

## Ring Oscillator Simulation
Simulate the oscillator to ensure the signals are oscillating and out of phase of eachother.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab6/Images/osc_sim.png)

## 3 Stage Charge Pump
The charge pump will allow our voltage to increase from 1V to 2V. 

### Stage Charge Pump Schematic
Utilize the 2 oscillating signals as inputs to charge the capacitors.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab6/Images/chr_sch.png)

### Stage Charge Pump Simulation
Simulate the charge pump to ensure that the output reaches 2V.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab6/Images/chr_sim.png)

## Regulator
The regulator will control the voltage so it is not higher than 2V. 

### Regulator Schematic
The regulator will utilize two of the NOT gates.    

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab6/Images/reg_sch.png)

### Regulator Simulation
Simulate the regulator to ensure the enable output is high when the voltage is below 2V. My Regulator cuts off at 1V.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab6/Images/reg_sim.png)

## DC to DC Charge Pump
Now the DC-to-DC Charge Pump will utilize all of the above.

### DC to DC Charge Pump Schematic
Combine the Ring Oscillator, Charge Pump, and Regulator to creat the DC-to-DC Charge Pump.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab6/Images/DC_sch.png)

### DC to DC Charge Pump Simulation
Simulate to see if it is working properly. My regulator is not working properly so the DC-toDC- Charge Pump is not working.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/Lab6/Images/DC_sim.png)
