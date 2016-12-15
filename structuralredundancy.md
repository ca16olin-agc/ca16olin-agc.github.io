---
layout: page
title: Structural Redundancy
permalink: /faulttolerance/structuralredundancy
---

Structural redundancy is the idea that hardware can be replicated, such that if one device fails, a back-up can take its place. This can be significantly more expensive than the other methods of time and information redundancy because the same hardware may need to be copied several times, in order to make the device robust to errors.

This section will discuss the different ways that structural redundancy can be implemented in a computer.

## N-Modular Redundancy
Any module, such as an ALU or a multiplexer, can be copied multiple times and can run in parallel to each other. Ideally, the outputs of these devices are the same, but environmental conditions can cause random bit-flips or corrupted data. N-modular redundancy seeks to mitigate this by passing the outputs from the parallel modules into a voter.

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/triple_structure.png" alt="Triple redundancy" style="width: 500px;"/>
  <figcaption>Dubrova, Elena. Fault-tolerant design. Springer, 2013.</figcaption>
</figure>
</center>

If the error rate for a particular device is 1%, the error rate for multiple devices to fail at the same time would be significantly lower. Thus, the voter outputs the majority of the bits that have been outputted by the parallel modules. For instance, if there are 3 modules that output single-bit values of 1, 1, and 0, the voter will return 1, which at least two of the three modules voted for.

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/voter.jpg" alt="Voter circuit" style="width: 300px;"/>
  <figcaption>http://www.labbookpages.co.uk/teaching/evoHW/lab2.html</figcaption>
</figure>
</center>

## Non-Perfect Voters
However, voting is sometimes imperfect. Although this is particularly rare, since voters are generally comprised of simple gates, new mechanisms are required if the error rate needs to be kept low. Similar to the fact that the modules can be replicated, the voters can also be replicated, so that if one voter fails, the majority of outputs will return the correct value.

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/tmr_voting.png" alt="Triple the voters" style="width: 500px;"/>
  <figcaption>Dubrova, Elena. Fault-tolerant design. Springer, 2013.</figcaption>
</figure>
</center>

## Duplication With Comparison
Although N-modular redundancy can be extremely tolerant of errors, it can be quite expensive. It also only masks the error, so it doesn't alert the rest of the system when one of the modules has outputted an unexpected value.

Duplication with comparison is one way of reducing the number of modules required and throws an error signal once an error occurs. In this case, the module only needs to be copied once. Both of the outputs are compared to each other, and if there is a mismatch, then the error signal flags true. However, this does nothing to change the system, if an error actually occurs.

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/duplication_comparison.png" alt="Duplication With Comparison" style="width: 500px;"/>
  <figcaption>Dubrova, Elena. Fault-tolerant design. Springer, 2013.</figcaption>
</figure>
</center>

## Standby Redundancy
In order to actively correct for errors, standby redundancy is built with N modules, only one of which can be active at a time. A fault detection unit (FD) is used to detect if there has been some error, and this can take on many different forms. For instance, the FD unit could be comparing some on-board calculation with a signal transmitted from a ground station. A multiplexer or switch will point to the first module and move to the second one, if the first one fails. This process continues until all n devices have been exhausted, at which point, the entire system fails.

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/standby_redundancy.png" alt="Standby redundancy" style="width: 500px;"/>
  <figcaption>Dubrova, Elena. Fault-tolerant design. Springer, 2013.</figcaption>
</figure>
</center>

The biggeest advantage of this system is that it consumes very little energy, since all of the inactive modules can be turned off. Unlike the systems described previously, not all of the modules need to be running at the same time.

## Pair-and-a-Spare
This structure combines the duplication with comparison method and the standby redundancy method to further reduce errors. Instead of only one module being active at a time, two of them are enabled. The switch selects two working modules and compares those outputs, but if an error has occurred, the signal is passed back to the switch, which then looks at the currently active fault detection units to decide which of the two modules needs to be removed.

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/pairandasquare.png" alt="Pair-and-a-spare" style="width: 500px;"/>
  <figcaption>Dubrova, Elena. Fault-tolerant design. Springer, 2013.</figcaption>
</figure>
</center>

Due to the added stage of comparison after the switch, this system is more sensitive to error than just the standby redundancy method. However, it needs at least two working modules for everything to run correctly.

## Self-Purging
This is a spin on the N-modular redundancy method, such that the output of the voter is compared to the output of each of the modules. If one of the modules does not match up with the voter output, then that module is switched off and not even passed into the voter to begin with. As a result, malfunctioning modules do not have an effect on the voting outcome.

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/self_purging.png" alt="Self-purging" style="width: 500px;"/>
  <figcaption>Dubrova, Elena. Fault-tolerant design. Springer, 2013.</figcaption>
</figure>
</center>
