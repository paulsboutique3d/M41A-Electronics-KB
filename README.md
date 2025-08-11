# Wiring Harness Documentation

A comprehensive overview of the wire looms, their routing direction, and exact lengths used in this project.

---

## Wire looms

Each loom groups related circuits together into a single harness for ease of installation and maintenance.

- **Loom A (Thompson Trigger)**  
  - Loom from Manin board to Thompson trigger and Fire select potentiometer 
- **Loom B (Speakers)**  
   - Loom from main noard to Spaeaker box 
- **Loom C (LED Thompson)**  
  - Loom from main board to thompson barrel LED
- **Loom D (LED Remington)**  
  - Loom from main board to Remington LED
- **Loom E (Remington Trigger)**  
  - Loom from main board to Remington Trigger
- **Loom F ( Battery Loom)**
---

## Wire Direction

All wires are labeled and routed according to the following conventions:

- **Arrow markers** on the insulation indicate the primary current direction (→ from source to load).  
- Loom‑level directionality:
  - **Loom A** Thompson Trigger → Main Board  ➔ trigger * Positive left on main board  
  - **Loom B** → Speakers ➔ Main board ➔ speaker box  * Positive outer left and outer right  on main board
  - **Loom C** ↔ LED Thompson ↔ Main board - barrel LED  *   Positive is at the bottom on main board
  - **Loom D** LED Remington → Main Board  ➔ remington LED * Positive left at the bottom on main board  
  - **Loom E** → Remington Trigger ➔ Main board ➔ REmington Trigger  * Signal at the top, Ground middle, Positve at the bottom 
  - **Loom F** ↔ Battery ↔ Main board - battery lead  *   one way connector


---
<img width="472" height="655" alt="467487896-b9f9e950-c573-45ee-b419-ec67ae8e8052" src="https://github.com/user-attachments/assets/2987d446-6e37-44d9-b1e0-b7439fcf34ae" />

## Wire lengths

Wire lengths have been cut to ±2 mm tolerance. All lengths are measured end‑to‑end, excluding connector pin depth.

| Loom  | no wires| From             | To                  | Length (mm) |
|-------|---------|------------------|---------------------|-------------|
| A     | 4       | Trigger Board    | main board          | 150         |
| B     | 4       | Speaker Box      | Main Board          | 150         |
| C     | 3       | Thompson LED     | Main Board          | 330         |
| D     | 3       | Remington LED    | Main Board          | 300         |
| E     | 3       | Remington        | Main Board          | 100         |
| F     | 2       | Battery          | Main Board          | 50          |
---


