---
title: 	Fixel Detailizer 3 - Multi Scale, Edge Preserving & Halos Free Sharpening
date: 	2019-11-08
author: Fixel Algorithms
layout: post
class:  news
hidden: false
---
![Fixel Detailizer 3 Multi Scale Detail Booster Adobe Photoshop Plug In][01]

{% if layout.type != "post" %}
	Our newest product, [Fixel Detailizer 3][98] is [Fixel][99]'s new generation of Multi Scale Details Enhancer.  
	We're really proud in this one. Mainly because it was really challenging to create algorithms which both state of the art and fast enough for *Real Time* use.
{% endif %}

# Fixel Detailizer 3 - Multi Scale, Edge Preserving & Halos Free Sharpening

## Introduction

Our newest product, [Fixel Detailizer 3][98] is [Fixel][99]'s new generation of Multi Scale Details Enhancer.  
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

Blurring with *Gaussian Blur* creates smoothing of the edge. The extent of the smoothing is the *Radius* parameter of the Gaussian Blur.

{% include note.html content="The `Radius` parameter in the *Gaussian Blur* in Photoshop is actually the Standard Deviation of the [*Gaussian Kernel*](https://en.wikipedia.org/wiki/Gaussian_blur) the filter uses." %}

What about sharpening? Well there is an important intermediate step before the sharpening. It is the subtraction of the blurred image from the original image.

![][Figure003]{:class="center-img"}

As can be seen, the difference (The Details layer as it is commonly named in the *Image Processing* world) has few properties:

 *	Symmetric - It is symmetric to the left left and right in its extent.
 *	Anti Symmetric - Its values are negative mirroring of each other.

{% include note.html content="In the illustration above we added 50% Gray to the Difference in order to see it in the [0, 1] range. This is also what's Photohop's *High Pass Filter* does." %}

Sharpening is all about multiplying this *Difference* by a factor and adding it back to the image.  

![][Figure004]{:class="center-img"}

When added to the image one could see those added bumps compared to the original image. Those bumps are exactly the Halos.  
Say hello to Dark and Light Halos. The generating forces of the Unsharp Mask. You can actually see the effect of the Radius Parameter (Extent of the roll off of the Halo) and the Amplitude Parameter (The height of the Halo).  
Some will find the effect to be positively contributing. In some cases indeed it is.  
The problem is there is another parameter we don't control which plays a role here, the Edge itself.  The more contrast in the edge the more prominent the effect is.

