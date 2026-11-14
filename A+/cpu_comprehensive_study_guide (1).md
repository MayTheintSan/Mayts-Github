# Module: Central Processing Unit (CPU) Architecture & Specifications

*Source Curriculum Reference: iXUAA Learning Series (www.youtube.com/@iXUAA)*

## 1. Introduction to the Central Processing Unit (CPU)

The **CPU** (Central Processing Unit, also called the Processor or Microprocessor) is the main "brain" of a computer. It handles calculations, processes instructions, and works together with RAM, graphics processors (GPUs), and Input/Output (I/O) devices to run programs and display results.

* **Historical Milestone (1971):** Intel created the first commercial single-chip microprocessor—the **DIPP Type 4004** processor, which used a 4-bit architecture.
* **Machine Language & Binary System:** CPUs understand machine language based on binary electrical signals:
  * **Voltage ON:** `1` (Represents 1 bit)
  * **Voltage OFF:** `0` (Represents 1 bit)

### Units of Computer Memory & Data Measurement
* 8 bits (b) = 1 Byte (B)
* 1024 B = 1 KiloByte (KB)
* 1024 KB = 1 MegaByte (MB)
* 1024 MB = 1 GigaByte (GB)
* 1024 GB = 1 TerraByte (TB)
* 1024 TB = 1 PetaByte (PB)
* 1024 PB = 1 ExaByte (EB)
* 1024 EB = 1 ZettaByte (ZB)
* 1024 ZB = 1 YottaByte (YB)
* 1024 YottaByte = 1 RonnaByte
* 1024 RonnaByte = 1 QuettaByte

> **Practical Data Calculation Example:**
> For the name `"May Theint San"` (14 characters $\times$ 8 bits per character) = **112 bits / 14 Bytes**.

## 2. How a CPU Processes Instructions (Fetch-Decode-Execute)

Every task a CPU performs follows a fast, repeating four-step cycle:

1. **Fetch:** The CPU grabs the next instruction from system RAM and holds it in its internal memory.
2. **Decode:** The Control Unit translates the instruction to understand what action is needed (like adding numbers or moving data).
3. **Execute:** The Arithmetic Logic Unit (ALU) carries out the math or logic operation.
4. **Writeback:** The CPU saves the final result back into its internal registers or system RAM.

## 3. Physical Build & Transistor Technology

CPUs are built on thin slices of purified silicon called semiconductor wafers.

