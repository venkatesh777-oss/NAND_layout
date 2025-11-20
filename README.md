**2-Input CMOS NAND Gate – RTL to Layout using Yosys, Magic VLSI & NGSpice**

This repository contains the complete VLSI design flow for a 2-input CMOS NAND gate, covering RTL design, logic synthesis, custom layout, SPICE extraction, and transistor-level simulation.
The entire project is implemented using open-source EDA tools.

📘 Project Overview

This project demonstrates the following steps in a standard VLSI flow:

✔ Writing Verilog RTL for a 2-input NAND gate

✔ Synthesizing RTL to a gate-level netlist using Yosys

✔ Designing the full-custom CMOS layout using Magic VLSI

✔ Performing DRC, LVS, and parasitic extraction

✔ Running transistor-level simulation using NGSpice

✔ Validating correct NAND logic behavior

📁 Repository Structure
├── src/
│   ├── nand_gate.v              # RTL Verilog code
│
├── synth/
│   ├── nand_gate_synth.v        # Gate-level synthesized netlist
│
├── layout/
│   ├── nand_gate.mag            # Magic layout file
│   ├── nand_gate.spice          # Extracted SPICE netlist
│
├── spice/
│   ├── nand_gate.spice         # SPICE simulation file
│
└── README.md

 1. RTL Design (Verilog)

The NAND gate is implemented using a simple gate level Verilog description defining the logical function:

nand(out,a,b);

 2. Synthesis (Gate-Level)

The Verilog RTL is synthesized into a gate-level netlist, showing how the NAND logic is mapped into standard cells.
This netlist is stored in the synth/ directory.

🏗 3. Custom Layout (Magic VLSI)

The NAND gate is implemented at the transistor level with:

PMOS transistors in parallel (pull-up network)

NMOS transistors in series (pull-down network)

The layout includes:

Active diffusion regions

Polysilicon gates

Metal interconnects

Contact/via placements

n-well and p-well regions

DRC and LVS checks ensure the physical layout matches the intended logic.

 4. SPICE Extraction & Simulation

The layout is extracted to a SPICE netlist, capturing:

Transistor dimensions

Node connectivity

Parasitic capacitances

Simulation is done using NGSpice to verify NAND operation, analyzing:

Input transitions

Output voltage response

Rise/fall times

Propagation delays

Visual Outputs:

images/
  nand_ngspice_simulation.png

📈 Key Learning Outcomes

Understanding CMOS NAND transistor implementation

Building the connection between RTL, gate-level, and physical layout

Performing extraction and analyzing realistic electrical behavior

Applying open-source VLSI tools in a practical design flow

Strengthening fundamentals in digital IC design and custom layout

Tools Used

Yosys – RTL synthesis

Magic VLSI – Custom layout, DRC & LVS

NGSpice – Transistor-level simulation

Ubuntu Linux – Development and design environment

AUTHOR

VENKATESH DAMERA

VLSI & EMBEDDED ENTHUSIAST
