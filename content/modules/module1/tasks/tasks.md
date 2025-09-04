---
title: "Exercises"
summary: "Here I will post my solutions to the tasks from the module"
date: 2025-08-16
type: post
draft: false
design:
  view: card-grid
outputs: ["HTML"]
slug: "tasks"
url: "/modules/module1/tasks/"
---


## Hardware components
---

#### CPU  
The CPU is the part of the computer that executes program instructions. It performs calculations, logical operations, and controls the flow of data.  
- Modern CPUs have multiple cores, which allow them to work on several tasks at the same time.  
- Without the CPU, software cannot run.  

#### Motherboard 
The motherboard is the main circuit board that connects all hardware parts.  
- Components like the CPU, RAM, storage devices, GPU, and PSU are either installed directly on it or connected through it.  
- Modern motherboards often include built-in functions such as network connection, sound, and sometimes basic graphics output.  

#### RAM 
RAM is the short-term memory of the computer.  
- It stores data and program instructions that the CPU needs immediately.  
- RAM is much faster than storage, but it is volatile: all data is lost once the computer is powered off.  

#### Storage Device  
Storage devices keep data permanently, even when the computer is turned off.  
- HDD (Hard Disk Drive): uses spinning disks, cheaper and with large capacity but slower.  
- SSD (Solid State Drive): uses flash memory, much faster and more reliable than HDDs.  
- Storage is where the operating system, applications, and personal files are saved.  

#### PSU  
The PSU takes electricity from the wall and converts it into the lower voltages required by the components.  
- It powers the motherboard, CPU, GPU, storage, and other devices.  
- A stable PSU is essential for the reliability of the entire system.  

#### GPU  
The GPU is specialized for rendering images, videos, and animations.  
- It is highly efficient in parallel calculations, which makes it faster than the CPU for graphics tasks.  
- Some CPUs have integrated graphics, but dedicated GPUs are used for gaming, design, and other demanding applications.  

#### Cooling  
All electronic parts generate heat while working. Cooling systems remove this heat to keep the components safe.  
- Air cooling: uses fans and heatsinks, the most common method.  
- Water cooling: uses liquid to transport heat away, more efficient for high-performance systems.  
- Without proper cooling, the system could overheat and malfunction.  

## Advanced Questions
---

<details>
  <summary>How fast (in GHz) is the CPU you are using right now?</summary>
  <p>4.4GHz</p>
</details>

<details>
  <summary>What chipset is on the motherboard? Could there be more options?</summary>
  <p>Apple M4 SoC, no alternatives for laptops because everything is already integrated in one chip</p>
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
  <p>Laptop has an external power adapter, PC has an internal PSU</p>
</details>

<details>
  <summary>Do you have a GPU?</summary>
  <p>Yes, it is integrated in the chip</p>
</details>

<details>
  <summary>How does the cooling work in your device? What about a smartphone?</summary>
  <p>This laptop has no fan and has a passive cooling system with heatsink. Same system goes fot smartphones</p>
</details>

## Hypothetical machine
---

[Link to the hypothetical machine components](https://www.galaxus.ch/en/shoplist/show/CfDJ8KEwk7Q9MilFpMKq1D7DsMYZHMzdi6N0nHtamDe5NRsTGKuaTQzHPAtoqvRUC12oqlu1W7KiygJGgfElHFwuULBD0t1MmHeDoXrc9kJbzqwlZGMPJg1c3iRPtvPAGZ8ZDA)

## Bits and bytes

<details>
  <summary>Say you have a gigabit internet connection (downstream). How many kilobytes can you download per second?​</summary>
  <p>A gigabit is 1,000,000,000 bits/sec. Divide by 8 = 125,000,000 bytes/sec, which is about 122,070 KB/sec</p>
</details>

<details>
  <summary>How many bits are in a Mebibyte? </summary>
  <p>One Mebibyte = 2^20 bytes = 1,048,576 bytes. In bits: 1,048,576 × 8 = 8,388,608 bits</p>
</details>

<details>
  <summary>You buy an HDD advertised with 1TB. How much usable space will the Windows operating system report you and why?​</summary>
  <p>The drive shows about 931 GB usable. The difference comes from decimal vs binary units​</p>
</details>

<details>
  <summary>Decode the following binary sequences to text. Each character uses 8-bits. ​

01000001011011010110000101101110011011110111100000100000010101000110010101100001

Describe your approach in your learning-blog.​</summary>
  <p>I divided the long binary sequence into separate 8-bit chunks, since each ASCII character is stored in 8 bits. Then I translated each 8-bit value with the ASCII table into its corresponding letter, putting all characters together gave me the text “Amanox Tea”​</p>
</details>

## Multiplication with basic instructions