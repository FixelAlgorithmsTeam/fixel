---
title: 'Fixel FFT Wizard'
date: 	2018-07-20
author: Fixel Algorithms
layout: post
class:  news
hidden: true
---
![Fixel FFT Wizard Photoshop Plug In][01]

## Background

The [Fourier Transform][02] is one of the most powerful methods to analyze signals / data.  
It is widely used in the [Image Processing][03] world as on of the most used tool for any algorithms developer.  
It has a flavor specialized for [Discrete Signals](https://en.wikipedia.org/wiki/Discrete_time_and_continuous_time) called [Discrete Fourier Transform][4] (DFT) which has a fast and efficient implementation called [Fast Fourier Transform][05] (FFT). 
We won't dive into the math and ideas behind the [DFT][04] but the basic idea is pretty simple.  
For images the [DFT][04] means we can represent data either by values of each pixel in a spatial grid or have equivalent representation which is the energy of periodic 2D signal.  
In [Digital Image Processing][03] there are operations easier to do in the Spatial representation (Image itself) and operations easier to do on the frequency domain.

## Applications

There are many applications for the DFT in Image Processing.  
For instance, [Frequency Separation](https://fstoppers.com/post-production/ultimate-guide-frequency-separation-technique-8699), which is highly popular among Retouchers, can be easily analyzed (Implemented) using DFT.  
Actually many filters (See for instance ) can (Or are) be implemented in the frequency domain which under some conditions is more efficient (Faster).  
for instance have a look at [`Custom Filter`](https://helpx.adobe.com/photoshop-elements/using/filters-1.html#custom_filters) in Adobe Photoshop.

[Affinity Photo](https://affinity.serif.com/en-us/photo/) even use FFT for Denoising (See [FFT Denoise](https://www.youtube.com/watch?v=6wfeMGwcF0c&t=6s), Though it is more periodic pattern suppression, see below).

### Texture / Pattern Suppression

One of the task which is easier to do in the Frequency Domain is Texture / Pattern Suppression.  
Many users use to retouch scanned images or images with periodic pattern they want to remove.  

<br>
![]({{site.baseurl}}/news/images/FixelFFTWizard/FFTFilterRemovePattern.gif){:class="center-img"}
<br>

We won't display full use case of that but you can read and watch many examples in the following resources:

 *  [Use FFT To Reduce Texture](http://www.tipsquirrel.com/use-fft-to-reduce-texture/)
 *  [Lynda - Using an FFT plugin to remove paper texture](https://www.lynda.com/Photoshop-tutorials/Using-FFT-plugin-remove-paper-texture/373087/385421-4.html)  
    Behind a [Paywall](https://en.wikipedia.org/wiki/Paywall).
 *  [Youtube - Photoshop FFT Tutorial](Photoshop FFT Tutorial)
 *  [Youtube - Using FFT Filter for Photoshop to Remove Old Paper Texture](https://www.youtube.com/watch?v=SUqsm9_iCbQ)
 *  [Youtube - FFT Photoshop Action](https://www.youtube.com/watch?v=3jeOsgM5NMs)
 *  [Youtube - Using an FFT Filter to Remove Repeating Patterns](https://www.youtube.com/watch?v=yyox358zIRw&t=232s)
 *  [FFT Filter With Photoshop Action](http://www.skeller.ch/ps/fft_action.php)
 *  [DPReview Forum - FFT filter and Photoshop Action (Tutorial)](https://www.dpreview.com/forums/post/16172756)

All of them has the same basic idea:

 1. Transform the Image into Frequency Domain  
    Apply FFT Filter on an image in Photoshop. The filter will actually be applied on the Luminosity Data of the image.  
    The Plug In will yield 3 Channels image where 2 channels are dedicated to the Amplitude and Phase of the Frequency Domain.
 2. Adjust the Amplitude of the Fourier Transform  
    The user will adjust (**Only**) the Amplitude. Usually by removing energy which fits the unwanted pattern. This is basically applying manual Filtering of the image.
 3. Transform the Adjusted Frequency Data into Luminosity Image  
    Once the Amplitude is adjusted the use will apply the Inverse Transform (IFFT) which will result in Luminosity (Grayscale) image with the removed data according to the user applied filtering.
 4. Merge the Adjusted Luminosity Image with the Color Image of the Original Image  
    Now, the last step, is merging the Luminosity data with the color data of the original image. Usually by changing the blending mode to *Luminosity*.

## Fixel FFT Wizard Photoshop Plug In  

Adobe Photoshop, to our knowledge, has never offered DFT Filter integrated into Photoshop. Hence all solutions were based on Plug In's created by 3rd party.
In some of the above resources you'll find some of those 3rd party solutions (Plug In based) yet usually they are either not working on platforms, not updated or supported.

Yet there is demand for such solutions:

 *  [Adobe Photoshop Forum - Are There Any FFT (Fast Fourier Transform) Plug In's for Photoshop CC?](https://forums.adobe.com/thread/2198154).
 *  [Adobe POhotoshop Feedback Forum - Photoshop: FFT Based Pattern Remover (Filter)](https://feedback.photoshop.com/photoshop_family/topics/fft_based_pattern_remover_as_a_filter).
 *  [Reddit - FFT Filter](https://www.reddit.com/r/photoshop/comments/7npjwk/fftfilter/).
 *  [DPReview Forum - FFT (Fourier Filters) with Photoshop - For Larger Images](https://www.dpreview.com/forums/post/42187590).
 *  [Luminous Landscape - Free Mac Photoshop FFT / IFFT 64-bit Plugins for CC 2015 (OS 10.9+)](http://forum.luminous-landscape.com/index.php?topic=107038.0).
 *  [macOS Photoshop CS5, CS6, CC, CC 2015﻿ FFT / IFFT Filters (64 BIT)](http://djjoofa.com/download/fft_mac_ps_cc_2015).

So we thought we could assist the community with a product which will be supported as a commercial product but **will be offered for free** ([*Pay as You Want*](https://en.wikipedia.org/wiki/Pay_what_you_want)).

### Installation

Once you download Fixel FFT Wizard 

### Use

fds


### System Requirements

#### Operating System

 *  Windows
    Windows 7 x64 (Service Pack 1 Installed), Windows 10 x64.
 *  macOS
    macOS 10.10 and above.

We suggest the Operating System to be updated to its latest build.

#### Host Program

 *  Adobe Photoshop 64 Bit
    Photoshop CS6 64 Bit. Adobe Photoshop CC 2015 64 Bit, Adobe Photoshop CC 2017 64 Bit, Adobe Photoshop CC 2018 64 Bit

It should work on Adobe Photoshop CS5 64 Bit and all CC 64 Bit versions but we never validated it.

#### Hardware

 *  x64 Bit CPU (Intel or AMD) with SSE4 Support.  
    Baiscally any modern CPU created by Intel or AMD since ~2010.


## Summary

The reason we created Fixel FFT Wizard was reading about the need of people for FFT Plug In in Photoshop both for Windows and macOS.  
Moreover, usually the use case were old photos with sentimental significance.  
So we felt we could assist and created Fixel FFT Wizard to support those people who mostly use this for keep their memories with hem.  
Taking all these under consideration we decided to offer Fixel FFT Wizard for free for any user without any constraint on the use.  

At the moment Fixel FFT Wizard is in Public Release Candidate state and once we finalize it we'll put it behind [*Pay as You Want*](https://en.wikipedia.org/wiki/Pay_what_you_want) offer with free option always available.

The download requires Email Address so we could notify you about updates of Fixel FFT Wizard.

We hope you enjoy it and find it useful in your work flow.  
If you do, we'll be happy if you share your cases with us.


<!-- 
<figure>
![test](https://i.imgur.com/mcnGYL4.png){:class="center-img"}
<figcaption>
Try this...
</figcaption>
</figure>
-->

<!-- 
<figure>
<img src="https://i.imgur.com/mcnGYL4.png" alt="Italian Trulli" class="center-img">
<figcaption>
Try this...
</figcaption>
</figure>
-->




## Resources
 *  [Luminosity Mask: The Complete Kickstarter’s Guide](http://fotographee.com/tutorial-image-editing-luminosity-masks/).
 *  [Video - How to Generate the Classic Luminosity Masks Using Mask / Channel Operations (Add, Subtract, Intersect [Multiply])](https://www.youtube.com/watch?v=xvjno4d8uJ8).
 *  [Video - How to Generate the Classic Luminosity Masks Using Calculations (16 Bit Mode)](https://www.youtube.com/watch?v=43JbFIOckrM).
 *  [Video - Selecting Using Luminosity Masks (Using Curve Tool)](https://www.youtube.com/watch?v=la-zWPwjuQw).


<!-- This is commented out -->
[comment]: # (https://fstoppers.com/education/how-create-luminosity-masks-better-retouching-111111 for Luminosity Mask using Calculations.)
[comment]: # (https://www.capturelandscapes.com/introduction-to-luminosity-masks/.)
[comment]: # (https://fstoppers.com/composite/create-seamless-selections-using-luminosity-masks-159068.)
[comment]: # (https://www.psdbox.com/tutorials/complex-masking-using-channels-and-calculations.)
[comment]: # (https://www.youtube.com/watch?v=t3zSUK7KK7c)
[comment]: # (https://www.youtube.com/watch?v=htuf4yaanBI)
[comment]: # (http://play.macprovideo.com/photoshop-102-selection-masking-techniques/12)
[comment]: # (https://www.youtube.com/watch?v=QUkIgdmnBaE)
[comment]: # (http://fotographee.com/luminosity-masks-gradient/ See shortcuts for operations on Masks)
[comment]: # (https://www.youtube.com/watch?v=XGe_YC5dIwI Gamma in Luminosity Masks)

Key Words: [Fixel Algorithms][99], [Fixel][99], [Fixel FFT Wizard][98], [FFT][98], [DFT][98], [FFT Filter][98], [DFT Filter][98], [Photoshop][99], [Plug In][99].


<!-- This is commented out -->
  [01]: {{site.baseurl}}/news/images/FixelFFTWizard/FixelFFTWizardBlogPostIcon.png "Fixel FFT Wizard Photoshop Plug In"
  [02]: https://en.wikipedia.org/wiki/Fourier_transform "Wikipedia - Fourier Transform"
  [03]: https://en.wikipedia.org/wiki/Digital_image_processing "Wikipedia - Digital Image Processing"
  [04]: https://en.wikipedia.org/wiki/Discrete_Fourier_transform "Wikipedia - Discrete Fourier Transform"
  [05]: https://en.wikipedia.org/wiki/Fast_Fourier_transform "Wikipedia - Fast Fourier Transform"
  [88]: {{site.baseurl}}/news/2018/03/luminosity-mask-001 "Luminosity Mask - How Does It (Really) Works?"
  [88]: http://fotographee.com/tutorial-image-editing-luminosity-masks/ "Luminosity Mask: The Complete Kickstarter’s Guide"
  [88]: https://www.youtube.com/watch?v=xvjno4d8uJ8 "How to Generate the Classic Luminosity Masks Using Mask / Channel Operations (Add, Subtract, Intersect [Multiply])"
  [98]: https://fixelalgorithms.co "Fixel FFT Wizard"
  [99]: https://fixelalgorithms.co "Fixel Algorithms"
  [Figure001]: {{site.baseurl}}/news/images/LuminosityMask001/GrayScaleImageGeneration.png "Figure 001 - Extracting Luminosity Channel from RGB Image"
  [Figure002]: {{site.baseurl}}/news/images/LuminosityMask001/MaskGenerator.png "Figure 002 - Mapping Grayscale Image into Luminosity Mask"
  [Figure003]: {{site.baseurl}}/news/images/LuminosityMask001/LuminosityMaskShowCaseAnimated.png "Figure 003 - Luminosity Mask Generation"
  [Figure004]: {{site.baseurl}}/news/images/LuminosityMask001/PhotoshopCurveTool.png "Figure 004 - Photoshop Curve Tool"
  [Figure005]: {{site.baseurl}}/news/images/LuminosityMask001/LuminosityMaskRecipesAnimated.png "Figure 005 - Luminosity Masks Recipes"
