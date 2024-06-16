# Day 2: Microprocessor, Microcontroller, DSP, FPGA, and Hardware Design

## Microprocessor
- A general-purpose system that is used to execute a wide range of tasks and applications.
- Examples: Intel i7, ARM Cortex-A.

## Microcontroller
- A compact integrated circuit designed to govern a specific operation in an embedded system.
- Examples: AVR, PIC, ARM Cortex-M.

## DSP (Digital Signal Processor)
- Digital Signal Processor is mathematics on chip.
- DSPs usually run applications with hard real-time constraints.
- DSPs usually process infinite continuous data streams.
- **Key Features:**
  - MAC (Multiply-Accumulate) capability.
  - Designed for efficient mathematical manipulation of digital signals.

## Harvard and von-Neumann Architecture
### Harvard Architecture
- Separate memory and buses for program and data.
- Allows simultaneous access to program and data.

### von-Neumann Architecture
- Shared memory and bus for program and data.
- Sequential access to program and data, leading to potential bottlenecks.

## CPLD vs FPGA
### CPLD (Complex Programmable Logic Device)
- More predictable timing.
- Limited logic resources.
- Suitable for simpler, less complex designs.

### FPGA (Field Programmable Gate Array)
- Larger logic capacity.
- Suitable for complex and high-speed designs.
- **FPGA Technologies:**
  - **SRAM:** Reprogrammable but volatile.
  - **Flash:** Reprogrammable and non-volatile.
  - **Antifuse:** Non-volatile, one-time programmable.

## DSP vs FPGA
- **DSP:** Specialized for processing digital signals.
- **FPGA:** Highly versatile and can implement custom hardware circuits including DSP functions.

## Multicore Processor (SoC)
- 2 or more independent processors in 1 package.
### Symmetric Multiprocessing
- Multiple identical processors.
- Common shared memory.
- One operating system.

### Asymmetric Multiprocessing
- Different processors with different instruction sets.
- Different operating systems.
- Possible without shared memory.

## How FPGA is Different from ASICs
- **FPGA:** Reprogrammable, good for prototyping and low-volume production.
- **ASIC (Application-Specific Integrated Circuit):** Custom-designed for a specific task, optimized for high-volume production.

## Comparison
![Comparison](/Images/comperison.png)

## Selection of Package
- **DIP (Dual In-line Package):** Suitable for prototyping and manual soldering.
- **QFP (Quad Flat Package):** Requires a soldering station, used in compact designs.
- **SOIC (Small Outline Integrated Circuit):** Compact and suitable for surface mount.
- **PLCC (Plastic Leaded Chip Carrier):** Used for both surface mount and socket mount.
- **BGA (Ball Grid Array):** Requires reflow oven for soldering, used for high-density applications.

## Processor Selection Criteria
- **Development Tools:** Availability and quality of development tools.
- **Number of I/O:** Required number of input/output pins.
- **Performance:** Processing speed and capability.
- **Cost:** Budget considerations.
- **Operating System:** Compatibility with required OS.
- **Hardware Tools:** Availability of debugging and development hardware.
- **Peripherals:** Built-in peripherals like ADC, DAC, UART, etc.
- **Power Consumption:** Efficiency and power requirements.
- **Supplier Reputation:** Reliability and support from the supplier.

## Hardware Design Flow
![Hardware Design Flow](/Images/hardwareDesignFlow.png)
### Schematic Design
- Design of circuit diagram.
### Layout Design
- Placement of components and routing of connections.
### Assembly and Testing
- Soldering components and verifying functionality.

## Schematic Design Considerations
- **Power Supply Design:** Use tools like Webench Designer by TI.
- **Ground Splitting:** For designs with analog parts (High-speed ADC and DAC).
- **Decoupling Capacitors:** Proper calculation for VCC.
- **ESD Protection:** Use diodes for ESD-sensitive ICs.

## Layout Design Considerations
- **Footprints:** Ensure correct footprints for components.
- **Component Placement:** Place as per schematic and design requirements.
- **Decoupling Capacitors:** Place close to VCC pins.
- **Length Matching:** For high-speed memory interfaces.
- **Routing:** Avoid right-angle traces, use smooth curves.
- **High-speed Memory Placement:** Close to the processor to reduce latency.

## Software Design Flow
![Software Design Flow](/Images/SoftwareDesignFlow.png)

