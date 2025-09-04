This is a detailed description of the provided Logisim-evolution circuit file, which represents a 22-bit single-cycle MIPS CPU. The circuit is a comprehensive implementation of a processor's core functionality, demonstrating a strong grasp of computer organization and architecture principles.

Overview

The CPU's design follows the classic single-cycle architecture. All instructions are executed within a single clock cycle, with data flowing sequentially through the various components. The circuit is well-organized, with distinct blocks for the data path and the control unit.

Key Components and their Functions

Instruction Memory: A ROM (Read-Only Memory) component acts as the instruction memory. It is configured to handle 22-bit addresses and outputs 22-bit data, which corresponds to the instruction size. This component holds the program's instructions.
Program Counter (PC): The PC is a register that stores the memory address of the next instruction to be fetched. It is incremented by a 22-bit adder to move to the subsequent instruction in memory for sequential execution.
Register File: A custom sub-circuit named Reg22Bit serves as the register file. This is where the CPU stores data and intermediate results. It has three primary ports: two read ports (Rs, Rt) for retrieving data from two registers simultaneously and one write port (Rd) for writing data back to a register.
Data Memory: A RAM (Random-Access Memory) component is included for data storage. It's configured with 22-bit address and data widths, enabling the CPU to load and store data during program execution.
ALU (Arithmetic Logic Unit): The ALU is the core computational component. It receives two 22-bit inputs and an ALUOp control signal from the control unit to perform operations such as addition, subtraction, AND, and OR.
Control Unit: The control unit, likely a combinational logic circuit, is the "brain" of the CPU. It takes the instruction's opcode as input and generates all the necessary control signals (RegWrite, MemWrite, MemRead, ALUOp, etc.) to coordinate the operations of the other components.
Multiplexers (Muxes): These are used extensively throughout the circuit to select the correct data path. For example, a multiplexer determines whether the write data for the register file comes from the ALU's output or from the data memory.
Splitters: These components are used to break down the 22-bit instruction into smaller, manageable fields, such as the opcode, register addresses (Rs, Rt, Rd), and the immediate value.

Demonstrated Skills

This Logisim file serves as a practical portfolio piece, showcasing your ability to design and implement a complex digital system. It confirms a strong working knowledge of MIPS architecture, data path and control unit design, and the use of core components like memory, registers, and an ALU to create a functional processor.
