---
title: "Module 1"
summary: Hardware
date: 2025-08-15
weight: 1
type: page
draft: false
---

# Overview PC Components

## central processing unit

CPU - central processing unit, executes machine instructions of programs, manages memory and devices through controllers and buses

CPU cycle: fetch → decode → execute → write-back, works based on a clock generator

--- 

### how does the CPU work?

it fetches instructions from memory by clock cycles, decodes them, executes them through arithmetic-logic units (ALU/FPU) and stores the result back into registers or memory, while constantly managing the operation of other devices via controllers and buses.

---

### what physical components does it consist of?

**- lid**

the CPU components are built so that on the very top there is a metal lid which distributes heat evenly and transfers it to the heatsink or cooler. since the processor heats up during operation, this lid is needed to avoid overheating and to protect the die from mechanical damage. usually this lid is made of copper with a nickel-plated surface so it does not oxidize.

**- thermal paste**

below the lid there is a layer of thermal paste. thermal paste is used to ensure good thermal conductivity from the die to the lid, because without it the lid may not fit tightly enough to the die. the paste fills all gaps and transfers heat to the lid across the entire surface of the die. thermal paste can be metallic or ceramic. in both cases the base is usually silicone or synthetic polymer oil because it does not evaporate and dries quickly. fillers vary:

for ceramic ones boron nitride, aluminum oxide, aluminum nitride are often used (they are electrical insulators and do not conduct current, which makes them safe when in contact with electronic components).

in metallic fillers oxides of metals like zinc and aluminum may be used (cheap fillers, improve conductivity compared to pure oil, but worse than pure metals). in more expensive pastes silver or copper are used (silver conducts heat best, ~430 W/m·K vs ~400 for copper). in rare cases diamond dust is used (up to 2000 W/m·K).

**- die**

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

**- substrate**

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

---


## Motherboard

a motherboard is the main printed circuit board of a computer, a multilayer structure made of fiberglass-reinforced epoxy with copper traces. in the layers of the board are routed: signal lines, power planes, GND planes. the board provides physical mounting of components and electrical connection between them.

---

### motherboard components:

**-CPU socket**

this is the connector where the CPU is installed.

consists of hundreds/thousands of contact pins or pads (LGA - contacts are in the socket as in intel, PGA - contacts in the form of pins on the CPU as in amd, BGA - CPU soldered onto the board as in laptops).

contacts are made of copper/gold-plated alloys for reliable connection and oxidation protection. the socket’s task is to carry hundreds of signals (power, data, addresses, clocking) between CPU and the board.

**-RAM slots**

long connectors with spring-loaded contacts made of copper alloy with coating (usually gold/nickel) for memory modules.

DIMM (dual inline memory module) - standard for desktop PCs.
SO-DIMM (small outline DIMM) - shortened version for laptops and mini-PCs.

each slot is connected to the memory controller inside the CPU.

**-chipset(PCH)**

this is effectively a separate die that manages communication between CPU, RAM, storage, and peripherals.

previously there were two chips:

northbridge - worked with RAM and GPU.
southbridge - worked with slower peripherals (USB, SATA, audio, network).

today northbridge functions are integrated directly into the CPU via direct media interface, and only the PCH (former southbridge) remains on the board.

**-PCIe slots**

connectors for expansion cards: graphics cards, sound cards, network cards, capture cards, and also SSDs (PCIe format).

PCIe (peripheral component interconnect express) uses lanes implemented as differential signal pairs + and -.

x1 = 1 lane, x4 = 4 lanes, x16 = 16 lanes.

the more lanes, the higher the bandwidth.

**-storage connectors**

SATA ports - for HDD and SATA SSD.
M.2 slots - compact connectors for SSD. M.2 is a form factor (thin board), it can host either SATA SSD or NVMe SSD.

NVMe (non-volatile memory express) - protocol for SSD via PCIe. provides speeds of 10+ gb/s on modern generations.

VRM (voltage regulator module)

converts power for CPU and RAM. turns 12 v (from PSU) into required < 1.4 v for CPU and < 1.3 v for RAM.

details:

