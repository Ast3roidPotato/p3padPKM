---
excalidraw-default-mode: view
---

```toc

```

^TOC

<[[|previous]] | [[|next]]>

# Lesson Set 1

## Lesson 1-3

Machine Instructions are encoded designations of operations to perform.

Formatted instructions are Comp Arch Dependent


Common fields:
- Opcode (Operation Code)
- Operands - Source and/or destination operands of the instruction
- Mode (optional) - Addressing mode of the operation
- Conditional (optional)

ISA defines:
- Fields of instruction
- Bits per field
-  opcodes 
- addressing modes

#### Addressing mode:
- Effective address - where is the actual location of the operand
- May be determined by the opcode of by filed within instruction


Addressing Modes More:

Common Addressing Modes:
- Implicit
	- Effective address (or value) is implied by the opcode exe: PUSHPC
- Immediate
	- Value is provided directly within operand field
- Register addressing modes
	- The effective address is one of the CPU's general purpose registers
- Direct (Absolute) addressing mode
	- Effective address is provided directly in the instruction
		- Value is static and fixed in machine code, can not be modified by the program at runtime.
- Register indirect (indexed) addressing
	- Effective address is stored in a CPU register
	- Supports the full main memory address range with only a few bits needed for the operand field.
	- This means that the address space size is still only the register size. 
- Relative addressing
	- Effect address is sum of base address and offset.

From Slides:
Machine instructions are encoded micro-operations
They are decoded to produce inputs to datapath for operation
Instruction set architecture defines all possible operations and format of instructions
Opcode (Operation Code) —operation that the instruction should perform
• Operands — source and/or destination operands of the instruction
• Mode (optional) — Addressing mode of the operation
• Condition (optional) — Specific condition for executing the instruction
Addressing mode specifies how effective address is determined from operand field
• Effective address — actual location of the operand (main memory or CPU register)
Examples of addressing modes:
- Implicit — effective address (or value) is implied by opcode
- Immediate — value is provided directly within operand field
- Register addressing — effective address is one of CPU's general purpose registers
- Direct (Absolute) addressing — effective address is provided directly in instruction
- Register indirect (Indexed) addressing — effective address is stored in a CPU register
Relative addressing effective address is sum of base address and offset

## Lesson 1-4

### Memory 

Memory storage is organized in to different blocks
- Program mem
- Data memory 
- CPU Register Peripheral registers 
- Non-volatile data memory

Program memory is in non-volatile memory

ROM  = read only memory - data is set at production
PROM = program read only memory - can be programmed one time by the user
EPROM = erasable read only memory - erasing requires exposure to UV light
EEPROM = electrically erasable read only memory - in the field firmware updates

Data memory = RAM - readable and writeable at run-time

Typically **volatile memory** data is not retained when power is removed.

DRAM
- Cheaper and more dense than SRAM
- Slower than SRAM
SRAM
- Rlly faast
### CPU Registers
Types:
- General Purpose - ideal for frequently used or ephemeral data
- Special registers - vary by architecture
	- Status 
	- Stack pointer
	- program counter
#### Status register
VERY IMPORTANT
It stores status flags from previous ALU operations
- each flag only updated by certain instructions 
- may be read to determine outcome of previous operation
- may be used for conditional instructions
- register may include other status or configuration bits
Common flags:
- zero
- negative
- carry
- overflow
#### Peripheral registers
> also known as special function registers

connect directly to inputs and outputs of peripheral subsystems
Common ones:
- configuration registers
- status from peripheral circuit
- Data
- Interrupt control - enable and configure peripheral interrupts

### Peripherals

Each peripheral is a digital or mixed-signal circuit
Examples:
- Timers 
- general purpose I/O ports 
- ADCs
- Comparators
- Compare/capture modules
- Communication modules.

Each one normally has a:
- configuration register
- Data register
- Status register

#### Peripheral registers
bits may be defined as:
- Read/Write
- Read-only
- Write-only (uncommon)
- Unused/reserved


### Non-Volatile Data Memory

Some microcontrollers include, typically byte-addressable EEPROM in addition to ram

used for:
- Storage of updateable look-up tables
- Storage of initialized variables which retain values across power cycles
- Storage of error/log data for troubleshooting or recovery in case of failure
Memory-mapping is commonly used to provide a virtual continuous address space for multiple types of memory within the system
Peripheral registers are typically memory-mapped within the same address as data memory.
- For Harvard architectures, this is known as modified Harvard architecture
	- very common in modern systems.
	- Used to have the same instructions work on both memory banks.
