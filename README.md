# RISC-V-Week-2
Learnings and Lab results from RISC-V Chip Tapeout Workshop 

# **System-on-Chip (SoC)**

## **What is a System-on-Chip (SoC)?**

A **System-on-Chip (SoC)** is an integrated circuit (IC) that combines **all major components of a computer or electronic system** into a single chip.  
Unlike traditional systems where the CPU, memory, and peripherals are on separate chips connected via a motherboard, an SoC integrates everything on one silicon die.

> **Definition:**  
> A System-on-Chip (SoC) integrates a processor, memory, input/output ports, communication interfaces, and other peripherals into a single chip to perform a complete set of functions.

**Used in:** Smartphones, embedded devices, IoT systems, automotive controllers, etc.

---

## **Components of a Typical SoC**

A typical SoC consists of the following main components:

### 1. **CPU (Processor Core)**
- The **brain** of the SoC — executes program instructions.  
- Based on architectures like **ARM**, **RISC-V**, or **x86**.  
- Can be single-core or multi-core for performance and efficiency.

### 2. **Memory**
- **On-chip memory** (e.g., SRAM, ROM) for fast data access.  
- **External memory interfaces** (e.g., DDR controller) for large storage.  
- Stores both **program code** and **data**.

### 3. **Peripherals (I/O Interfaces and Controllers)**
- Manage communication and control with external devices:  
  - UART, SPI, I2C (communication)  
  - GPIO (general-purpose I/O)  
  - Timers, ADC/DAC, interrupt controllers, etc.  
- Typically accessed via **memory-mapped registers**.

### 4. **Interconnect / Bus System**
- Provides **data communication** between CPU, memory, and peripherals.  
- Common types: **AMBA (AXI, AHB, APB)**, **Wishbone**, etc.  
- Functions like an internal data highway connecting all modules.

## **Why BabySoC is a Simplified Model for Learning SoC Concepts**

**BabySoC** is a minimal educational SoC design — created to help students learn **how SoCs are structured and built** without industrial complexity.

### **Simplifications**
- Single lightweight CPU (like **PicoRV32** or a basic **RISC-V** core).  
- Few peripherals (UART, GPIO).  
- Simple memory subsystem (small SRAM, no cache).  
- Basic interconnect (e.g., **Wishbone** or **AXI-Lite**).

### **Learning Benefits**
- Easy to understand **data flow and communication** inside an SoC.  
- Enables practice with **RTL design**, **simulation**, and **synthesis**.  
- Compatible with **open-source EDA tools** (Yosys, OpenLane).  
- Acts as a **bridge** between theory and practical chip design.

---

## **Role of Functional Modelling Before RTL and Physical Design**

Functional modelling is an **early SoC design stage** where system behavior is verified **before** writing RTL code.

### **Purpose**
- Validate the **architecture and logic flow**.  
- Ensure correct **CPU–memory–peripheral** interactions.  
- Detect and fix **conceptual design errors early**.

### **How it Works**
- Written in **high-level languages** (C, Python, or SystemC).  
- Focuses on **functionality**, not timing or circuit details.  
- Example: simulate CPU–memory data transfer before Verilog coding.

### **Benefits**
- Early detection of design flaws.  
- Reduces time and cost before synthesis/layout.  
- Provides a **reference model** for later RTL verification.

# Lab Component
## Pre-synthesis
![](/images/pre_synth_waveform.png)<sjd>
## Post-synthesis
![](/images/post_synth_waveform.png)
## Conclusion
![](/images/pre_synth_waveform.png)
![](/images/post_synth_waveform.png)
From comparing both the waveforms, we can see no disimilarities implying that synthesis was successful in genearating a proper gate level design. 