volt (V) = voltage U, potential difference that “opens” transistors and pushes charge through the circuit.
ampere (A) = current I, how many electrons flow per second.
watt (W) = power P, how much energy per second is consumed:
P = U × I

CPU transistors operate at very low voltages (≈1 v), otherwise they would burn, since modern transistors have ultra-thin gate oxide, and high electric field strength would destroy the dielectric.

at low voltage, to provide required power (watts), very high current (amperes) is needed.

example: CPU = 100 W:

at 12 v → 8 A

at 1.2 v → 83 A

that’s why VRM on the motherboard lowers 12 v to 1 v, but drastically increases the current.

VRM consists of:

MOSFET transistors
MOSFET = metal-oxide-semiconductor field-effect transistor.
it has three pins: drain, source, and gate.
if gate receives a signal, drain and source connect and current flows; if not, the circuit is open.

in VRM MOSFETs work in pairs:
high-side connects load to +12 v,
low-side connects it to ground.
they switch rapidly, turning constant 12 v into high-frequency pulses.

chokes (inductors)
a choke is coil of copper wire wound on a ferrite core (ferrite is ceramic material of iron oxides, non-conductive).
a coil resists sharp current changes:
when MOSFET is on, current flows through coil, magnetic field builds up, storing energy;
when MOSFET is off, coil keeps current flowing by releasing stored energy.

thus pulses are smoothed.

around the CPU socket there are usually dozens of capacitors of different types (ceramic, polymer) so they work at different frequencies and smooth sudden load spikes.

capacitors
a capacitor = two conductive plates separated by a dielectric (ceramic, polymer, aluminum oxide, etc.).
its job is to store electric charge and release it quickly.
in VRM they smooth ripples after the choke, equalizing output voltage.

**-BIOS/UEFI chip**

NAND/NOR flash die in a plastic package with firmware, stored in SPI flash memory, responsible for initial hardware initialization and OS boot, read directly by CPU at startup via SPI bus.

**-I/O ports**
USB, HDMI/DP, ethernet (RJ45), audio, sometimes VGA/DVI, DP, USB-C.

**-fan headers**

connectors for fans.

**-power connectors**

24-pin ATX power for the whole board

4/8-pin CPU power for processor supply

**-buses**

a shared set of conductors that transfer data, addresses, or control signals.

types:
address bus — points to the memory cell being accessed.
data bus — transfers the actual data.
control bus — transfers commands (e.g., read or write).

bus interfaces:
SATA - connects storage to chipset (~600 mb/s limit).
PCI express - modern universal bus with lanes.

how it works: buses are synchronized by clock signals, devices negotiate who transmits and who receives. it’s like a shared road where different participants can drive at different times.

---

### form factors:

ATX, micro-ATX, mini-ITX, E-ATX. the smaller the board, the fewer connectors and slots.

---

## Memory

### units of memory measurement

bit - the smallest unit of data: 0 or 1.

byte - 8 bits.

then come the "multiple units," and here is the nuance:

decimal:

1 KB = 1000 bytes

1 MB = 1000 KB = 10^6 bytes

1 GB = 10^9 bytes

this is how storage manufacturers count (HDD, SSD, USB flash drives).

binary:

1 KIB (kibibyte) = 1024 bytes

1 MIB = 1024 KIB = 2^20 bytes

1 GIB = 2^30 bytes

this is how operating systems and RAM manufacturers count.

---

### what bit storage technologies exist

**- DRAM - dynamic random access memory**

DRAM is volatile memory.

DRAM consists of cells, each made of a transistor and a capacitor (1 cell = 1 bit). the capacitor stores a charge of 1 or 0, which quickly leaks through the transistor and dielectric.

data must be constantly refreshed due to charge leakage; the memory controller located in the CPU (or formerly in the chipset) rereads and rewrites all data about every 64 ms.

because of frequent refreshing it is relatively slow, but it is cheap and compact.

use: main memory, video memory.

**- SRAM - static random access memory**

SRAM is also volatile.

data does not need refreshing, it stays as long as there is power.

