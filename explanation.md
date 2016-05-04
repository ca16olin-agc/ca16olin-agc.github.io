---
layout: page
title: How does it work?
permalink: /explanation/
---
<center><script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script></center>

![Flow Chart]({{ site.baseurl }}/images/exp_flowchart.PNG "Flow Chart")

Encoding message into image
One possible way for encoding message in image is by replacing values in the image with the values of the message. The values of the message can be obtained by <a href = 'http://kr.mathworks.com/help/matlab/matlab_prog/converting-from-string-to-numeric.html'>converting characters to numeric values</a>  using the double function in matlab. Replacing the values of the image directly will result in obvious change in the encoded image. Therefore, we transformed the image using discrete cosine transform (DCT) to convert the image from spatial domain to frequency domain. In the frequency domain, we can replace out the middle range values with the values of the message without making obvious change to the image. Replacing the high and low frequency will result in more obvious change in the image. More explanation is given in our <a href = 'http://sigsys16steganography.github.io/image_processing/'>image processing tab</a> . After replacing the values, we applied inverse discrete cosine transform (IDCT) to change back the image from frequency domain to spatial domain and get the encoded image. 

Decoding encoded image to generate the message
We can apply IDCT and get the values in the encoded area. Then, we convert the values to characters to get the message.

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
<center><img src="{{ site.baseurl }}/images/dctvsfft.gif"></center>

DCT is similar to the Fast Fourier Transform (FFT), but can approximate lines well with fewer coefficients. [4]

