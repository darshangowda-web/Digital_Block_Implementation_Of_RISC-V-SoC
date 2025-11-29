# Digital Block Implementation of RISC-V SoC

A simple RISC-V RV32I digital core implementation with UART, I2C, and TCM, completed through the full ASIC flow.

## Core Features
- RV32I 32-bit processor
- 3-stage pipeline
- Harvard architecture
- 32 registers + CSR
- IFU, IDU, EXU, LSU
- UART and I2C integration
- 64 KB TCM

## ASIC Flow
- RTL design
- Functional verification
- Synthesis (Genus)
- Floorplan
- Placement
- CTS
- Routing
- Timing (Tempus)
- Physical verification

## Results
- Power: ~24.64 mW
- Area: ~6.99 mm²
- Fully routed and timing-clean

## Repo Structure
rtl/ | synthesis/ | floorplan/ | placement/ | cts/ | routing/ | results/ | docs/

## Run
genus -files synthesis.tcl  
innovus -files pnr_flow.tcl  
tempus -files timing.tcl

## Contact
Darshan Mune Gowda  
darshangowda.academia@gmail.com