SRAM consists of 6 transistors (to build a latch = 1 memory cell, you need two cross-coupled inverting circuits of 2 transistors each plus 2 for access). usually CMOS (complementary metal–oxide–semiconductor, technology where pairs of p- and n-channel transistors work together, reducing power consumption).

the logic latch stores 0 or 1 without capacitors, so the bit is stored not as charge but as the stable state of the circuit. this is faster and more reliable, but takes more chip area.

since it requires no refreshing, read/write is very fast. however, it takes more space on the die and is more expensive.

used in registers, caches.

**- VRAM*

GDDR - graphics DDR
GDDR is a type of DRAM with doubled/tripled data bus, optimized for parallel access from many GPU threads.

HBM - high bandwidth memory
3d: DRAM chips are stacked and connected vertically through TSV (through-silicon vias). this increases bus width (thousands of bits instead of hundreds) and reduces power consumption.

difference from regular DRAM (RAM): CPU memory works with a relatively narrow bus (64–128 bits), while GPU VRAM uses a very wide one (up to thousands of bits) for parallel processing.

**- NVRAM - non-volatile RAM general name for all non-volatile RAM**

- NAND flash

non-volatile but lifespan is limited by write/erase cycles — typically 500–1000 (QLC) up to 100k (SLC). the reason is gradual degradation of the floating gate insulator.

one cell = transistor with floating gate. it has two gates: one control gate, one floating gate insulated by dielectric, where electrons can be trapped. their presence or absence changes the transistor threshold, encoding 0 or 1.

can store 1, 2, 3, 4 bits per cell:

SLC = 1 bit → very reliable

MLC = 2 bits

TLC = 3 bits

QLC = 4 bits → cheap, high density, but slower and less durable

cells are grouped into pages (4–16 KB), then into blocks (128–512 pages).

used in SSD, USB sticks, memory cards.

- MRAM - magnetoresistive RAM
uses magnetic tunnel junction (MTJ). a cell has two ferromagnetic layers: one fixed, one free. their relative orientation (parallel or antiparallel) changes resistance, encoding 0/1.

non-volatile, fast, durable, but expensive, currently used mainly in automotive electronics.

- FRAM - ferroelectric RAM
uses ferroelectric crystals (dipoles switch under electric field and retain state without power).

in the cell, capacitor is replaced by ferroelectric. dipole state = 0 or 1.

expensive and small capacity, but very resistant to rewrites. used mainly in medical devices or bank cards.

- ROM - read only memory

non-volatile, data remains without power.

permanent memory programmed once or several times; after programming only reading is possible. examples: BIOS/UEFI firmware, microcontrollers in appliances, game cartridges.

types (where they are used?):

mask ROM - written at factory (not changeable)

PROM - programmable once

EPROM - erasable by ultraviolet

EEPROM - electrically erasable programmable ROM

flash (NAND/NOR) - modern type of EEPROM, widely used (BIOS, SSD, USB)

---

### functional memory hierarchy


**- CPU registers**
built from SRAM cells.
fastest memory in the PC. located on the CPU die, holds data loaded into ALU or FPU.

---

**- CPU caches**
also implemented with SRAM.
L1, L2, L3 caches store frequently used data from RAM for faster CPU access. when accessing RAM, part of the data is copied into cache. if CPU requests it again, it is taken from cache (ns) instead of RAM (tens of ns).

---

## RAM

volatile computer memory based on DRAM. it is the main working memory, where active data and program code are stored.

### working principle:

data in DRAM cells is organized as a matrix of rows and columns.

activation (ACT): a row is opened, its contents are transferred into sense amplifiers.

read/write (RD/WR): access to a specific column in the active row.

precharge (PRE): array is prepared for the next access.

one access cycle = ACT > RD/WR > PRE.

due to charge leakage DRAM requires periodic refresh (~every 64 ms).

## components:

- DRAM chips
dies made of cells (1 transistor + 1 capacitor = 1 bit).
data stored as charge in the capacitor.

- memory modules
printed circuit boards with DRAM chips.

UDIMM (unbuffered DIMM) - standard desktop modules

SO-DIMM - shortened modules for laptops and small PCs

RDIMM (registered DIMM) - server modules with buffer register reducing load on controller