Real world edges are blurred to begin with (This is has to do with the [Sampling Theorem](https://en.wikipedia.org/wiki/Nyquist%E2%80%93Shannon_sampling_theorem), but that's a story for another day).

![][Figure005]{:class="center-img"}

In real world image the effect looks much less satisfactory. The reason is the roll on isn't as sharp as in the example above. It seems the peak of the halo gets too late.  
But in both cases we get values which reach outside of the boundary of the expected values. This is the concept of Halos. This is a property of all Sharpeners which are originated from classic blur filters (Called *Spatially Invariant Linear Filters*).  
They just average data form both sides of an edge while conceptually we'd prefer to average pixels on the left with pixels similar to them, on the left and the same holds for the other side.

What really bothers us about Halos is their *Roll Off*. The part were after the overshooting they get back to the local value. We would like the Roll Off not to happen.  
Instead of roll off, we'd like small over shoot and slight increase of the values. So bright gets brighter and dark get darker.

### Edge Preserving Blurring & Sharpening

So, we saw the problem with Gaussian Blur based filters. They all mix pixel values from both sides of the edge. So Image Processing researchers in the late 90's started thinking about solving this.  
In 1998 there was an article named - [Carlo Tomasi, Roberto Manduchi, Bilateral Filtering for Gray and Color Images](https://en.wikipedia.org/wiki/Bilateral_filter) (Roberto Manduchi was in the Interactive Media Group of Apple).  
It is the source of the *Surface Blur* we have in Photoshop. Basically a local filter which doesn't blur across edges.  

What happens if we use it on the same cases as above? Let's see.

![][Figure006]{:class="center-img"}

No blurring? Indeed. It didn't average pixels on both side and since each side is flat, nothing happened. Can you think what would have happened if we had some noise there?  
The Bilateral Filter would do the perfect thing to do, average all pixels which are similar, don't mix with those who are not. Basically, this is what a good denoiser would have done.

![][Figure007]{:class="center-img"}

No surprise here. If no blurring the difference is none.

![][Figure008]{:class="center-img"}

It is like the *Bilateral Filter* understood the image is sharp to perfection and did nothing.

![][Figure009]{:class="center-img"}

In the real world case we can see that the *Bilateral Filter* kept the Halos in a lower level. This is what we want, sharpener with lower level of Halos!  
Could we do better?

{% include note.html content="Those with sharp eyes will notice some artifact just in the middle of the edge. This is called the *Gradient Reversal* artifact of the *Bilateral Filter*." %}

It was 1998, so we certainly can do better. [Detailizer 3][98] uses a different concept. While those filters are *Local*, taking decisions based on a local, limited in size, area of pixels [Detailizer 3][98] looks on the image in a global manner.  
Without getting into Math which will make everyone sad, being global let the filter spread bad things among all pixels. So it yields even lower level of Halos.

Let's have a look on what will [Detailizer 3][98] do.

![][Figure010]{:class="center-img"}

No one crosses to other side. Just like *Bilateral Filter*.

{% include note.html content="If you look closely you see the brighter pixels got a bit darker while darker pixels got a little brighter. Nice thing, due to global optimization, all got the same value. So no artifact." %}

![][Figure011]{:class="center-img"}

*Copy & Paste*: No surprise here. If no blurring the difference is none.

![][Figure012]{:class="center-img"}

OK, when the Edge is perfect it does the right thing to do - Nothing. Just like the *Bilateral Filter*. So, why not take the *Bilateral Filter*?  
Let's have a look on the real world case.

{% include note.html content="Same as before. Bright got a little brighter and dark got a little darker. But all pixels with the same value. No artifact. Just higher contrast." %}

![][Figure013]{:class="center-img"}

Here it is. Perfect! Not only we have no Halos it indeed do a real sharpening. The slope of edge get sharper, the contrast between all the flat area of both sides is increased.

In Detailizer we created our own *Global Edge Preserving Smoothing Filter*. It allows us control the height of the Halo and its Roll Off.  
So when we set to low height and no roll off we get the result above. To show you the nice balance, let's have a case where we give higher Halo but still no *Roll Off*.

{% include note.html content="Remember the *Gradient Reversal* of the *Bilateral Filter*? Gone!" %}

![][Figure014]{:class="center-img"}

Nice, isn't it? We increased the contrast between those 2 flat zones without the artifact of the *Roll Off* of the *Bilateral Filter* or the *Gaussian Filter*.  
So we have made progress in the last 20 years, haven't we? This is exactly what we want. Slight overshoot but no *Roll Off*.  
Since [Detailizer 3][98] works globally it "understands" those are flat zone on a side of an edge, so shrink the edge blurring and increase the local contrast.  

We have accomplished what we asked for sharpening!

## Multi Scale Sharpening

When we say Multi Scale Sharpening, what do we mean?  
In a layman words, it means looking on the image at different resolutions / scales.  
For instance, given an image at a given size, the Multi Scale approach suggests processing it at its original size and half of that and half of that and so on...  
Well, at least it is one way to look at it.  

![Fixel Detailizer Multi Scale][Figure015]{:class="center-img"}

The approaches to implement Multi Scale Analysis are endless.  
Yet in the Image Processing World it all started with the [Image Pyramid][05].  
Later came the Filter Banks and the the [Wavelet Transform][06].  

In [Detailizer 2][02] our guideline was quality hence we used [Undecimated Wavelet Transform][06] which yields less artifacts ([Halos / Ringing][07]) than the classic Wavelets.  
Yet [Detailizer 3][98] required extending this idea farther as we used a blurring approch which is different.  
This approach assisted us taking quality into next level though it also costs in more computational time. No free lunch here.


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
  [05]: https://en.wikipedia.org/wiki/Pyramid_(image_processing)
  [06]: https://en.wikipedia.org/wiki/Stationary_wavelet_transform
  [07]: https://en.wikipedia.org/wiki/Ringing_artifacts
  [98]: https://fixelalgorithms.co/products/detailizer3/ "Fixel Detailizer 3 - Multi Frequency / Scale Halos Free Details Booster - Adobe Photoshop Plug In"
  [99]: https://fixelalgorithms.co "Fixel Algorithms"
  [Figure001]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0001.png "Figure 001 - Reference Image"
  [Figure002]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0002.png "Figure 002 - Blurring Effect"
  [Figure003]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0003.png "Figure 003 - The Difference"
  [Figure004]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0004.png "Figure 004 - The Sharpened Image"
  [Figure005]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0005.png "Figure 005 - The Real World Sharpened Image"
  [Figure006]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0006.png "Figure 006 - Blurring Effect - Bilateral Filter"
  [Figure007]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0007.png "Figure 007 - The Difference - Bilateral Filter"
  [Figure008]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0008.png "Figure 008 - The Sharpened Image - Bilateral Filter"
  [Figure009]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0009.png "Figure 009 - The Real World Sharpened Image - Bilateral Filter"
  [Figure010]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0010.png "Figure 010 - Blurring Effect - Fixel Detailizer 3"
  [Figure011]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0011.png "Figure 011 - The Difference - Fixel Detailizer 3"
  [Figure012]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0012.png "Figure 012 - The Sharpened Image - Fixel Detailizer 3"
  [Figure013]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0013.png "Figure 013 - The Real World Sharpened Image - Fixel Detailizer 3"
  [Figure014]: {{site.baseurl}}/news/images/FixelDetailizer3/BlogPost0014.png "Figure 013 - The Real World Sharpened Image - Fixel Detailizer 3 - Higher Overshoot, No Roll Off"
  [Figure015]: {{site.baseurl}}/news/images/FixelDetailizerScales004.png "Fixel Detailizer Multi Scale"
  
