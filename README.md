# Intelx86-motherboard
In this project, I designed and implemented a system using the 8086 microprocessor to interface with a 7-segment display and push buttons. The objective is to demonstrate how the microprocessor can control and display numbers on the 7-segment display based on user input from the push buttons. Key components used include the 8086 microprocessor, 7-segment display, 74HC373 latches for data storage, 2716 EPROMs for program storage, resistors for current limiting, PPI 8255 for parallel interfacing, and 74LS138 decoders for address decoding. The primary goal of this project is to showcase the interaction between the 8086 microprocessor and external components in a simple embedded system setup. By pressing individual push buttons, users can input numbers that are then displayed sequentially on the 7-segment display. This demonstrates the microprocessor's ability to read input states, process them using programmed logic stored in EPROMs, and output the corresponding data to control the display. 

## Schematic Diagram of 8086 complete system:   

![schematic](https://github.com/user-attachments/assets/76344236-5c3e-4b13-babb-0fc380746d6c)  
# Modules:  
Modules that are used in this project are:  
## 1. 8086 Microprocessor (U1)  
### Function:  
8086 Microprocessor is an advanced version of the 8085 Microprocessor, designed by Intel in 1976. It is a 16-bit microprocessor. It has 16 bits of the data bus, which is why it can read or write either 16 bits or 8 bits of data at a time. It is a Central processing unit that executes instructions and controls other components.  
### Connections:  
**AD0-AD15:** Multiplexed address/data bus connected to the latches (U3, U5, U2).   
**A16-A19:** Address lines for higher addresses.   
**ALE (Address Latch Enable):** Signal used to latch the address into U3, U5, U2.   
**RD (Read), WR (Write):** Control signals for read and write operations connected to the EPROMs (U4, U6) and PPI (U10).   
**READY, RESET, CLK:** Signals connected to the clock generator and other timing control circuits. 