LRDIMM (load-reduced DIMM) - server modules with extended buffering

- memory controller
built into modern CPU. manages row/column access, refresh cycles, bus synchronization.

- ECC (error-correcting code)
used in server modules. adds Hamming code bits to each data block to correct single-bit errors and detect double-bit errors.

---

**- video memory (VRAM)**

difference from normal DRAM: much wider bus + special GPU controllers for thousands of parallel threads.

**- persistent storage: HDD, SSD**

## HDD

hard disk drive - magnetic storage device where data is stored on spinning platters.

### working principle:

when powered on, spindle motor spins the platters. actuator positions heads over the needed track.

write: head generates a magnetic field and changes orientation of a domain (north/south = 0/1).

read: head senses domain orientation and converts it to electric signal. signals are amplified, processed by controller, and sent to the PC via interface.

### components:

**- platters**
made of glass, aluminum, or ceramic. coated with thin ferromagnetic layer (cobalt, nickel, platinum alloys), protective carbon top layer and lubricant. data stored as domain orientation.

**- spindle and motor**
spindle holds platters, motor spins them. controlled by driver circuit, sets RPM.

**- actuator**
moving arm that positions heads across the platter radius. driven by electromagnet for fast precise positioning.

**- read/write heads**
microscopic elements on actuator arms. write: create magnetic field, flip domains. read: use magnetoresistive effect (resistance depends on field orientation). heads float 5–10 nm above surface due to air cushion from spinning.

**- head stack**
set of arms with heads for both sides of platters.

**- PCB controller**
under the drive. includes:

controller - manages motors, heads, SATA/SAS/USB interface

preamps - boost weak signals from heads

DRAM cache - buffers writes, holds sector translation tables

**- enclosure and filters**

sealed body with air or helium inside. filters trap dust/micro-particles since one speck can crash the head.

---

## SSD

solid-state drive - electronic storage using NAND semiconductor cells, no moving parts.

### working principle:

write: controller receives OS command, translates to physical addresses, charges/discharges floating gates in NAND.

read: controller accesses pages, checks gate state (charge/no charge) = 0/1.

erase: whole block must be erased before rewriting. controller uses garbage collection and cache to mitigate delays.

### components:

NAND flash chips
dies of semiconductor memory. floating gate transistors trap or release electrons: charged = 1, empty = 0. modern types store multiple bits per cell (SLC, MLC, TLC, QLC).
NAND dies are grouped into arrays (banks, blocks, pages).

**- controller**
specialized processor managing NAND access. functions:

FTL - flash translation layer, maps logical → physical addresses

wear leveling - spreads writes evenly

garbage collection - erases blocks for reuse

ECC - error correction

**- cache**

DRAM cache - separate memory module for FTL tables, speeds access

SLC cache - part of NAND used in 1-bit mode for fast buffering

**- interface**

SATA, limited to ~550 MB/s

PCIe (NVMe), up to 14 GB/s (PCIe 5.0)
connectors are copper with gold plating.

**- PCB**
multilayer board with traces for power/signals, holds all components.

**- power & protection**

3.3 V M.2 or 5 V SATA power

server SSDs use capacitors (PLP - power loss protection) to finish writes on sudden shutdown

---

**- firmware ROM**

chip storing BIOS/UEFI. holds low-level code and drivers to boot the PC. BIOS = old standard, UEFI = modern (graphics, GPT, drivers).

**- virtual memory & swap**

OS mechanism where process address space > physical RAM. when RAM is full, pages are swapped to disk (swap file/partition). adds flexibility but slow.

---

## Tasks

---

### Hardware components
---

**- CPU**  
the CPU is the part of the computer that executes program instructions. It performs calculations, logical operations, and controls the flow of data.  
modern CPUs have multiple cores, which allow them to work on several tasks at the same time. without the CPU, software cannot run.  

**- Motherboard**
the motherboard is the main circuit board that connects all hardware parts. components like the CPU, RAM, storage devices, GPU, and PSU are either installed directly on it or connected through it. modern motherboards often include built-in functions such as network connection, sound, and sometimes basic graphics output.  

