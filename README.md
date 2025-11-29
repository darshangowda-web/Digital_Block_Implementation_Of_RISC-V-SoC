# How to Read and Understand the "Digital Block Implementation of RISC-V SoC" Report

This guide helps you easily navigate the RISC-V SoC report and understand what technical details you’ll find in each chapter.  
Think of this as a simple, interactive walk-through so you know exactly where to look without getting lost.

---

## 1. Start Here: Introduction (Pages 1–13)

This chapter sets the foundation and answers:
- What are integrated circuits and ASICs?
- Why RISC-V is important?
- What motivates designing a custom SoC?
- What the project aims to achieve.

If you’re new to ASIC or RISC-V, **read this first**.  
It gives context before diving into technical details.

---

## 2. Literature Survey (Page 14 onwards)

This chapter explains:
- What other researchers have done
- What architectures or techniques exist today
- Why this project is innovative

Read this if you want to understand the background research behind the design.

---

## 3. Core of the Report: Design & Methodology (Pages 27–43)

This is where the action happens.

Here you learn:
- How the SoC is architected  
- What ARAMB-180 SoC structure looks like  
- How the SCR1 core works  
- What the Digital Core contains  
- What registers, buses, and interfaces are used  
- Hardware and software requirements  

You’ll also see:
- Block diagrams  
- Register architecture  
- Memory maps  
- Pipelining diagrams  

This chapter is perfect if you want to understand **how the RISC-V SoC is built from scratch**.

---

## 4. Physical Design & Results (Pages 44–68)

This is the chapter for ASIC/EDA enthusiasts.

You’ll see each physical design stage:
- Synthesis  
- Floorplanning  
- Power mesh  
- Placement  
- Clock Tree Synthesis  
- Routing  
- Timing closure  

Each stage includes:
- Tool screenshots  
- Completion indicators  
- Reports (power, area, timing)  
- Visuals of the routed chip  

If you want to know how the RTL becomes an actual silicon-ready layout, **this is your chapter**.

---

## 5. Conclusion & Future Scope (Pages 69–70)

A short, crisp summary of:
- What the SoC achieved  
- Area and power results  
- Why the design is valid  
- What can be improved or added later  

Future scope includes:
- Adding more ISA extensions  
- Including analog blocks  
- Optimizing power further  
- Expanding into a full SoC product  

---

## Quick Guide: How to Read This Report Effectively

If you're in a hurry:

1. **Introduction** → understand the purpose  
2. **Design Implementation** → understand the architecture  
3. **Digital Core** → understand CPU details  
4. **Physical Design** → understand ASIC flow  
5. **Results** → see final chip performance  

This flow gives you the full picture fast.

---

## What You Will Learn Technically

By following the report, you’ll learn:
- How ASIC design flow works (RTL → GDS)  
- How to integrate a RISC-V core with peripherals  
- How pipelining and memory maps work  
- How synthesis and place-and-route are done  
- How to interpret area, power, and timing reports  

This makes the report valuable for:
- VLSI learners  
- Embedded engineers  
- SoC designers  
- Students building processor projects  

---

## Final Note

This report is detailed but very structured.  
Use this guide to navigate it chapter-by-chapter, and you’ll understand the entire RISC-V SoC design journey—from ISA theory to a routed, timing-clean digital chip.

