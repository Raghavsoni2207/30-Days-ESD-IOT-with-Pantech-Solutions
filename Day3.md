# Day 3: Basic Elements of Embedded Systems, IDE, Software Development Flow, and Communication Protocols

## Basic Elements of Embedded System
- **User Interface**: Keypad, keyboard, mouse, touch panel.
- **Input Variables**: Sensors (analog/digital).
- **Output Variables**: Display devices, motors, relays.
- **Link to Other Systems**: Communication interfaces like UART, I2C, SPI, RS232, WIFI, Bluetooth.
- **Embedded Computer**: Combination of hardware and software.

## What is IDE (Integrated Development Environment)?
- **Components of an IDE**:
  - Compiler, Assembler, Linker, Loader
  - Editor window, Console window, Project window
  - Debug/Release modes
  - Memory window, Register window
  - Breakpoints, Watchpoints
  - Debugger
  - Programming options

## Software Development Flow

## Linker Description File
### Sections and Locations
| Section | Location | Why |
|---------|----------|-----|
| .text   | FLASH    | Must exist after reset |
| .cinit  | FLASH    | Must exist after reset |
| .bss    | Internal | Must be in RAM memory |
| .stack  | Internal | Must be in RAM memory |

## Compiler Section Names
| Section Name | Description | Memory Type |
|--------------|-------------|-------------|
| .text        | Code        | Initialized  |
| .switch      | Tables for switch instructions | Initialized |
| .const       | Global and static string literals | Initialized |
| .cinit       | Initial values for global/static variables | Initialized |
| .pinit       | Initial values for C++ constructors | Initialized |
| .bss         | Global and static variables | Uninitialized |
| .far         | Aggregates (arrays & structures) | Uninitialized |
| .stack       | Stack (local variables) | Uninitialized |
| .sysmem      | Memory for malloc functions (heap) | Uninitialized |
| .cio         | Buffer for stdio functions | Uninitialized |

## Structure of Linker File
- **Linker.cmd**:
  - Hardware memory description (name, location, length)
  - Software sections (name, memory area to link to)
- **Object File to Executable Flow**:
  - `.obj -> Linker -> .out`
  - `.map` file for memory mapping

## Sample Linker Command File
MEMORY
{
FLASH (RX) : ORIGIN = 0x08000000, LENGTH = 256K
RAM (RWX) : ORIGIN = 0x20000000, LENGTH = 64K
}

SECTIONS
{
.text : {
*(.text)
} > FLASH

.bss : {
*(.bss)
} > RAM

.data : {
*(.data)
} > RAM
}

## Programming Techniques
- **ISP (In-System Programming)**
- **ICSP (In-Circuit Serial Programming)**
- **IAP (In-Application Programming)**
- **JTAG (Joint Test Action Group)**

## Common Embedded Peripherals
- GPIO Controllers
- Timers
- PWM Controllers
- DACs (Digital to Analog Converters)
- ADCs (Analog to Digital Converters)
- Serial communication controllers for UART, SPI, I2C, and Ethernet
- Memory (SRAM, DRAM, Flash, EEPROM)
- Interrupt controllers
- Direct memory access controllers (DMA)
- CAN (Controller Area Network)
- LIN (Local Interconnect Network)
- JTAG
- USB
- Video Ports

## Memories
- **Primary Memory**: SRAM, DRAM
- **Secondary Memory**: NVRAM, Flash, EEPROM, PROM, Masked ROM

## What is UART?
- **Universal Asynchronous Receiver and Transmitter**
  - Serial port, COM port, RS232, RS485
  - Very common and simple
  - Useful for communication to microcontrollers, computers, other FPGAs
  - **Pins**: TXD, RXD, GND
  - **Range**: 3 meters

## Introduction to SPI
- **Serial Peripheral Interface**
  - Full-duplex, Serial communication protocol
  - Synchronous communication protocol
  - Four-wire communication protocol
  - Single master, multiple slaves
  - Widely used for short-distance communication, primarily in embedded systems
  - Recommended within the circuit board (1-meter range)

## I2C
- **Inter-Integrated Circuit**
  - Combines the best features of SPI and UART
  - Allows multiple slaves to connect to a single master
  - Two-wire communication (SDA and SCL)
