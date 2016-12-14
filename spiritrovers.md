---
layout: page
title: Spirit and Opportunity Rovers 
permalink: /history/spiritrovers
---

Spirit Launch: June 10 2003
Spirit Land: January 3 2004

Opportunity Launch: July 7 2003
Opportunity Land: January 24 2004

### Background
Spirit and Opportunity Mars rovers conduct field geology and make atmospheric observation. They weight nearly 180kg and far exceeded their initial 90 day warranties on Mars.

### RAD6000

#### Background
RAD6000 is a radiation-hardened microprocessor designed by IBM.It is a circuit copy of the IBM RISC System/ 6000 single chip CPU; RAD6000 is a circuit-by-circuit translation of the IBM POWER microprocessor, which consisted of individual integrated circuits. It was produced from 1997 and as of 2008, there were 200 RAD6000 processors in space in various spacecrafts, landers, probes, orbiter and rover.

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/baerad6000.png" alt="BAE RAD6000" style="width: 300px;"/>
  <figcaption>BAE RAD6000 Single Chip CPU</figcaption>
</figure>
</center>

#### Specification
Maximum CPU clock: 2.5MHz to 33MHz

Minimum Feature Size: 0.5 μm

Instruction Set: POWER1

Cores: 1

L1 chache: 8KB

Processing Speed: 35MIPS

Architecture: 32-bit RISC

Transistors: 1.1 million

ECC RAM(Error Correcting Code Memory): 128MB

Cost: Between US$200,000 and US$300,000

#### Power Problem
Usually the RAD6000 has selectable clock frequency options of 33MHz and 66MHz. However, in the Mars Rovers Spirit and Opportunity project, it operates at 20MHz to consume less power (slower clock speed consumes less power). Fortunately, because RAD6000 processor has 32-bit RISC architecture which allows processor to pipeline and execute multiple instructions per single cycle, it was possible to achieve a high processing throughput even with the low clock frequency. Also, because it only has 1.1 million transistors, the power requirement is very low, allowing the motherboard to operate with solar cells.

#### Development History
RAD6000 was succeeded by RAD750, which was produced from 2001 and used in variety of spacecrafts from 2005 to 2012. RAD750 is succeeded by RAD5500.