**- RAM**
RAM is the short-term memory of the computer. it stores data and program instructions that the CPU needs immediately. RAM is much faster than storage, but it is volatile: all data is lost once the computer is powered off.  

**- Storage Device**
storage devices keep data permanently, even when the computer is turned off.
- HDD (Hard Disk Drive): uses spinning disks, cheaper and with large capacity but slower.  
- SSD (Solid State Drive): uses flash memory, much faster and more reliable than HDDs.  
storage is where the operating system, applications, and personal files are saved.  

**- PSU** 
the PSU takes electricity from the wall and converts it into the lower voltages required by the components. it powers the motherboard, CPU, GPU, storage, and other devices. a stable PSU is essential for the reliability of the entire system.  

**- GPU** 
the GPU is specialized for rendering images, videos, and animations.  
- it is highly efficient in parallel calculations, which makes it faster than the CPU for graphics tasks.  
- some CPUs have integrated graphics, but dedicated GPUs are used for gaming, design, and other demanding applications.  

**- Cooling**
all electronic parts generate heat while working. Cooling systems remove this heat to keep the components safe.  
- air cooling: uses fans and heatsinks, the most common method.  
- water cooling: uses liquid to transport heat away, more efficient for high-performance systems.  
- without proper cooling, the system could overheat and malfunction.  

--- 

### Advanced Questions
---

<details>
  <summary>How fast (in GHz) is the CPU you are using right now?</summary>
  <p>4.4GHz</p>
</details>

<details>
  <summary>What chipset is on the motherboard? Could there be more options?</summary>
  <p>apple M4 SoC, no alternatives for laptops because everything is already integrated in one chip</p>
</details>

<details>
  <summary>How many gigabytes of RAM are in the PC you’re using?</summary>
  <p>24GB </p>
</details>

<details>
  <summary>What is/are the storage medium/media in your PC?</summary>
  <p>SSD, 512GB</p>
</details>

<details>
  <summary>Where is the PSU in your PC? What about a laptop?</summary>
  <p>laptop has an external power adapter, PC has an internal PSU</p>
</details>

<details>
  <summary>Do you have a GPU?</summary>
  <p>yes, it is integrated in the chip</p>
</details>

<details>
  <summary>How does the cooling work in your device? What about a smartphone?</summary>
  <p>this laptop has no fan and has a passive cooling system with heatsink. same system goes fot smartphones</p>
</details>

---

### Hypothetical machine
---

[link to the hypothetical machine components](https://www.galaxus.ch/en/shoplist/show/CfDJ8KEwk7Q9MilFpMKq1D7DsMYZHMzdi6N0nHtamDe5NRsTGKuaTQzHPAtoqvRUC12oqlu1W7KiygJGgfElHFwuULBD0t1MmHeDoXrc9kJbzqwlZGMPJg1c3iRPtvPAGZ8ZDA)

---

### Bits and bytes

<details>
  <summary>Say you have a gigabit internet connection (downstream). How many kilobytes can you download per second?​</summary>
  <p>a gigabit is 1,000,000,000 bits/sec. Divide by 8 = 125,000,000 bytes/sec, which is about 122,070 KB/sec</p>
</details>

<details>
  <summary>How many bits are in a Mebibyte? </summary>
  <p>O
  one Mebibyte = 2^20 bytes = 1,048,576 bytes. in bits: 1,048,576 × 8 = 8,388,608 bits</p>
</details>

<details>
  <summary>you buy an HDD advertised with 1TB. How much usable space will the Windows operating system report you and why?​</summary>
  <p>The drive shows about 931 GB usable. the difference comes from decimal vs binary units​</p>
</details>

<details>
  <summary>Decode the following binary sequences to text. Each character uses 8-bits. ​

01000001011011010110000101101110011011110111100000100000010101000110010101100001

Describe your approach in your learning-blog.​</summary>
  <p>i divided the long binary sequence into separate 8-bit chunks, since each ASCII character is stored in 8 bits. then I translated each 8-bit value with the ASCII table into its corresponding letter, putting all characters together gave me the text “Amanox Tea”​</p>
</details>

---

### Multiplication with basic instructions