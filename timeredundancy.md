---
layout: page
title: Time Redundancy
permalink: /faulttolerance/timeredundancy
---

- Computations or data transmissions are repeated at different points in time and the result is compared to a stored copy of the previous result
- Low hardware and software overhead at the expense of time
- Implemented in applications where time is less valuable than hardware
- Effective against transient faults, which are the majority of hardware faults
- Can distinguish between transient and permanent faults
- Respond to failures by rolling back the execution and re-executing the program (to reduce the inefficiency, checkpoints are implemented)



## Transient Fault Detection

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/transientfaultdetection.png" alt="Trasient Fault Detection" style="width: 500px;"/>
  <figcaption>Trasient Fault Detection (Laprie, Kanoon, Romano, Fault tolerant design techniques)</figcaption>
</figure>
</center>



## Permanent Fault Detection
- Minimal extra hardware implemented

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/permanentfaultdetection.png" alt="Permanent Fault Detection" style="width: 500px;"/>
  <figcaption>Permanent Fault Detection (Laprie, Kanoon, Romano, Fault tolerant design techniques)</figcaption>
</figure>
</center>


### Coding Schemes
- Time redundancy methods differ based on the coding schemes
- Error correction can be implemented by repeating the operation >3 times and voting over the results

#### Complementing
- Requires circuit to implement self-dual function

##### Self- duality
fd (dual of f) is obtained by replacing AND to OR, OR to AND, 1 to 0 and 0 to 1

f = x1x'2 + x3  →  f' = (x'1 + x2) x'3  →  fd = (x1 + x'2) x3

self-duality: fd = f

- Good for stuck-at type fault detection
- The circuit has fault if the output to the input assignment (x1, x2, ... xn) are equal to the next input assignment (x'1, x'2, ... x'n)

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/alternatinglogic.png" alt="Alternating Logic" style="width: 500px;"/>
  <figcaption>Alternating Logic (Elena Dubrova, Design of Fault Tolerant Systems)</figcaption>
</figure>
</center>


#### Recomputing with shifted operands (RESO)
- Good for fault detection in ALUs with bit slicing
- Encoder: Left Shift
- Decoder: Right Shift
- Requires extra 1 bit is for left shift operation

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/reso.png" alt="RESO" style="width: 500px;"/>
  <figcaption>RESO (Elena Dubrova, Design of Fault Tolerant Systems)</figcaption>
</figure>
</center>

Assume ith bit is erroneus. The first computation at t0 will result in output with error in ith bit. The second computation at t1 will result in output error in (i-1)th bit due to the left shift encoding. After right shift decoding, the two outputs will disagree at ith and (i-1)th bit.


#### Recomputing with swapped operands (RESWO)
- Good for fault detection in ALUs with bit slicing
- Swaps upper and lower halves of the operands

<center>	 
<figure>
  <img src="{{ site.baseurl }}/images/reswo.png" alt="RESWO" style="width: 500px;"/>
  <figcaption>RESWO (Elena Dubrova, Design of Fault Tolerant Systems)</figcaption>
</figure>
</center>