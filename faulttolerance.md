---
layout: page
title: Fault Tolerance
permalink: /faulttolerance
---

We have discovered that the harsh conditions of space may mess up computer operations and generate errors. In this part of the website, we discuss three different architectures that can counter error.

<a href = '{{ site.baseurl }}/faulttolerance/inforedundancy'>Information Redundancy</a>

<a href = '{{ site.baseurl }}/faulttolerance/structuralredundancy'>Structural Redundancy</a>

<a href = '{{ site.baseurl }}/faulttolerance/timeredundancy'>Time Redundancy</a>

It is important to realize that these techniques can be used individually and together. However, each method has costs and benefits. For example, the structural redundancy method has no time penalty, as we do not have to generate more bits to store information, or run the process multiple times. However, the area cost is massive. Another example would be time redundancy, which has low area cost but very high time cost.