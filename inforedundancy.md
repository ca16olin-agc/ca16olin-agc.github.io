---
layout: page
title: Information Redundancy
permalink: /faulttolerance/inforedundancy
---

An improvement on Parity Bits is the Hamming Code. This code uses parity bits too, but in a way that allows detection of up to two errors and correction of up to one error. Hamming Code is a seven bit signal, with the first four bits transmitting data and the last three bits acting as an accuracy check. The Parity bits would be one or zero as to make the statements below correct. For example, you have a 4 bit binary signal:


	Signal: A0 ,A1 ,A2 ,A3 = 0 1 1 0		

	Parity Bits: X, Y, Z


	A0 ⊕ A1 ⊕ A2 ⊕ X = 0

	A0 ⊕ A2 ⊕ A3 ⊕ Y = 0

	A0 ⊕ A3 ⊕ A4 ⊕ Z = 0


In this case, X would be 0, Y would be 1, and Z would be 1 in order for the statements to be true, and the full signal would look like 0 1 1 0 0 1 1.


The receiver receives the signal, and double checks the equations above. If there is only one error, the system can locate the error going backwards through the failed equations. With complicated logic using xor gates, this is also able to correct single errors. This makes the Hamming Code much more useful.

![Hamming Example](/images/hamming_ex2.png "Hamming Example")