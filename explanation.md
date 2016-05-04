---
layout: page
title: How does it work?
permalink: /explanation/
---
<center><script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script></center>

![Flow Chart]({{ site.baseurl }}/images/exp_flowchart.PNG "Flow Chart")

#### Encoding message into image
One possible way for encoding message in image is by replacing values in the image with the values of the message. The values of the message can be obtained by <a href = 'http://kr.mathworks.com/help/matlab/matlab_prog/converting-from-string-to-numeric.html'>converting characters to numeric values</a>  using the double function in matlab. Replacing the values of the image directly will result in obvious change in the encoded image. Therefore, we transformed the image using discrete cosine transform (DCT) to convert the image from spatial domain to frequency domain. In the frequency domain, we can replace out the middle range values with the values of the message without making obvious change to the image. Replacing the high and low frequency will result in more obvious change in the image. More explanation is given in our <a href = 'http://sigsys16steganography.github.io/image_processing/'>image processing tab</a> . After replacing the values, we applied inverse discrete cosine transform (IDCT) to change back the image from frequency domain to spatial domain and get the encoded image. 

#### Decoding encoded image to generate the message
We can apply IDCT and get the values in the encoded area. Then, we convert the values to characters to get the message.

#### Example
<center>![Example Cat Image]({{ site.baseurl }}/images/catdemo.png "Example Cat Image")</center>

<center><i>Example of hiding message to an image<i></center>

Above shows an example of encoding message to an image. The first photo is the original image, and below is the fourier transformed version of the image. In order to create least amount of damage to the image, we selected mid-frequency range to hide the information. Altering low frequency component of the image will distort the information showing the general trend, while altering high frequency component will distort the sharp transition points of the image. Thus, selecting a mid-range frequency makes sense.

After encoding the message to the fourier transformed image, we invert it back to original spatial domain, giving the image with encoded message on the top right. You see the image has a little bit of distortion, but is not so much different from the original image, showing successful hiding of information.

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

