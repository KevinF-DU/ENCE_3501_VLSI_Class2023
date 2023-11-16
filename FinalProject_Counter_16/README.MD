# Lab 6: Counter 16

## Table of Contents
- [Lab Description](#lab-description)
- [AND](#and)
  - [AND Schematic](#and-schematic)
  - [AND Simulation](#and-simulation)
- [NOT](#not)
  - [NOT Schematic](#not-schematic)
  - [NOT Simulation](#not-simulation)
- [D Flip Flop](#d-flip-flop)
  - [D Flip Flop Schematic](#d-flip-flop-schematic)
  - [D Flip Flop Simulation](#d-flip-flop-simulation)
- [Counter](#counter)
  - [Counter Schematic](#counter-schematic)
  - [Counter Simulation](counter-simulation)


## Lab Description
The goal is to create 4 bit counter using D flip-flops and using standard cells is electric VLSI. All transistors are using the 1u spice modle.

## AND
First we will need a and gate in order to have an enable pin. When the enable and clock are high the counter will increase.

### AND Schematic
Create the schematic and an icon that resembles a 2-input AND.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/FinalProject_Counter_16/Images/and_sch.png)

### AND Simulation
Simulate the gate to ensure that it works properly. Apply all four inputs (00,01,10,11).

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/FinalProject_Counter_16/Images/and_sim.png)


## NOT
A not gate is also needed to get the inverse of the flip flop output.

### NOT Schematic
The schematic consists of only one NMOS and one PMOS.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/FinalProject_Counter_16/Images/inv_sch.png)

### NOT Simulation
Again simulate the gate using both inputs (0,1).

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/FinalProject_Counter_16/Images/inv_sim.png)


## D Flip Flop
Four D flip-flops are needed. One for each bit.

### D Flip Flop Schematic
The schematic is taken form the mudlib07 library.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/FinalProject_Counter_16/Images/ff_sch.png)

### D Flip Flop Simulation
To make the flip-flop a rising edge the ph1 pin is the clock, and the ph2 is the inverse of the clock.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/FinalProject_Counter_16/Images/ff_sim.png)

### Counter
Now put everything together to create the counter.

## Counter Schematic
The AND gate is used so the counter only counts when the enable is high, the NOTs are used to get inverse of the flip-flops. Ensure that the ph1 and ph2 pins ares set accordingly.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/FinalProject_Counter_16/Images/counter_sch.png)

## Counter Simulation
No simulate the counter to see if it counts up form 0 to 15 (4bits). I set the initial voltages of all bits to zero.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/FinalProject_Counter_16/Images/counter_sim.png)

To show that the enable pin works simulate with enable going to low halfway on the count.

![image](https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/FinalProject_Counter_16/Images/enb_sim.png)

To show that the reset works simulate witht he reset being low hlfway on the count.
https://github.com/KevinF-DU/ENCE_3501_VLSI_Class2023/blob/main/FinalProject_Counter_16/Images/reset_sim.png


