---
title: 'Fixel Detailizer 3 - Multi Scale, Edge Preserving & Halos Free Sharpening'
date: 	2019-04-26
author: Fixel Algorithms
layout: post
class:  news
hidden: true
---
![Fixel Detailizer 3 Multi Scale Detail Booster Adobe Photoshop Plug In][01]

# Fixel Detailizer 3 - Multi Scale, Edge Preserving & Halos Free Sharpening

## Introduction

[Fixel Detailizer 3][98] is [Fixel][99]'s new generation of Multi Scale Details Enhancer.  
We're really proud in this one. Mainly because it was really challenging to create algorithms which both state of the art and fast enough for *Real Time* use.

[Detalizer 3][98] main features are:

 *	Multi Scale Details Boosting  
	[Detailizer 3][98] works in a Multi Scale manner. Namely it analyze the image in different scales.  
	Namely one tool to handle small, medium and large details.
 *	Edge Preserving Halos Free Sharpening  
	One of the artifacts of sharpening is Halos. Well, no more. [Detailizer 3][98] can sharpen without creating any artifact.
 *	5 Bands / Scales to Set Details Amplification and Enhancement Level  
	The user can set the amplification level of each detail scale as easy as setting amplification level for different bands in *Hi-Fi Equalizer*.
 *	Intuitive & User Friendly
	[Detailizer 3][98]'s UI was rebuilt according to [Detailizer 2][02]'s users feedback. It uses Photoshop CC Native Panel (HTML Panel) API to allow the user simple, intuitive and effective work flow.
 *	32 Bit Internal Processing  
	All the *Math* is done in `32 Bit` precision to avoid clipping, quantization and histogram distortions effects.
 *	`8`, `16` and `32 Bit` Mode Support   
	The filter supports `8`, `16` and `32 Bit` Mode (RGB & Grayscale) including support for HDR Photography

We, at [Fixel Algorithms][99], thought it would be a good idea to tell you some behind the scene details about sharpening and Detailizer.  
It will be a little technical but easy to read and understand. If we made something too technical, please notify us and we'll try make it clearer.

## Edge Preserving Sharpening

This section will discuss the following:

 *	Classic Sharpening Methods & Limitation (Halos)  
	When we write classic we mean Unsharp Mask, High Pass and to some extent Smart Sharpen in Photoshop.  
	They have the main properties of being *Linear* and *Spatially Invariant*. This means they have **no ability** to adapt according to the image itself (Locally or globally).  
	Yet this property also makes them simple and fast. Really fast on modern CPU's.
 *	Modern Edge Preserving Sharpening Methods  
	Edge Preserving Filters are inherently different from the *Classic Sharpeners*. They adapt to the information they "see".  
	While the date back to the early 90's there have been major progress in this field. Modern algorithms do amazing work.  

But before we dive into them deeper, let's us tell you a wide known secret - **All sharpeners are born as blurring filters**.  
So in order to understand classic sharpeners vs. edge preserving sharpeners we have to look into classic blurring vs. edge preserving blurring.

We'll do the analysis using a simple generated image which emulates edge in image.

![][Figure001]{:class="center-img"}

### Classic Blurring & Sharpening

Before diving into the analysis we must refer you to a great (Funny!) video about sharpening made by our partner [Davide Barranca](https://cc-extensions.com/) - [Double USM 2 Panel for Adobe Photoshop](https://www.youtube.com/watch?v=G-sO5rKc2B0).  
This video will explain some idea in a way only a video and Davide can. Really wort watching.

The sharpening procedure starts with blurring. When one says blurring in the context of Image Processing it usually means *Gaussian Blur*.  
Indeed it holds in our case as well. Actually in Photoshop both *Unsharp Mask* and *High Pass Filter* are built upon *Gaussian Blur* blurring. Really!  

Let's see how it works. So we said sharpening starts with blurring. So what happens when we blur?

![][Figure002]{:class="center-img"}

### Edge Preserving Blurring & Sharpening



## Multi Scale Sharpening


As can be seen above, the Panel is composed of 3 Tabs for 3 Filters.  
By default the first Filter / Tab presented in PixelGear 2 panel is SkinGear. If you want to use EdgeGear or ToneGear, simply click them at the bottom of the panel.

### Fixel 5 Bands

To start the retouch process, you need first to create a selection of the skin areas.

Click on the `Color Range` button to open the Color Range dialog box.


## Summary
[Fixel Detailizer 3][98] is a new generation of sharpeners. While [Fixel Detailizer 2][02] brought the Multi Scale / Frequency to the market surpassing any classic sharpening tool (High Pass Sharpening, Unsharp Mask, Smart sharpen) [Fixel Detailizer 3][98] brings another jump forward - Edge Preserving Based & Halos Free Sharpening.  
It is intuitive and easy to use yet in utilizes state of the art algorithm which is proprietary to Fixel Algorithms after years of development.  
We listened to the feedback of many of [Fixel Detailizer 2][02] users and used it to create this move forward step.  

We hope you'll find it useful as well and hope to hear your feedback to get even better with the upcoming iterations.


## Resources
 *  [Fixel Detailizer 3 Product Page][98].
 *  [Fixel Detailizer 3 Installation Guide][03].
 *  [Fixel Detailizer 3 User Guide][04].

Key Words: [Fixel Algorithms][99], [Fixel][99], [Fixel Detailizer][98], [Image Enhancement][98], [Image Contrast][98], [Image Sharpening][98], [Image Sharpening][98], [Detail Enhancement][98], [Contrast Enhancement][98], [Detail Boosting][98], [Multi Scale][98], [Multi Frequency][98], [Photoshop][99], [Plug In][99], [Photoshop Plug In][99].


<!-- This is commented out -->
  [01]: {{site.baseurl}}/news/images/FixelDetailizer3/Fixel Detailizer 3 Logo.png "Fixel Detailizer 3 Icon"
  [02]: {{site.baseurl}}/products/detailizer2 "Fixel Detailizer 2"
  [03]: {{site.baseurl}}/support/fixel-detailizer-3-installation-guide.html "Fixel Detailizer 3 Installation Guide"
  [04]: {{site.baseurl}}/news/2019/04/fixel-detailizer-3-user-guide "Fixel Detailizer 3 User Guide"
  [98]: https://fixelalgorithms.co/products/detailizer3/ "Fixel Detailizer 3 - Multi Frequency / Scale Halos Free Details Booster - Adobe Photoshop Plug In"
  [99]: https://fixelalgorithms.co "Fixel Algorithms"
  [Figure001]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost001.png "Figure 001 - Reference Image"
  [Figure001]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost002.png "Figure 002 - Blurring Effect"
  
