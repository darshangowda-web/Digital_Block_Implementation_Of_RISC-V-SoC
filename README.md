# 🔧 Digital Block Implementation of RISC-V SoC

This project implements the **Digital Core** of a RISC-V SoC using the **SCR1 (Syntacore) RV32I processor**, and integrates it with peripherals such as **UART** and **I2C**, along with tightly coupled memory.  
It follows the complete **ASIC design flow**, from RTL design to synthesis, place & route, timing analysis, and physical verification.  
The design and results are based on the RISC-V SoC report included in this repository.

---

## 📘 **Project Overview**

This SoC design is based on the **RISC-V RV32I Instruction Set Architecture**, using a **3-stage pipeline** and **load-store architecture**.  
The implementation focuses on:

- Digital Core of the processor  
- Integration of peripherals (UART, I2C)  
- ASIC flow with Cadence EDA tools  
- Power, area, timing, and layout analysis  
- Final routed and verified GDS-level output  

The design is optimized for **low power**, **scalability**, and **embedded system applications**.

---

## 🧩 **Features Implemented**

### 🔹 **RISC-V Digital Core**
- RV32I Base Instruction Set  
- 3-stage pipelined architecture  
- Harvard architecture (separate instruction/data buses)  
- 32 × 32-bit general-purpose registers (x0–x31)  
- Control and Status Registers (CSR)  
- Load/Store Unit (LSU)  
- Instruction Fetch & Decode Units (IFU, IDU)  
- Execution Unit with Integer ALU (EXU)  
- 32-bit AXI4/AHB-Lite external memory interface  

### 🔹 **Peripherals Integrated**
- UART  
- I2C  

### 🔹 **Memory System**
- 64 KB Tightly Coupled Memory (TCM)  
- Configurable memory map  
- Little-endian memory architecture  

---

## 🛠️ **ASIC Flow Used**

As illustrated in the **ASIC Design Flow diagram on page 12** of the report :contentReference[oaicite:1]{index=1}, the following steps were executed:

1. **RTL Design** (Verilog)
2. **Functional Verification**
3. **Logic Synthesis** — Cadence Genus  
4. **Floorplanning**  
5. **Power Mesh / Power Planning**
6. **Placement**
7. **Clock Tree Synthesis (CTS)**
8. **Routing**
9. **Timing Analysis** — Cadence Tempus  
10. **Physical Verification**
11. **Tape-out-ready GDS**

Each stage includes screenshots and logs (pages 44–68).

---

## 📊 **Results Summary**

Captured from **Chapter 4: Physical Design Verification & Results** (pages 55–68):

### ✔️ **Power Consumption**
- **~24.64 mW** total power  
  (as reported in synthesis power analysis)

### ✔️ **Area**
- Total chip area: **~6.99 mm²**

### ✔️ **Routing**
- Fully routed design (Figures 4.16–4.29 show routing results)

### ✔️ **CTS**
- Balanced clock distribution achieved  
  (Figures 4.26 & 4.27)

This confirms the design meets timing, power, and area constraints for ASIC readiness.

---

## 🧠 **System Architecture**

### 📌 **SCR1 Processor (Syntacore)**  
Key features (from pages 20–21):

- 32-bit RISC-V MCU core  
- RV32I base ISA  
- Hardware multiply/divide support  
- Customization flexibility  
- Low-power optimized  
- Configurable memory architecture  
- Interrupt support & timers  

### 📌 **Digital Core Block Diagram**  
Shown in report **Figure 3.2 (Page 22)**.

### 📌 **ARAMB-180 SoC Overview**  
Includes Digital Core, Memory, and Analog blocks  
— diagram shown in **Figure 3.1 (Page 20)**.

---

## 📁 **Repository Contents**

📦 RISC-V-SoC
┣ 📜 rtl/ → Verilog RTL code
┣ 📜 synthesis/ → Genus synthesis reports
┣ 📜 floorplan/ → Floorplanning snapshots
┣ 📜 placement/ → Placement logs & images
┣ 📜 cts/ → Clock tree synthesis data
┣ 📜 routing/ → Routed design (DEF/GDS)
┣ 📜 results/ → Area, power, timing reports
┣ 📜 docs/ → RISC-V SoC Report (PDF)
┗ 📜 README.md

markdown
Copy code

---

## 🚀 **How to Run / Reproduce**

### **1. Requirements**
- Linux (Ubuntu recommended)  
- Cadence Tool Suite:
  - **Genus** (Synthesis)
  - **Innovus** (P&R)
  - **Tempus** (Timing)
- Verilog RTL files (included)

### **2. Run Synthesis**
```bash
genus -files synthesis.tcl
3. Run Place & Route
bash
Copy code
innovus -files pnr_flow.tcl
4. Timing Analysis
bash
Copy code
tempus -files timing.tcl
🧪 Testing & Verification
RTL simulation using testbenches

Functional verification for basic RV32I instructions

Memory access tests (load/store)

UART & I2C read/write tests

🎯 Objectives Achieved
As stated in Section 1.6 (Page 18):

✔️ Gained complete ASIC flow understanding

✔️ Implemented RV32I Digital Core

✔️ Integrated peripherals into SoC

✔️ Obtained synthesis, placement, routing, and performance reports

✔️ Delivered nearly tape-out-ready SoC digital design

📌 Future Scope
From Section 5.2 (Page 70):

Add more RISC-V instruction extensions

Integrate analog blocks

Improve power optimization

Fabricate and test silicon prototype

Add interrupt controller, SPI, and DMA

Explore FPGA deployment

✨ Credits
This design is based on the academic project report:
“Digital Block Implementation of RISC-V SoC”
by Darshan Mune Gowda 
RISC-V_SoC_Report

.

📬 Contact
Darshan Mune Gowda
📧 darshangowda.academia@gmail.com
🌐 GitHub: https://github.com/darshangowda-web
