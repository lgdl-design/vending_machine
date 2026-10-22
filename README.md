# Vending Machine

Coin-Counting Vending machine that uses flip logic to simulate counting; operates using a custom-built PCB and does not use a microcontroller
![Megasumo V3 in competition](Images/In_Competition.png)

## Hardware

- **Flip-Flops:** Basic sequential circuit components that provide memory. Used to count coins in our vending machine
- **IR Sensor:** Sensor used to detect a coin falling. Pointed towards a black background and detects a change in color when a coin falls in front of it, activating the counting circuit, also used at the end of the vending machine to detect if the object has been dispensed, which resets the counter.
- **L293D:** Motor driver that runs our motor to activate the wheel mechanism used to dispense objects from the vending machine.
- **5V DC Motor:** Motor used to spin the wheel mechanism to dispense the object


## About The Machine

The vending machine was designed as a college project to demonstrate the use of flip-flops in other circuits. We used a jk flip-flop based asynchronous counter, which used the inputs read from the IR sensor to count up rather than using a clock like in normal counters. The jk flip flop also allows us to reset the counter using the input from the IR sensor placed at the end of the vending machine when the object is dispensed.

The machine is operated using a custom-built PCB which houses the logic components, including the gates, flip-flops, and other components which operate the rest of the machine. The PCB's output links to a 7 segment which displays the current count of the coins, and is also linked to the motor driver which drives the motor that allows us to dispense objects.
![Megasumo V3 chassis model](Images/Chassis_Model.png)


## Files

- Firmware: [SLU_SUMO.ino](firmware/SLU_SUMO.ino)
- CAD (STEP): [ASSEMBLY.step](3d_design/ASSEMBLY.step)
- CAD (STL): [ASSEMBLY.stl](3d_design/ASSEMBLY.stl)
