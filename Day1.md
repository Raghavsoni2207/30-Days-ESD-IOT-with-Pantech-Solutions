# Day 1: Introduction to Embedded Design and IoT

## Overview
- **Summary:** Introduction to the basics of embedded systems and IoT, including their definitions, classifications, and applications.

## Key Concepts
### What is an Embedded System?
An embedded system is a combination of both software and hardware, sometimes including mechanical parts, designed to perform a specific task. These systems are often optimized for performance, efficiency, and reliability. 
- **Examples:** Printer, washing machine, smartwatch, etc.

### Classification of Embedded Systems
1. **Real-Time Embedded Systems**
   - **Hard Real-Time:** Systems that must adhere strictly to timing constraints. Missing a deadline could lead to catastrophic failures.
   - **Soft Real-Time:** Systems where timing constraints are important but not critical. Missing deadlines may degrade performance but not lead to system failure.
2. **Network Embedded Systems:** Systems designed to operate over a network, often for data collection and processing.
3. **Mobile Embedded Systems:** Systems designed for portability and battery efficiency, commonly found in mobile devices.

### Types of Processors and Controllers for Embedded System Design
- **Microprocessors/Microcontrollers:** (e.g., 8085, 8086, 8051)
- **DSP/DSC:** Digital Signal Processors/Controllers for signal processing tasks.
- **CPLD/FPGA:** Complex Programmable Logic Devices/Field Programmable Gate Arrays for customizable hardware solutions.
- **ASIC:** Application-Specific Integrated Circuits for highly optimized, single-purpose designs.
- **SOC:** System on Chip integrates all components of a computer or other electronic system into a single chip.

### Languages for Embedded System Design
- **ASM:** Assembly language for low-level hardware interaction.
- **C:** Popular high-level language for embedded systems.
- **Mixed C/ASM:** Combining C and assembly for performance-critical sections.
- **Python:** Increasingly used for higher-level control and scripting.
- **HDL:** Hardware Description Languages (e.g., VHDL, Verilog) for FPGA and ASIC designs.
- **Graphical / Visual:** Tools like LabVIEW for visual programming.

### Peripherals in Microcontroller/DSP/FPGA
- **GPIO:** General-Purpose Input/Output pins.
- **UART:** Universal Asynchronous Receiver-Transmitter.
- **SPI:** Serial Peripheral Interface.
- **I2C:** Inter-Integrated Circuit.
- **ADC/DAC:** Analog to Digital Converter / Digital to Analog Converter.
- **MEMORY:** Types include SDRAM, FLASH.
- **CAN:** Controller Area Network.
- **LIN:** Local Interconnect Network.
- **ETHERNET:** Network communication protocol.
- **RTC:** Real-Time Clock.
- **USB:** Universal Serial Bus.
- **HDMI:** High-Definition Multimedia Interface.
- **VGA:** Video Graphics Array.
- **INTERRUPT:** Mechanism to handle events.
- **PWM:** Pulse Width Modulation.
- **DMA:** Direct Memory Access.
- **TIMERS:** Timing and counting functions.

### Applications of Embedded System Design
- **Aerospace**
- **Automotive Infotainment**
- **Smart Home**
- **Industry Automation**
- **Robotics**
- **Communication**
- **Audio, Video, and Medical Imaging**

### What is Internet of Things (IoT)?
The Internet of Things (IoT) refers to a network of physical devices embedded with sensors, software, and other technologies to connect and exchange data with other devices and systems over the internet.

### IoT vs IIoT
- **IoT (Internet of Things):** Focuses on devices and applications for consumer and commercial use, such as smart home devices.
- **IIoT (Industrial Internet of Things):** Focuses on industrial applications, improving efficiency, safety, and operations in sectors like manufacturing and energy.
- **Common Aspects:** Data management, connectivity, data security, and secure cloud services.

### Challenges of IoT
- **Complex System:** Requires integration of various technologies.
- **No Single Vendor Solution:** Multiple vendors often provide different parts of the solution.
- **Multiple Expertise Required:** Involves firmware, communication, web/IT, data science, and security.
- **Lack of Consolidation on Industry Standards:** No universally accepted standards.

### List of Cloud Providers
- **Think Speak**
- **AWS**
- **Microsoft Azure**
- **Google Cloud**
- **Oracle**

### How to Convert an Idea to a Prototype?
1. **Choose the Right Processor**
2. **Choose the Development Tool**
3. **Determine if the Application Needs an RTOS or a Simple Program**
4. **Select Your Packages and Product Tools**
5. **Schematic Design (considering DFT and DFM)**
6. **Layout Design**
7. **Assembling, Debugging, and Testing**
8. **Enclosure Design**
9. **Plan for Certification if Required**
10. **Design of Test Jig for Mass Production**

### Embedded Development Life Cycle
![Embedded Development Life Cycle](../images/development_lifecycle.png)
- This image shows the various stages of the embedded development life cycle.
