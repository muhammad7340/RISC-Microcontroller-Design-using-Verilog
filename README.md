# 🧮 Multicycle RISC style Microcontroller Design using Verilog

 

[![Verilog](https://img.shields.io/badge/Verilog-HDL-blue)](https://en.wikipedia.org/wiki/Verilog)[![VHDL](https://img.shields.io/badge/VHDL-HDL-purple)](https://en.wikipedia.org/wiki/VHDL)[![Quartus Prime](https://img.shields.io/badge/Quartus%20Prime-Intel%20FPGA-green)](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/overview.html)[![ModelSim](https://img.shields.io/badge/ModelSim-Mentor%20Graphics-red)](https://www.mentor.com/products/fv/modelsim/) [![Xilinx Vivado](https://img.shields.io/badge/Xilinx%20Vivado-FPGA-orange)](https://www.xilinx.com/products/design-tools/vivado.html)  [![Digital Logic](https://img.shields.io/badge/Digital%20Logic-Design-brightgreen)](https://en.wikipedia.org/wiki/Digital_electronics)  [![Embedded Systems](https://img.shields.io/badge/Embedded%20Systems-Development-blue)](https://en.wikipedia.org/wiki/Embedded_system)  [![Computer Architecture](https://img.shields.io/badge/Computer%20Architecture-Hardware-orange)](https://en.wikipedia.org/wiki/Computer_architecture)  [![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

 ![Microcontroller](/docs/multicycle_microcotroller.jpg)

 
## 🚀 Overview
This project presents a **custom-designed RISC-based microcontroller** implemented using Verilog, featuring a simplified instruction set, Harvard architecture, and non-pipelined execution. The design ensures efficient processing, reduced cycle time, and optimized resource utilization.

## 🎯 Objectives
- Design a **RISC-based** microcontroller using Verilog.
- Implement **Arithmetic Logic Unit (ALU)**, **Control Unit (CU)**, **Registers**, **Multiplexers (MUX)**, **Memory (Program & Data)**, and **Program Counter (PC) Adder**.
- Execute various **instruction sets** and validate the design through simulation.


**🔹 Concepts & Core Skills:**  
- Digital Logic Design  
- FPGA Programming  
- Embedded Systems  
- Microcontroller Design
 
## 🏗️ Architecture & Components

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/1ac83aff-6d60-463a-8179-c9e2bbfff911" />



### 1️⃣ **Control Unit (CU)**
Manages the execution flow by decoding instructions and generating control signals.

### 2️⃣ **Arithmetic Logic Unit (ALU)**
Performs arithmetic operations (addition, subtraction) and logical operations (AND, OR, XOR).

### 3️⃣ **Registers**
Stores intermediate and final computation results for efficient data handling.

### 4️⃣ **Program Counter (PC) Adder**
Increments the program counter to fetch the next instruction.

### 5️⃣ **Multiplexers (MUX1 & MUX2)**
Selects appropriate input data for ALU and memory operations.

### 6️⃣ **Memory (Program & Data)**
- **Program Memory (PMem):** Stores instruction codes.
- **Data Memory (DMem):** Stores data required for operations.

## 📜 Instruction Set
### 🔄 **Data Transfer Group**
- `MOVAM`: Move accumulator value to memory.
- `MOVMA`: Move memory value to accumulator.
- `MOVIA`: Move immediate value to accumulator.

### ➕ **Arithmetic Group**
- `ADD`: Perform addition.
- `SUB`: Perform subtraction.
- `INC`: Increment accumulator value.
- `DEC`: Decrement accumulator value.

### 🔣 **Logical Group**
- `AND`: Logical AND operation.
- `OR`: Logical OR operation.
- `XOR`: Logical XOR operation.

### 🔁 **Branching Group**
- `JMP`: Unconditional jump.
- `JNZ`: Jump if zero flag is not set.

### ⚙ **Machine Control Group**
- `NOP`: No operation.

## 🛠️ Implementation using Verilog

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/13d977ba-d9ef-4db4-8327-aad897d55296" />

This microcontroller is implemented using Verilog HDL, structured into modular components:

- `control_unit.v`: Implements control logic.
- `alu.v`: Defines arithmetic and logical operations.
- `registers.v`: Manages data storage.
- `mux.v`: Implements multiplexer logic.
- `memory.v`: Defines program and data memory.
- `pc_adder.v`: Handles program counter incrementation.
- `testbench.v`: Simulates and verifies the design.

  
## ✅ Verification & Simulation
### 🔬 Sample Test 1: Finding Maximum of Three Numbers
- Compares three numbers (e.g., `5, 12, 2`) and stores the largest in the accumulator.
- **Simulation Results:** Verified using Verilog testbench.

### 🔬 Sample Test 2: Logical and Arithmetic Operations
- Performs a sequence of logical and arithmetic operations.
- **Simulation Results:** Correct values stored in Data Memory (DMem).

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/3aea3eed-eeb5-4102-b974-332e2135e9c0" />


## 📌 Methodology
1. **Design & Planning:** Define architecture and instruction set.
2. **Implementation:** Code microcontroller modules in Verilog.
3. **Simulation & Testing:** Verify correctness using sample test cases.
4. **Optimization:** Improve efficiency and reduce hardware cost.
5. **Final Verification:** Validate through comprehensive simulations.

## 📄 Future Enhancements

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/10ad34ca-f55e-43f9-a52f-84dee12e878f" />

## 📁 Project Files
```
Advanced-RISC-Microcontroller-Design-using-Verilog/
├── 📜 README.md                   # Project Overview
├── 📂 src/                        # Source Code
│   ├── Adder.v                    # Adder Module
│   ├── ALU.v                      # Arithmetic Logic Unit
│   ├── ControlUnit.v              # Control Unit Module
│   ├── DMem.v                     # Data Memory Module
│   ├── instr_set.dat              # Instruction Set Data
│   ├── Microcontroller.v          # Main Microcontroller Module
│   ├── Microcontroller.v.bak      # Backup of Microcontroller Module
│   ├── MicroController_tb.v       # Testbench for Microcontroller
│   ├── MicroController_tb.v.bak   # Backup of Testbench
│   ├── MUX.v                      # Multiplexer Module
│   ├── PMem.v                     # Program Memory Module
│   ├── test_1.txt                 # Test File 1
│   ├── test_2.txt                 # Test File 2
│   ├── Microcontroller.qpf        # Quartus Prime Project File
│   ├── Microcontroller.qsf        # Quartus Settings File
│   ├── Microcontroller.qws        # Quartus Workspace File
│   ├── Microcontroller_nativelink_simulation.rpt  # Simulation Report
│   ├── c5_pin_model_dump.txt      # Pin Configuration
├── 📂 docs/                       # Documentation
│   ├── Project_Report.pdf         # Project Report
│   ├── architecture_diagram.png   # Architecture Diagram
├── 📂 simulation/                 # Test Results & Waveforms
│   ├── RTL_diagram.png            # RTL Diagram
│   ├── Timming_diagram_testbench.png  # Timing Diagram from Testbench
├── 📜 LICENSE                     # License File
└── 📜 .gitignore                  # Git Ignore File
```
## 📜 References
- Harvard Architecture: [Wikipedia](https://en.wikipedia.org/wiki/Harvard_architecture)
- Verilog HDL: [IEEE Standard 1364-2005](https://standards.ieee.org/standard/1364-2005.html)
- RISC Concept: [Computer Science Guide](https://en.wikipedia.org/wiki/Reduced_instruction_set_computer)

## 🏆 Conclusion
This project successfully implements a **custom RISC-based microcontroller** in Verilog. The architecture, instruction set, and simulation results validate the functionality and efficiency of the design. Future enhancements can further optimize the microcontroller’s performance.

---

🚀 **Designed & Developed by:** ahtishamsudheer@gmail.com

🌟 If you found this project useful, don’t forget to give it a ⭐ on GitHub!
