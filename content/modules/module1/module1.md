---
title: "Module 1"
summary: Hardware
date: 2025-08-15
weight: 1
type: page
draft: false
---

## Tasks

---

### Hardware components

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

### More on HDDs and SSDs

If you ever shopped for HDDs, you probably stumbled across multiple flavors. For example, consumer-grade, NAS-grade and server-grade. ​

What are the differences between those grades?​

- consumer HDD which is made for normal PCs, cheap but not built for 24/7
- NAS HDD which is designed for network storage, optimized for multiple drives running all the time, better vibration protection
- server or enterprise HDD is very reliable, can run 24/7 under heavy load, long warranty, but much more expensive

Are there grades/tiers for SSDs? ​

- consumer SSD which is SATA or NVMe, fast but not built for extreme workloads
- enterprise SSD has higher endurance, power loss protection, stable speed which is better for servers

Search the web for 2 HDDs and SSDs that you would use in a consumer PC or server (1 for each use case)

- ​consumer pc:
HDD: western digital blue 2tb
SSD: samsung 970 evo plus 1tb
- server:
HDD: seagate exos x18 18tb
SSD: samsung pm9a3 3.84tb

---

### Desired interfaces

What are your desired interfaces in a consumer PC/laptop?​

- consumer pc/laptop:
USB-C with charging and video out
USB-A ports for mouse, keyboard, headset
DP for external monitor
WI-FI 6/7 and BLUETOOTH
M.2 NVME slot for fast SSD
SATA for extra drives
AUDIO JACK for headphones

- server:
BMC/IPMI for remote management
MGMT NIC (RJ-45) for that management
high-speed network ports: 10/25/40/100 GBE with SFP+ or QSFP modules
FRONT BAYS with SAS/SATA/NVME drives for storage
RAID controller for reliability
REDUNDANT PSU

---

### Pros and Cons of display technologies

Why did manufacturers ditch the CRT and plasma technologies?​

- CRT cos its too heavy, too deep, uses lots of power, not good for high resolution
- Plasma had better picture than CRT, but still very hot, power hungry, had risk of burn-in and was expensive to make

What are the pros and cons of LCD and OLED compared to eachother?

- LCD:
pros: cheaper, bright, long lifespan, no burn-in
cons: weaker contrast, slower response, viewing angles not perfect

- OLED:
pros: good contrast, better colors, fast response, flexible panels possible
cons: can burn-in over time, not as bright on large screens, usually more expensive

---

### Office workplace​

Create a list of IT-components needed to setup an office workplace (without furniture). ​​How should the PC perform? Did you choose a laptop or a workstation?​

- main pc:
i would choose a laptop like windows or mac, it is flexible cos i can work in the office, at home or on the move. performance should be good enough for office apps, programming, video calls, etc so a modern cpu, 16 gb RAM and a fast NVMe SSD are enough
peripherals in office:
dock station: connects laptop to everything with one usb-c cable
external monitor
keyboard + mouse
headset with microphone for calls
network: stable connection via ethernet but also wifi 6
printer/scanner shared in the office network

What interfaces do you need?

usb-c/thunderbolt for docking, charging, external monitor
rj-45 ethernet
audio jack or bluetooth for headset

Is an upgrade possible down the road?

with a laptop upgrades are limited, usually only RAM and SSD can be changed, but in the office i can upgrade peripherals easily like bigger monitors, better dock, new headset, faster network, etc. the system stays flexible because the laptop connects to all devices through the dock

---

### Are you a fan of airflow?​

What metric should be high for a fan on a heatsink?

- for a cpu or gpu heatsink you want static pressure to be high, this means the fan can push air strongly through the dense fins of the cooler

What metric should be high for a case fan?​

- for case fans you want airflow to be high, the goal is to move as much air as possible through the case to refresh the inside with cooler outside air

Why do servers often use small fans instead of bigger ones?​

- ervers use small high-rpm fans because racks are very tight and airflow paths are narrow, small fans can spin faster, create strong pressure, and keep air moving straight front-to-back through the chassis. they are very loud, but in datacenters noise doesn’t really matter