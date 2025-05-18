# IDEGEN PROCESSOR - A Custom 19-bit Computer Architecture

This repository contains the design documentation (in PDF format) for the **IDEGEN PROCESSOR**, a custom-designed 19-bit basic computer architecture. This project details the complete conceptualization of a processor, from its instruction format and addressing modes to its memory organization, instruction set, control signals, and core components.

## Project Overview

The IDEGEN PROCESSOR is designed with a 19-bit instruction word, carefully partitioned to specify the addressing mode, the operation to be performed (opcode), and the data or memory location involved (operand). Key features of this architecture include:

* **19-bit Instruction Format:** Allowing for a rich set of instructions and addressing capabilities.
* **Memory Architecture:** A 4096-word (2^12) main memory, with a dedicated 511-word section reserved for stack operations. Each memory word has a width of 19 bits.
* **Four Addressing Modes:** The processor implements four distinct addressing modes, enhancing flexibility in accessing operands:
    * **Direct Addressing:** The operand field directly specifies the memory address.
    * **Indirect Addressing:** The operand field points to a memory location containing the actual address of the operand.
    * **Immediate Addressing:** The operand field itself contains the value to be used in the operation.
    * **Indexed Addressing:** The effective address is calculated by adding the operand field to the value in the Index Register.
* **Comprehensive Instruction Set:** A 5-bit opcode enables up to 32 unique instructions, categorized into three primary types:
    * **Memory Reference Instructions:** Operations that involve accessing and manipulating data in the main memory.
    * **Register Reference Instructions:** Operations that are performed directly on the processor's internal registers.
    * **Input/Output Instructions:** Operations that facilitate communication with external devices.
* **Essential Register Set:** The processor incorporates a set of crucial registers for its operation, including:
    * Accumulator (AC) for arithmetic and logic operations.
    * Program Counter (PC) to track the address of the next instruction.
    * Address Register (AR) to hold the memory address for the current operation.
    * Data Register (DR) to temporarily store data being read from or written to memory.
    * Index Register (IX) to support indexed addressing.
    * Temporary Register (TR) for holding intermediate calculation results.
    * Stack Pointer (SP) to manage the stack memory.
    * Input Register (INPR) to receive data from input devices.
    * Output Register (OUTR) to send data to output devices.
* **Control Flags:** Several key flags (implemented as flip-flops) manage the processor's state and control its behavior, including flags for addressing mode selection, sequence control, extended arithmetic results, interrupt handling, and input/output status.
* **Arithmetic Logic Unit (ALU):** A versatile ALU capable of performing eight distinct operations, including arithmetic, logical, shift, comparison, and code conversion functions (Binary to Gray and Gray to Binary).
* **Custom Control Unit:** A dedicated control unit designed to interpret instructions and generate the necessary control signals for the processor's operation, featuring a 5x32 decoder to handle the instruction opcodes and logic for managing the different addressing modes.
* **Detailed Execution Cycles:** The design includes a well-defined Fetch-Decode-Execute cycle for instruction processing, as well as a mechanism for handling interrupts.

## Included Files

* `IDEGEN PROCESSOR Design.pdf`: The complete documentation detailing the architecture, instruction set, and operational aspects of the IDEGEN PROCESSOR.

## Key Components and Concepts Explored

This project delves into the fundamental aspects of computer architecture, including:

* Instruction set design and encoding.
* Implementation of various addressing modes.
* Memory organization and stack management.
* The role and operation of key processor registers.
* The function of control flags in managing processor state.
* The design and capabilities of an Arithmetic Logic Unit.
* The architecture and control logic of a basic Control Unit.
* The step-by-step process of instruction fetching, decoding, and execution.
* Basic interrupt handling mechanisms.
* Control signals for register manipulation and data transfer across a common bus.

The IDEGEN PROCESSOR project represents a comprehensive exploration of the core principles behind computer architecture and provides a detailed blueprint for a functional, albeit basic, central processing unit.
