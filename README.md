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
## 2. Latches (74HC373) (U5, U3, U2):  
### Function:  
The 74HC373; 74HCT373 is an octal D-type transparent latch featuring separate D-type inputs for each latch and 3-state outputs for bus oriented applications. A latch enable (LE) input and an output enable (OE) input are common to all latches. It also De-multiplexes the address/data bus to separate the address lines.  
### Connections:  
Inputs (AD0-AD7) from 8086 to latches.   
Outputs (A0-A7) from latches to the address bus.   
LE (Latch Enable) Connected to ALE from the microprocessor.   
## 3. Decoders (74LS138) (U7, U8):  
### Function:   
The 74LS138 is a 3:8 Decoder IC that is commonly used in decoding or de-multiplexing circuits for memory decoding or data routing process. It is designed for high-speed operations and has three enable pins to make it easier to cascade with other ICs. It decodes the address lines to select specific memory or I/O devices.  
### Connections:   
Address Inputs (A, B, C): Connected to the address lines.   
Enable Inputs (G1, G2A, G2B): Enable signals for the decoder, connected to the control bus.   
Outputs (Y0-Y7): Connected to chip select inputs of the EPROMs (U4, U6) and PPI (U10).   
## 4. EPROMs (2716) (U4, U6):  
### Function:  
The Intel 2716 is a 16,384-bit ultraviolet erasable and electrically programmable read-only memory (EPROM). The 2716 operates from a single 5-volt power supply, has a static standby mode, and features fast single address programming.  It makes designing with EPROMs fast, easy and economical. It has Non-volatile memory storing the program code.  
### Connections:   
Address Inputs (A0-A10): Connected to the address bus.   
Data Outputs (D0-D7): Connected to the data bus. 
Control Inputs (CE, OE): Chip Enable and Output Enable, connected to the control signals from the decoder (U7, U8). 
## 5. PPI (8255) (U10):  
### Function:  
PPI 8255 is a general purpose I/O device designed to interface the CPU with its outside world such as ADC, DAC, keyboard etc. We can program it according to the given condition. It can be used with almost any microprocessor. It consists of three 8-bit bidirectional I/O ports i.e. PORT A, PORT B and PORT C.  
### Connections:    
Data Bus (D0-D7): Connected to the data bus.   
Control Signals (CS, RD, WR): Chip Select, Read, and Write signals connected to the microprocessor and decoders.   
Ports (PA0-PA7, PB0-PB7, PC0-PC7): Connected to peripheral devices like the 7-segment display and LEDs.   
## Simulation Results  

![image](https://github.com/user-attachments/assets/c0c6b92c-a96f-4d3e-bee7-9afcde644046)  
![image](https://github.com/user-attachments/assets/6848dfbb-175f-40e9-bf53-4d33c4c2dc1a)  
![image](https://github.com/user-attachments/assets/9eb0cc2c-ee95-45a1-a433-26467f290584)  

## Hardware Implementation  
![WhatsApp Image 2025-02-21 at 3 12 38 AM](https://github.com/user-attachments/assets/a68b0c73-7576-4845-9730-fedd2dde1f70)  
![WhatsApp Image 2025-02-21 at 3 12 38 AM (1)](https://github.com/user-attachments/assets/4a3194e2-8caa-4a74-8006-69602e5092ff)  






