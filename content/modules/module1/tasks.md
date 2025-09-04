---
title: "Exercises"
summary: "Here I will post my solutions to the tasks from the module"
date: 2025-08-15
weight: 2
type: page
_build:
  list: never 

design:
  card:
    shadow: true
    border_radius: "0.5rem"
    padding: "1rem"
    hover_effect: lift
    color: red
    background_color: default
---


## Hardware components
---

#### CPU  
the CPU is the part of the computer that executes program instructions. It performs calculations, logical operations, and controls the flow of data.  
- modern CPUs have multiple cores, which allow them to work on several tasks at the same time.  
- without the CPU, software cannot run.  

#### Motherboard 
the motherboard is the main circuit board that connects all hardware parts.  
- components like the CPU, RAM, storage devices, GPU, and PSU are either installed directly on it or connected through it.  
- modern motherboards often include built-in functions such as network connection, sound, and sometimes basic graphics output.  

#### RAM 
RAM is the short-term memory of the computer.  
- it stores data and program instructions that the CPU needs immediately.  
- RAM is much faster than storage, but it is volatile: all data is lost once the computer is powered off.  

#### Storage Device  
storage devices keep data permanently, even when the computer is turned off.  
- HDD (Hard Disk Drive): uses spinning disks, cheaper and with large capacity but slower.  
- SSD (Solid State Drive): uses flash memory, much faster and more reliable than HDDs.  
- storage is where the operating system, applications, and personal files are saved.  

#### PSU  
the PSU takes electricity from the wall and converts it into the lower voltages required by the components.  
- it powers the motherboard, CPU, GPU, storage, and other devices.  
- a stable PSU is essential for the reliability of the entire system.  

#### GPU  
the GPU is specialized for rendering images, videos, and animations.  
- it is highly efficient in parallel calculations, which makes it faster than the CPU for graphics tasks.  
- some CPUs have integrated graphics, but dedicated GPUs are used for gaming, design, and other demanding applications.  

#### Cooling  
all electronic parts generate heat while working. Cooling systems remove this heat to keep the components safe.  
- air cooling: uses fans and heatsinks, the most common method.  
- water cooling: uses liquid to transport heat away, more efficient for high-performance systems.  
- without proper cooling, the system could overheat and malfunction.  

--- 

## Advanced Questions
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

## Hypothetical machine
---

[link to the hypothetical machine components](https://www.galaxus.ch/en/shoplist/show/CfDJ8KEwk7Q9MilFpMKq1D7DsMYZHMzdi6N0nHtamDe5NRsTGKuaTQzHPAtoqvRUC12oqlu1W7KiygJGgfElHFwuULBD0t1MmHeDoXrc9kJbzqwlZGMPJg1c3iRPtvPAGZ8ZDA)

---

## Bits and bytes

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

## Multiplication with basic instructions