# A 32-bit Single-Cycle RISC-V Processor Core

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Language](https://img.shields.io/badge/Language-Verilog-blue.svg)](./)
[![Tool](https://img.shields.io/badge/Tool-Vivado%202024.1-purple.svg)](./)

A single-cycle processor implementing the 32-bit RISC-V (RV32I) base integer ISA. Designed from the ground up in Verilog, this project serves as a robust foundation for exploring more advanced pipelined and SoC architectures.

## Key Features
* **ISA:** RV32I Base Integer Instruction Set
* **Architecture:** Single-Cycle Datapath
* **Modularity:** Designed different modules for ALU, Control Unit, Register File, etc., resulting in a modular approach to build the datapath
* **Reproducible Workflow:** Used `Makefile` for automating build processes

Find more information about the datapath architecture in [here](/doc/architecture.md).

## Project Tree


```
├── doc/                    # Documentation (Architecture, Diagrams)
├── hex/                    # hex file acting as the instruction mem (*.hex)
├── rtl/                    # Verilog RTL source files (*.v)
├── scripts/                # Build and simulation scripts (*.tcl)
├── tb/                     # Verilog testbenches
├── LICENSE                 # MIT License
└── Makefile                # Makefile for automating the build process
```

## Workflow using Make

This project uses a `Makefile` to automate all common tasks. All commands must be run from the root directory of the repository.

### Prerequisites
* Xilinx Vivado Design Suite (e.g., 2024.1 or later)
* `make` build automation tool

### Instructions

1.  **Clone the Repository:**
    ```shell
    git clone [https://github.com/Sreeram-Ramesh/riscv-single-cycle-core.git](https://github.com/Sreeram-Ramesh/riscv-single-cycle-core.git)
    cd riscv-single-cycle-core
    ```

2.  **Build the Vivado Project:**
    This command generates a fresh Vivado project in the `build/` directory using the provided Tcl script.
    ```shell
    make
    ```

3.  **Clean the Project:**
    This command completely removes the generated `build/` directory and all log files, ensuring a clean state.
    ```shell
    make clean
    ```

4.  **Open the Project in the GUI:**
    This command opens the generated project in the Vivado GUI for analysis and simulation.
    ```shell
    make gui
    ```

## Future Works
- Currently making progress in designing a 5-staged RISC-V processor core.
- Targeting more ISA extensions.     

## Acknowledgements

 - [e-Yantra 2024 Competition](https://www.e-yantra.org/)
 - [IIT Hyderabad Next Gen Computer Architecture (ROCA 2025)](https://www.linkedin.com/posts/department-of-cse-iit-hyderabad_roca2025-iithyderabad-intelindia-activity-7353655624469037058-1N_4?utm_source=share&utm_medium=member_ios&rcm=ACoAADkvqGUB94WOdm3s7FTbFnSzMv0dUWeNtaY)
 - [RISCV Handbook - Patterson and Hennessy](https://www.cs.sfu.ca/~ashriram/Courses/CS295/assets/books/HandP_RISCV.pdf)