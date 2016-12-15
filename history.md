---
layout: page
title: History
permalink: /history
---

In this part of the website, we will discuss notable spacecrafts that have implemented computer architectures that countered the harsh conditions of space. Feel free to click on any of the links that will give you more information on the specific spacecraft.


## 1977: 

The Voyager program was launched in 1977 to explore the further planets from the solar system while the alignments of Jupiter, Saturn, Uranus, and Neptune were efficient for travel. Two probes were launched and are still in operation.

<center><img src="http://voyager.jpl.nasa.gov/news/images/PIA17049_top.jpg"></center>

<center><i>Voyager 1, travelling in deep space.</i></center>

The Voyager program has 2 probes still in extended mission and are both around 16 billion miles away from earth. Redundancy management was a great theme in the Voyager computers as they each had 3 different computer types with 2 of each kind.


## 2004:

Spirit 
- Launch: June 10 2003
- Land: January 3 2004

Opportunity 
- Launch: July 7 2003
- Land: January 24 2004

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
- Maximum CPU clock: 2.5MHz to 33MHz
- Minimum Feature Size: 0.5 μm
- Instruction Set: POWER1
- Cores: 1
- L1 chache: 8KB
- Processing Speed: 35MIPS
- Architecture: 32-bit RISC
- Transistors: 1.1 million
- ECC RAM(Error Correcting Code Memory): 128MB
- Cost: Between US$200,000 and US$300,000

#### Power Problem
Usually the RAD6000 has selectable clock frequency options of 33MHz and 66MHz. However, in the Mars Rovers Spirit and Opportunity project, it operates at 20MHz to consume less power (slower clock speed consumes less power). Fortunately, because RAD6000 processor has 32-bit RISC architecture which allows processor to pipeline and execute multiple instructions per single cycle, it was possible to achieve a high processing throughput even with the low clock frequency. Also, because it only has 1.1 million transistors, the power requirement is very low, allowing the motherboard to operate with solar cells.


#### Development History
RAD6000 was succeeded by RAD750, which was produced from 2001 and used in variety of spacecrafts from 2005 to 2012. RAD750 is succeeded by RAD5500.

## 2006-2026:

New Horizons, launched in 2006, was designed for interplanetary travel. The spacecraft had two major computer system. One for commanding and data handling, and the other for guidance and control processing. The chips and circuits used in the computer are radiation hardened (MIPS R3000 CPU). Redundancy management is also present, as multiple clocks and timing routines are implemented to prevent errors in the computer process.

<center><img src="http://a.abcnews.com/images/Technology/gty_new_horizons_kennedy_jc_150716_16x9_992.jpg"></center>

<center><i>New Horizons probe examined.</i></center>

