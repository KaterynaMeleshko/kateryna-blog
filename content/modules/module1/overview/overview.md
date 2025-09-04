---
title: "Overview"
summary: Here i will post my overview on this module
date: 2025-08-15
weight: 1
type: page
draft: false
_build:
  list: never 
---

# PC Components

## central processing unit

CPU - central processing unit, executes machine instructions of programs, manages memory and devices through controllers and buses

CPU cycle: fetch → decode → execute → write-back, works based on a clock generator

--- 

### how does the CPU work?

it fetches instructions from memory by clock cycles, decodes them, executes them through arithmetic-logic units (ALU/FPU) and stores the result back into registers or memory, while constantly managing the operation of other devices via controllers and buses.

---

### what physical components does it consist of?

#### - lid

the CPU components are built so that on the very top there is a metal lid which distributes heat evenly and transfers it to the heatsink or cooler. since the processor heats up during operation, this lid is needed to avoid overheating and to protect the die from mechanical damage. usually this lid is made of copper with a nickel-plated surface so it does not oxidize.

#### - thermal paste

below the lid there is a layer of thermal paste. thermal paste is used to ensure good thermal conductivity from the die to the lid, because without it the lid may not fit tightly enough to the die. the paste fills all gaps and transfers heat to the lid across the entire surface of the die. thermal paste can be metallic or ceramic. in both cases the base is usually silicone or synthetic polymer oil because it does not evaporate and dries quickly. fillers vary:

for ceramic ones boron nitride, aluminum oxide, aluminum nitride are often used (they are electrical insulators and do not conduct current, which makes them safe when in contact with electronic components).

in metallic fillers oxides of metals like zinc and aluminum may be used (cheap fillers, improve conductivity compared to pure oil, but worse than pure metals). in more expensive pastes silver or copper are used (silver conducts heat best, ~430 W/m·K vs ~400 for copper). in rare cases diamond dust is used (up to 2000 W/m·K).

#### - die

definitions:

wafer - thin round plate of pure silicon on which hundreds of processor or memory circuits are made

dies - when circuits are patterned on the wafer, it is cut into dies, each block is a separate die containing all transistors and microcircuits

chip - after the die is ready it is packaged into a protective case, contacts are soldered, heatspreader is attached

the CPU die is a thin plate of silicon (a few hundred microns), where transistors and multilayer metal interconnections separated by dielectrics are formed by photolithography. thin top layers are used for local connections, thick bottom ones for power and clock signals.

silicon (Si) - a chemical element that is a semiconductor, depending on doping can act as conductor or insulator.

doping - adding a very small amount of another element, about one atom per million. impurities create extra electrons or holes. as a result, the main element (silicon, 4 outer electrons) can become:

n-type (electron conductor) impurity of phosphorus or other elements with 5 electrons on the outer shell. one extra electron is free → moves easily → creates free electrons = conductivity.

p-type (hole conductor) impurity of boron/aluminum or any element with 3 outer electrons. when they replace a silicon atom (with 4), a hole appears — a place where an electron can jump. these holes move through the crystal and also create conductivity.

insulator - pure silicon without impurities, electrons remain fixed.

modern processors are manufactured using CMOS technology, which combines n-type and p-type transistors in each logic circuit. this allows building basic logic elements with minimal power consumption: current flows only during switching, not in static state. controlling current through the transistor channel (gate opens or closes the path for electrons) allows forming logic elements such as AND, OR, NOT.

how is the die made?

first silicon is extracted. quartz sand is melted, then purified, a silicon crystal is grown. the crystal is grown in cylindrical form and then sliced into thin wafers. then dielectric, metal and conductor layers are deposited. a photosensitive layer is applied, exposed to ultraviolet light forming the pattern of future transistors, then developed so the needed structure remains. doping is done by ion implantation to change conductivity of areas. these steps are repeated many times, forming transistors and connections. then the wafer is cut into dies, tested and soldered into the package.

#### - substrate

after the die is manufactured it is soldered onto a green substrate which is a multilayer high-precision PCB. this acts as an adapter between the chip and the contacts that fit into the motherboard.

---

### what blocks does the CPU have?

(CPU cycle: fetch → decode → execute → write-back)

- frontend. loads and decodes instructions (former CU - control unit)

- ALU. integer calculations

- FPU or vector unit. works with floating point numbers and vectors

- register file. the fastest memory unit in the PC, very small, stores only numbers for addition and memory addresses. data is loaded here and then goes to ALU/FPU

- store units. access to RAM or cache

- branch predictor. predicts where the program will go at conditional branches (if, loops, comparisons). example: if (x>0) { … } else { … }. CPU tries to guess which branch will execute to preload instructions in advance and avoid stalling.

- cache memory. L1 is the smallest (up to 64KB) and fastest, located inside the core. L2 also inside the core, larger and slightly slower (up to 1MB). L3 shared across all cores. what is stored in cache: copies of frequently used data and instructions from RAM.

- integrated GPU. not required in all processors but used almost always in modern computers. outputs image to the screen. includes shader blocks (mini-ALU optimized for processing pixels/vertices/colors), media blocks, display controller (manages HDMI and screen output).

- controllers:

IMC - integrated memory controller. communicates directly with RAM.

PCIe controller manages PCIe express lanes (connection CPU ↔ GPU, SSD, network cards).

DMI/UPI connection with chipset and other dies.

PMU monitors power consumption.

Clock&PLL generates clock signals and creates stable frequency.

- system agent: part of the processor that unites non-compute blocks — memory controller (IMC), PCIe controller, graphics (iGPU), L3 cache and chipset interfaces. its job is to manage interaction of these blocks and distribute data between cores, memory, graphics and peripherals.

all these blocks are made of transistors. a transistor is a tiny element that opens or closes current flow. the die itself is multilayered: bottom silicon with transistors, then many layers of metal tracks connecting them, together forming functional blocks of the CPU. the die refers to all these layers as one whole.

---

CPU architectures may be based on either CISC (complex instruction set computer) or RISC (reduced instruction set computer), on which architectures like these are built:

x86 - capable of executing complex commands since they have powerful processors and high performance. used in PCs, laptops, servers.

ARM - minimalist instruction set, commands execute one task step by step. efficient in power consumption. used in smartphones, tablets, MacBooks.

