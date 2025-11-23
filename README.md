# My 8-Bit Computer Project

This was a project to build a functional 8-bit computer from scratch in a simulator. It was an amazing learning experience where I learned a ton about system architectures, bus systems, EPROMs, and how CPUs work (they aren't magic, but the transistor density is crazy). Also helped me gain an intuitive understanding of barebones systems logic, which made learning systems languages like C++ and Rust surprisingly simple. 

## Project Status: Halted

I've taken this project as far as I can. The simulation software I was using **cannot save the state of the memory chips**.

This is a critical blocker. It means I can't store the binary translations for my bytecode. Without a way to store the program, building a functional CPU to fetch and execute instructions is impossible, as the program would be erased every time I reopen the file. Furthermore, the lack of state saving made making a completely functional instruction ROM impossible.

### Implemented Components

* **Architecture:** 8-bit bus system
* **ALU:** Capable of basic 8-bit addition and subtraction.
* **Registers:** 2 value registers connected to the ALU.
* **RAM:** 16x8 bytes (16 bytes total).
* **Display:** 8-bit digital display.

### Unrealized Features

I also built the logic for a control unit, but these parts are useless without a CPU to manage them:

* **4-Bit Program Counter:** Can sequentially select memory addresses. Its value can also be changed, which would have allowed for loops and jumps.
* **Sum 0 Check:** A flag that, combined with the PC and a "CPU," would have been enough to make the computer Turing complete.

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
