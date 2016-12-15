---
layout: page
title: Space Conditions - Radiation
permalink: /spaceconditions/radiation
---

## Radiation in Space
Space is a highly radioactive environment. There are four primary causes of this radiation: trapped electrons, trapped protons, solar protons and cosmic rays. 

Trapped electrons are negatively charged particles that are relatively low in mass, but they are also extremely energetic. Due to their small masses, they are typically found is very high orbits such as the Geosynchronous orbits (or GEO orbits) that are approximately 36,000 km above the earth. 

Trapped protons are positively charged particles held captive by a planet’s gravitation field. They are less energetic that electrons, but they are approximately 2000 times more massive than electrons. They exist in high concentrations at low altitudes. For example, Low Earth Orbits (LEOs), such as those located 1400km – 2000km from the earth’s surface, are proton-dominated orbits. 

Solar protons are similar to trapped protons except they are ejected from the Sun during a solar flare event and are therefore not trapped in the planet’s gravitational field.

Cosmic rays are the final source of natural space-borne radiation. They are comprised of alpha particles, heavy ions and protons. 

Heavy ions are the primary concern when considering the effects of cosmic rays on semiconductors because the massive, highly charged particles can cause severe damage to devices. How trapped protons, trapped electrons, solar protons and cosmic rays interact with semiconductor components is generically called radiation effects. 


## Space Radiation Effects
Total Ionizing Dose (TID)

Single Event Effect (SEE)

- Single Event Latch-Up (SEL)

- Single Event Upset (SEU)

- Single Event Transient (SET)

- Single Event Functional Interrupt (SEFI)

Other Radiation Effect 

- Prompt Dose/ Dose Rate

- Neutron Single Event Upset

TID, SEL and SEU are most commonly used to show how resistant an electronic device is against radiation.


## Radiation Hardening
Radiation hardening is making electronic components and systems resistant to damage and malfunctions caused by ionizing radiation.

### Why is the technology behind
Due to the extensive development and testing required to produce a radiation-tolerant design of a microelectronic chip, radiation-hardened chips tend to lag behind the most recent developments. Radiation-hardened electronics are typically two to four generations behind commercial electronics in terms of performance.

### How is it different from commercial electronics
Radiation hardened electronics contain extra transistors that take more energy to switch on and off, so that the cosmic rays can’t trigger them too easily. However, they are more expensive, power consuming and slow.

### How to hardened against radiation
Process insulators so that there are fewer defects, which reduces the number of sites where positive charges can be trapped.

Dope regions between transistors to make devices more resistant to the effects of radiation
Shield electronics in enclosures made of lead/ very dense materials to help protect the electronics from radiation. 

### Radiation Hardening Technique

1.Insulating Substrate
Manufacture hardened chips on insulating substrate instead of semiconductor wafer. Insulating substrate enables chips to withstand more radiation, many orders of magnitude greater that commercial chips, which can withstand 5 to 10 krad. Some examples of insulating substrate include Silicon on insulator (SOI) and Silicon on sapphire (SOS).

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/semiconductorwafer.png" alt="Semiconductor Wafer" style="width: 300px;"/>
  <figcaption>Semiconductor Wafer</figcaption>
</figure>
</center>


2.Bipolar IC
Bipolar IC generally have higher tolerance to radiation than CMOS circuits.


3.Magnetoresistive RAM (MRAM)
MRAM data is stored in magnetic state, rather than electronic charge, resulting in longer data retention and reduction in power. Early tests suggest that MRAM is not susceptible to ionization induced data loss.


4.Shielding

Shielding the package

- Shielding reduces the intensity of radiation depending on the thickness. 

Shielding the chips

- Boron-10 readily captures neutrons and undergoes alpha decay. Chips can be protected by shilded using depleted boron (isotope boron-11).


5.Static Random Access Memory (SRAM)
SRAM is more rugged than capacitor based Dynamic Random Access Memory (DRAM). However, it is larger and more expensive.

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/sramdram.png" alt="SRAM and DRAM" style="width: 500px;"/>
  <figcaption>SRAM and DRAM</figcaption>
</figure>
</center>

SRAM vs DRAM

<table border="2">
<tr>
<th>SRAM</th>
<th>DRAM</th>
</tr>
<tr>
<td>uses an array of 6 transistors for each memory cell</td>
<td>uses a transistor and a capacitor to store each bit of data</td>
</tr>
<tr>
<td>faster data access</td>
<td>slower data access</td>
</tr>
<tr>
<td>consumes more power</td>
<td>consumes less power</td>
</tr>
<tr>
<td>less density/memory per chip</td>
<td>higher density/memory per chip</td>
</tr>
<tr>
<td>higher cost per bit</td>
<td>lower cost per bit</td>
</tr>
<tr>
<td>stores data till power is supplied</td>
<td>stores data for few milliseconds</td>
</tr>
</table>

6.Wide bandgap semiconductors (WBG)
Substrate with wide band gap gives higher tolerance to deep level defects. WBG has emerged as front-running solution to the slow-down in silicon in the high power, high temperature segments. WBG has better conduction and can produce smaller, faster and more efficient devices. Example of WBG includes silicon carbide (SiC) and gallium nitride (GaN)

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/wbg.png" alt="wbg" style="width: 500px;"/>
  <figcaption>Energy Bandgap</figcaption>
</figure>
</center>

WBG materials are has relatively wider energy bandgap compared to conventional silicon. The electronic bandgap is the energy gap between the top of the valence band and the bottom of the conduction band in solid materials. Electrons can jump the gap to the conduction band by means of thermal or optical excitation. Insulators are materials with very large bandgaps, typically greater than 4 electronvolts (eV), and high resistivity. Bandgap allows semiconductor devices to partially conduct and gives semiconductors the ability to switch currents on and off as desired in order to achieve a given electrical function. A higher energy bandgap imparts characteristics that make WBG materials superior to silicon as a semiconductor. WBG-based devices tolerate much higher operating temperatures in a smaller size than the equivalent silicon-based device, enabling previously impossible applications. Silicon possesses a bandgap of 1.1 eV while SiC and GaN have a bandgap of 3.3 eV and 3.4 eV respectively. 

### Radiation Hardened Electronics

#### Space-Grade Virtex-5QV by Xilinx (12 November 2014)
The industry's first high performance rad-hard reconfigurable FPGA for processing-intensive space systems

