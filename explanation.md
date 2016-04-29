---
layout: page
title: How does it work?
permalink: /explanation/
---
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

![Flow Chart]({{ site.baseurl }}/images/exp_flowchart.PNG "Flow Chart")

### Discrete Cosine Transform (DCT)
* Convert signal into elementary frequency components
* Similar to discrete Fourier Transform using only real numbers
* Transform an image form the spatial domain to the frequency domain
* Can approximate lines well with fewer coefficients

#### DCT II
\\[X_k =
 \sum_{n=0}^{N-1} x_n \cos \left[\frac{\pi}{N} \left(n+\frac{1}{2}\right) k \right] \quad \quad k = 0, \dots, N-1\\]

 In matlab, x0 is multiplied by $$1/√2$$ and the resulting matrix is multiplied by scale factor of $$\sqrt{2/N}$$ to make the matrix orthogonal for normalization. [7]


#### Why DCT?
<img src="{{ site.baseurl }}/images/dctvsfft.gif">

DCT is similar to the Fast Fourier Transform (FFT), but can approximate lines well with fewer coefficients. [4]

