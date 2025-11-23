# My 8-Bit Computer Project

This was a project to build a functional (hypothetically Turing-complete) 8-bit computer from scratch in a simulator. It was an amazing learning experience where I learned a ton about system architectures, bus systems, EPROMs, and how CPUs work (they aren't magic, but the transistor density is crazy). Also helped me gain an intuitive understanding of barebones systems logic, which made learning systems languages like C++ and Rust surprisingly simple. 

## Simulator Used

This project was built using the **Logic.ly** online demo. You can try it out here:

[![Simulator: Logic.ly](https://img.shields.io/badge/Simulator-Logic.ly-blue)](https://logic.ly/demo/)

## Project Status: Halted

I've taken this project as far as I can. The simulation software I was using **cannot save the state of the memory chips**.

This is a critical blocker. It means I couldn't create a permanent **Instruction ROM** to store the binary translations (bytecode) for my instruction set. Without a stored program, building a functional CPU to fetch and execute instructions is impossible, as the program would be erased every time I reopen the file.

### Implemented Components

* **Architecture:** 8-bit bus system
* **ALU:** Capable of basic 8-bit addition and subtraction.
* **Registers:** 2 value registers connected to the ALU.
* **RAM:** 16x8 bytes (16 bytes total).
* **Display:** 8-bit digital display.
* **Register Flags:** 0 Check Sum
* **4-Bit Program Counter:** Can sequentially select memory addresses. Its value can also be changed, which *would have* allowed for loops and jumps if a CPU were present.

### Missing CPU / Control Unit Components

Because of the save-state limitation, I could not build the final pieces of the Control Unit:

* **Instruction ROM:** To store the "syntax table" or a persistent list of bytecode instructions.
* **Instruction Decoder:** The logic required to translate an instruction's bytecode (e.g., `0001`) into the correct control signals (e.g., "Enable Register A," "Enable ALU," "Write to Register B").
* **Full CPU:** The final integration of all these parts to create a working fetch-decode-execute cycle.

## Repository Purpose

This repository now serves as an archive of my component designs. I'm storing the schematics for all the chips I built in case I ever want to restart this project in a different environment.

### Included Chip Designs

* ALU
* 4-Bit Adder
* Half-Adder
* Full-Adder
* 8-Bit Bus I/O
* Bus Pins
* 4-Bit Counter (Program Counter)
* 8-Bit Memory
* 16x8 byte RAM
* 4-Bit Memory Address Decoder
* 8-Bit to 3 Digital Display (7447)
* Bit Inverter
* D Flip-Flop (tied PRE and CLR)
* Dable
