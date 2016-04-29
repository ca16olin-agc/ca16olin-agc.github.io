---
layout: page
title: Image Processing
permalink: /image_processing/
---

##Image as Two Dimensional Signals

Images can be thought of as discrete two dimensional signals, which are linear combinations of eigenfunctions (cosine, sine, or complex exponentials). Thus, taking discrete fourier transform of an image can be thought of as putting together the coefficients of the eigenfunctions on each row and each column. Images can be altered using the similar techniques used for one dimensional signals. That is, taking fourier transformation, altering the signal in frequency domain, and taking inverse fourier transform.

### Fourier Transform Pair in Images

The fourier transform pairs in one dimension can be extended to two dimensions, or images. Just to remind ourselves of some of the fourier transform pairs, Box functions become Sinc functions, Delta functions become just a constant, and Cosine functions become two Delta functions in the frequency domain when Fourier transformed. 

Below are the images equivalent to Delta, Cosine, Sinc, and Box functions. To briefly explain, Delta function in two dimensions is an image where all but one pixel in the middle has maximum brightness, Cosine and Sinc functions in two dimensions are images where the pixel brightness in horizontal and vertical direction alternate in Cosine and Sinc-wise manner from minimum and maximum brightness, and the Box function in two dimensions is an image where the pixel brightness is zero except for the square in the middle.

Taking the fourier transform of those images result in images which are two dimensional equivalent of the fourier transform pairs for the Delta, Cosine, Sinc and Box functions. 

![Fourier Transform pairs in Two Dimensions]({{ site.baseurl }}/images/fourier_transform_pair.PNG "Fourier Transform Pairs in Two Dimensions")

The fourier transform pair of the:

1. Delta function is just an white image (constant)
2. Cosine function is an image with four brightest spots (two delta functions each in horizontal and vertical direction)
3. Sinc function is an image with bright square in the middle (Box function)
4. Box function is an image equivalent to Sinc function.  


### Filters in Images

Altering an image in a way we run signals through filters can be done in two different ways. 

First is through convolving the image with an kernel that mimics the impulse response of the filters for one dimensional signals.
Second is through multiplying (or directly altering) the fourier transformed image to a filter.

Figure below shows examples of how an image gets altered when filtered through low pass and high pass filters.
Low pass filter keeps only the low frequency component of the image (mid-sections of the transformed image), and throws away all the high frequency components, while high pass filter keeps the opposite.

Image that went through low pass filter blurs the image, which is the "general trend" of the image contour.
On the other hand, the high pass filter works like an edge detector. 
(Edge = sharp transition of the pixel values = high frequency component)

![Image Filtering]({{ site.baseurl }}/images/fourier_filter.PNG "Image Filtering")