* **MOSFET Technology:** Modern Integrated Circuit (IC) chips hold billions of microscopic **MOSFETs** (Metal-Oxide-Semiconductor Field-Effect Transistors) that act as ultra-fast electronic switches.
* **How We Measure a Better CPU:**
  * **Logically:** By comparing its processing speed, clock rate, and efficiency.
  * **Physically:** By comparing how many transistors are packed inside (for example, Apple's ARM-based M1 Max chip packed 57 billion MOSFETs).

### CPU Housing & Substrates
* **Ceramic Housing:** Used in older or specialized chips because purified ceramic resists extreme heat (surviving over 2000°C—similar to carbon-ceramic brakes on Formula 1 race cars). Even though normal CPUs stay under 100°C, ceramic protected the silicon well.
* **Organic Substrates:** Because ceramic is expensive to make and can crack easily if dropped or pressed too hard, modern consumer CPUs use durable organic substrates instead.

## 4. Inside the CPU: Cores, Threads & Cache

### Cores and Multi-Threading
* **Physical Core:** An individual processing unit inside the CPU chip that can run its own tasks independently. Multi-core CPUs (like 6-core, 8-core, or 16-core chips) handle heavy multitasking much smoothly.
* **Logical Processors / Threads (Hyper-Threading / SMT):** Features like Intel **Hyper-Threading** and AMD **SMT (Simultaneous Multi-Threading)** let a single physical core split its workload into two virtual threads at once, boosting speed during demanding tasks.

### CPU Cache Memory (L1, L2, L3)
Because pulling data from main system RAM takes extra time, CPUs include small pools of ultra-fast memory right on the chip to store frequently used data:

| Cache Level | Typical Size | Speed & Location | Purpose |
| :--- | :--- | :--- | :--- |
| **L1 Cache** | ~32KB – 80KB per core | Fastest; built right inside each core. | Holds immediate data the core is actively working on right now. |
| **L2 Cache** | ~256KB – 2MB per core | Very fast; dedicated to each core. | Quickly feeds upcoming data into the L1 cache. |
| **L3 Cache** | ~16MB – 96MB+ shared | Fast; shared by all cores on the chip. | Keeps cores from waiting on slower main system RAM. |

## 5. Processor Architectures: x86 vs. ARM

Processors are designed around two major instruction styles:

* **x86 / x86-64 (CISC – Complex Instruction Set Computer):**
  * **How it works:** Built to handle complex, heavy instructions directly.
  * **Where it's used:** Desktop PCs, gaming laptops, workstations, and servers (made mainly by Intel and AMD).
  * **Trade-offs:** Delivers high raw power, but uses more electricity and needs active cooling fans.
* **ARM (RISC – Reduced Instruction Set Computer):**
  * **How it works:** Uses simpler, streamlined instructions that run very efficiently.
  * **Where it's used:** Smartphones, tablets, and modern thin-and-light laptops (such as Apple Silicon M-series and Qualcomm Snapdragon chips).
  * **Trade-offs:** Great battery life and very low heat—many ARM laptops don't even need cooling fans inside.

## 6. Core CPU Components & Packaging

1. **Manufacturer:** The company that designs the processor (e.g., Intel, AMD, Qualcomm).
2. **IHS (Integrated Heat Spreader):** The metal cover on top of the CPU that serves two main jobs: protecting the fragile silicon chip from dust and pressure, and spreading heat outward to the cooler.
3. **Socket & Mounting Types:**
   * **DIPP** (Dual In-line Package)
   * **PLCC** (Plastic Leaded Chip Carrier)
   * **LGA** (Land Grid Array — pins are on the motherboard socket)
   * **PGA** (Pin Grid Array — pins are on the bottom of the CPU)
   * **BGA** (Ball Grid Array — soldered permanently onto the motherboard, common in laptops)
4. **Cooling Systems:**
   * **Active Cooling:** Uses moving parts to push heat away (Air coolers with fans, or Liquid coolers with pumps and radiators).
   * **Passive Cooling:** Uses only a metal heatsink with no moving fans.
5. **Power Connector:** Gets dedicated electricity from the motherboard through **+12V CPU power ports** (such as 4-pin P4 or 8-pin connectors).

### Clock Speed, Overclocking & Thermal Throttling
* **Clock Speed (GHz):** Shows how many billions of cycles a CPU completes per second (for example, `3.80 GHz`).
* **Overclocking:** Manually tuning a CPU to run faster than its factory speed by raising power limits (requires an unlocked chip and strong cooling).
* **Thermal Throttling:** A built-in safety feature where the CPU automatically slows itself down if it gets too hot (usually around 100°C) so the chip doesn't get damaged.

## 7. Intel CPU Lineups & Naming Guide

* **Entry-Level Lineups:** Celeron, Pentium
* **Mainstream Core Series (Introduced ~2005):** Core i3, i5, i7, i9 (Core i9 started with the 9th generation; the series goes up to the 14th generation, followed by **Core Ultra** chips built with AI features).
* **Server & Workstation Series:** Xeon
* **Low-Power Mobile Series:** Atom

### Model Number Breakdown Example: `Intel Core i7-8700 @3.20GHz`
* `Intel` = Manufacturer Name
* `Core` = Brand Series Name
* `i7` = Performance Tier Model Name
* `@3.20GHz` = Base Clock Speed
* `8700` = `8` (Generation ID) + `700` (SKU / Stock Keeping Unit)
  * *SKU Rule:* 3rd through 11th generations use 3-digit SKUs; 12th through 14th generations use 2-digit SKUs.

### Intel Processor Suffix Meanings
* **No Suffix (e.g., `i7-8700`):** Standard desktop processor.
* **K (e.g., `i7-13700K`):** Unlocked desktop chip made for overclocking.
* **F (e.g., `i7-13700F`):** Desktop chip with **no built-in GPU**; you must install a separate graphics card to see anything on your screen.
* **U / P / M (e.g., `i7-8550U`):** Laptop processors built to save battery power (`U` = Ultra-low power, `P` = Portable performance, `M` = Legacy Mobile).
* **H / HX / Q:** High-performance processors built for gaming and heavy workstation laptops.
* **G1 – G7:** Shows the strength of built-in graphics on laptop processors.
* **S:** Special edition desktop chips tuned for higher peak speeds.

### Intel Core Generation Codenames
| Generation | Codename |
| :--- | :--- |
| 1st Gen | Nehalem |
| 2nd Gen | Sandy Bridge |
| 3rd Gen | Ivy Bridge |
| 4th Gen | Haswell |
| 5th Gen | Broadwell |
| 6th Gen | Skylake |
| 7th Gen | Kaby Lake |
| 8th Gen | Coffee Lake |
| 9th Gen | Coffee Lake Refresh |
| 10th Gen | Comet Lake / Ice Lake |
| 11th Gen | Tiger Lake / Rocket Lake |
| 12th Gen | Alder Lake |
| 13th Gen | Raptor Lake |
| 14th Gen | Raptor Lake Refresh / Meteor Lake |

## 8. AMD CPU Lineups & Naming Guide

* **Entry-Level Lineup:** Athlon (Silver, Gold)
* **Mainstream Consumer Series (Introduced 2017):** Ryzen 3, Ryzen 5, Ryzen 7, Ryzen 9
* **High-End Desktop & Workstation Series:** Ryzen Threadripper
* **Enterprise Server Series:** EPYC

### AMD Ryzen Generation (Zen Architecture) Map
| Architecture Generation | Release Timeline | Corresponding Ryzen Series |
| :--- | :--- | :--- |
| **Zen** | March 2017 | Ryzen 1000 series |
| **Zen+** | April 2018 | Ryzen 2000 series |
| **Zen 2** | July 2019 | Ryzen 3000 series |
| **Zen 3** | November 2020 | Ryzen 5000 series |
| **Zen 4** | September 2022 | Ryzen 7000 series |
| **Zen 5** | August 2024 | Ryzen 9000 series |