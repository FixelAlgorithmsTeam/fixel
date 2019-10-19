---
title: 'Fixel Detailizer 3 - User Guide'
date: 	2019-04-12
author: Fixel Algorithms
layout: post
class:  news
hidden: true
---
![Fixel Detailizer 3 Multi Scale Detail Booster Adobe Photoshop Plug In][01]

# Fixel Detailizer 3 - Multi Scale Detail Booster Adobe Photoshop Plug In - User Guide

## Introduction

[Fixel Detailizer 3][98] is the 3rd generation of the [Fixel Detailizer][97] family.  
This version adds the following features:

 *	State of The Art Edge Preserving Engine  
	The new engine is built on a global approach to image sharpening (As opposed to *Local Filters*) which reduce the artifacts and halos which are common in sharpening.  
	The new engine gives the user the ability to push farther the sharpening level for *Halos Free* stunning results.
 *	HTML Based UI  
	New UI for optimized and intuitive workflow build around *Adobe Photoshop*'s HTML Panel technology.  
	Unlike classic Plug In's [Fixel Detailizer 3][98] can be used as a side panel with the image always available for peaking, zooming and panning.

This user guide present [Fixel Detailizer 3][98] to the user with simple guidelines on how to use properly to achieve optimal results.

{% include note.html content="The new UI Technology requires Adobe Photoshop CC 2015 and above. For CS6 compatibility the user should use [Fixel Detailizer 2][02]." %}

## Installation
The installation is automated using the Windows and macOS installers.  
Please follow the following steps:

 *	Verify *Adobe Photoshop* is not running.
 *	Unzip the `ZIP` file downloaded on purchase.
 *	Run the installer inside the `ZIP` file:
	*	Windows - *Double Click* `Fixel Detailizer 3 - Windows Installer.exe` installer and follow instruction.  
		The user may be asked for *Administrator* privileges in order to install the Plug In.
	*	macOS - *Double Click* on `Fixel Detailizer - macOS Installer.dmg` disk image and follow instructions.  
		The user may be asked for *Administrator* privileges in order to install the Plug In.
 *	Start *Adobe Photoshop* and launch the UI (See below).

If any issues arise, please refer to [Fixel Detailizer 3 Installation Guide][03].

## Fixel Detailizer 3 UI

This section will show [Fixel Detailizer 3][98] User Interface (UI) and how to use it.

### Launching Detailizer 3 User Interface (Panel)

In order to launch the panel the user should:

 *	Open Photoshop.
 *	In Photoshop menu click on `Window -> Extensions -> Fixel Detailizer 3`.

Once done, the Detailizer 3 UI will present itself:

![][Figure001]{:class="center-img"}

The UI enable simple and intuitive operation of the sharpening process.  
The panel allows the user to interact with the image while adjusting its parameters as it was any other native *Panel* of *Photoshop*.  
Namely you can zoom in, zoom out, do panning, change opacity or visibility while interacting with the panel.

### Main Window UI Components

This section elaborates on each UI Component.

![][Figure002]{:class="center-img"}

As can be seen above, the Panel is composed of 3 main sections:

 *	Plug In Parameters
	*	5 Bands Detail Boosting Sliders.  
		Each slider boost / enhance details of different scale (Size).  
	*	Intensity Slider.  
		Sets the overall intensity of the filter.
	*	Luminosity Mode.  
		When set to `ON` the filter is applied on the *Luminosity Channel* of the image (*Saturation* and *Hue* channels are untouched).
 *	Panel State Elements - *Apply*, *Reset* and *Preview*.  
	In case the `Live View` is disabled one must click on `Apply` to run the filter. The button *Reset* resets the slider into their default values. The *Preview* button toggles between seeing the input image and the output image.
 *	Home Page, Settings, User Guide and About Screen Link Buttons.  
	Home Page opens a browser with the Fixel Website, Settings opens the Settings Window (See below) of the Plug In, User Guide open a web browser with this address and the About icon opens a window with the version string of the Plug In.

The main feature of the Plug In is being able to boost details at different scales.  
Hence the user, at most time, will interact with the 5 upper sliders to adjust the Plug In effect to taste.

### Settings Window Parameters

The settings window is controlling 2 main parameters of the behavior of the Plug In.

| ![][Figure003] 	| ![][Figure004] 	| ![][Figure005] 	|
{:align="center" style="margin: 0px auto;"}

As can be seen above, the parameters are:

 *	Live Mode
	*	`ON` (Default) - The output image is updated with each interaction with the main panel window.  
		For instance, any movement of any slider of the different scales will run the Plug In and render the output.
	*	`OFF` - The output image isn't updated automatically as above. In order to update the output image according to the Plug In's parameters one must click `Apply`.
	*	`Auto` - For images which are less than `4MP` the Plug In will behave as it is in `ON` mode. For images larger than `4MP` it will behave as `OFF`.
 *	Layer Mode
	*	`Active Layer` (Default) - The Plug In will work on the current layer (Given it is a Bit Map / Rasterized Layer) of Photoshop and will adjust it according o parameters.
	*	`Stamp Visible` - The Plug In will create a new layer from the current view and will use it as input image.

The defaults should imitate behavior of a classic plug in's.  
The settings are saved in a user preference file and kept between Photoshop sessions.


## Using Fixel Detailizer 3

This section describe how to use [Fixel Detailizer 3][98].

### Workflow

[Fixel Detailizer 3][98] is designed to give the user the experience of classic Plug In yet within Photoshop main window.  
The recommended usage of Plug In is as following:

 *	Start a new session by launching the Panel.
 *	Interact and adjust its parameters (Move a slider).
 *	Pan & Zoom In / Out to evaluate result.
 *	Tweak parameters to adjust output to taste.
 *	Use `Preview` switch to compare output to input.

When done with the Plug In, continue working on Photoshop.  
The next time the user interacts with the panel it will start a new session.  

{% include note.html content="Changing the active layer or doing any destructive action (Anything but Zooming, Panning, Changing Visibility or Opacity) while working with the Panel will cause it to start a new session." %}

### Effect of Parameters

[Fixel Detailizer 3][98] has few parameters to adjust.  
This section will focus on the ability of [Fixel Detailizer 3][98] (Basically the whole [Fixel Detailizer][97] family) to adjust different scales of details.  
The design was built to imitate *Hi-Fi Equalizer*. Just like equalizer can target different frequencies, [Detailizer][98] can target different scales (Which are equivalent of Frequencies in *Image Processing*).

<!-- Retina Display Support - https://stackoverflow.com/a/19186878/195787 -->
![][Figure006]{: class="center-img" srcset="{{site.baseurl}}/news/images/FixelDetailizer3/FixelDetailizer3SclaesImage001@2x.png 2x"}

In the above figure one could 6 images where one is the *Original Image* and all the other are created by applying sharpening on single scale: Small, MEdium Small, Medium, Medium Large, Large.  
As can be seen, each scale has different effect on the image and targets different size of details.

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure007]{: class="center-img" width="900" height="500"}

The above figure is another example how could one use different scales to enhance different features in the image.  
As can be seen, even when pushed to extreme the Halos are almost non to exist.

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure008]{: class="center-img" width="900" height="600"}

The above image displays another style of images where the scales approach works really well.  
The important advantage of [Fixel Detailizer 3][98] in this context is the minimal amount of artifact although the sharpening is applied with extreme intensity.

### Comparing to Unsharp Mask (USM) - Halos Free Sharpening

As stated above, [Fixel Detailizer 3][98] can create much less artifacts than classic sharpeners.  
This section compares [Fixel Detailizer 3][98] to *Photoshop*'s *Unsharp Mask* (USM).

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure009]{: class="center-img" width="900" height="300"}

The figure above shows the *Original Image*, Image sharpened with *Unsharp Mask* (USM) with `Amount = 250` and `Radius = 15` using Luminosity Blend Mode and [Fixel Detailizer 3][98] with `Medium = 250` with `Luminosity Mode = ON`.  
As could one see above, [Fixel Detailizer 3][98] yields much less artifacts and *Halos*.  
For instance, have a look at the orange petals at the bottom left of the USM Image, the color is brighter due to [Light Halos][04] while there is no such effect on the [Fixel Detailizer 3][98] image.  
Looking at the drops all over the flower one could see both [dark and light Halos][04] on the USM image while no apparent *Halos* on [Fixel Detailizer 3][98] image.  
Of course in the above case values were exaggerated to show the point. Though if someone is after *Pseudo HDR Look* one could see the effectiveness of [Fixel Detailizer 3][98] which creates more natural and artifact & Halos free image.

### Tips & Tricks

There are some simple guidelines to keep in order to maximize the effectiveness of using [Fixel Detailizer 3][98]:

 *	Make sure that the sum of the Boosting Slider doesn't go above ~400. This will ensure limited level of artifacts and halos.
 *	Usually you can push small details boosting level to higher values without any issues.
 *	Intense boosting of Large Details can be used for *Pseudo HDR* effect with much less halos and more natural result then using *HiRaHiAm Sharpening* (High Radius, High Amplitude in USM).
 *	When using high values one might want to use `Luminosity Mode` set to `OFF` in order to prevent reduction in saturation. In most cases one should set `Luminosity Mode` to `OFF` for no color shift and faster execution.
 

## Showcase

This section shows few images with *Before & After* animation. Under each image one could see the settings used to generate result.

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure010]{: class="center-img" width="900" height="600"}
{% include callout.html type="info" content=" `Small = 100`, `Medium Small = 35`, `Medium = 50`, `Medium Large = 95`, `Large = 50`, `Intensity Level = 75`, `Luminosity Mode = OFF`" %}

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure011]{: class="center-img" width="900" height="600"}
{% include callout.html type="info" content=" `Small = 100`, `Medium Small = 250`, `Medium = 160`, `Medium Large = 40`, `Large = 130`, `Intensity Level = 50`, `Luminosity Mode = ON`" %}

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure012]{: class="center-img" width="900" height="600"}
{% include callout.html type="info" content=" `Small = 50`, `Medium Small = 50`, `Medium = 150`, `Medium Large = 100`, `Large = 50`, `Intensity Level = 80`, `Luminosity Mode = OFF`" %}

### Users Showcase  
This section displays images created by users of [Fixel Detailizer 3][98].

{% include image-user.html style="width: 800px; height: 711px;" content="Credit: [Jane](https://www.flickr.com/photos/151740882@N05/47029584231) by Mireille Lannoo" %}




## Summary
[Fixel Detailizer 3][98] is a new generation of sharpeners. While [Fixel Detailizer 2][02] brought the Multi Scale / Frequency to the market surpassing any classic sharpening tool (*High Pass Sharpening*, *Unsharp Mask*, *Smart Sharpen*) [Fixel Detailizer 3][98] brings another jump forward - Edge Preserving Based & Halos Free Sharpening.  
It is intuitive and easy to use (Classic Plug In behavior within Photoshop *Main Window*) yet in utilizes state of the art algorithm which is proprietary to Fixel Algorithms after years of development.  
We listened to the feedback of many of [Fixel Detailizer 2][02] users and used it to create this step forward.  

We hope you'll find it useful as well and hope to hear your feedback to get even better with the upcoming iterations.

{% include important.html content="[Fixel Detailizer 3][98] & [Fixel Detailizer 2][02] have completely different sharpening engines which produce different results. Many find them to work greatly side by side as they find each one better for different images. Hence any user of [Fixel Detailizer 3][98] can get [Fixel Detailizer 2][02] for 50% discount. See *Upgrade Policy* in the respective product pages or *Contact Us*." %}


## Resources
 *  [Fixel Detailizer 3 Product Page][98].
 *  [Fixel Detailizer 3 Installation Guide][03].
 *  [Fixel Detailizer 2 Product Page][02].
 *  [Davide Barranca's Video on *Dark and Light Halos*][04] ([DoubleUSM Plug In][05]).

Key Words: [Fixel Algorithms][99], [Fixel][99], [Fixel Detailizer][98], [Image Enhancement][98], [Image Contrast][98], [Image Sharpening][98], [Image Sharpening][98], [Detail Enhancement][98], [Contrast Enhancement][98], [Detail Boosting][98], [Multi Scale][98], [Multi Frequency][98], [Photoshop][99], [Plug In][99], [Photoshop Plug In][99].


<!-- This is commented out -->
  [01]: {{site.baseurl}}/news/images/FixelDetailizer2Icon150px.png "Fixel Detailizer 3 Icon"
  [02]: {{site.baseurl}}/products/detailizer2 "Fixel Detailizer 2"
  [03]: {{site.baseurl}}/support/fixel-detailizer-3-installation-guide.html "Fixel Detailizer 3 Installation Guide"
  [04]: https://www.youtube.com/watch?v=G-sO5rKc2B0 "DoubleUSM 2 Video - Dark and Light Halos"
  [05]: https://cc-extensions.com/products/doubleusm/ "DoubleUSM 2 Product Page"
  [97]: https://fixelalgorithms.co/products/detailizer/ "Fixel Detailizer - Multi Frequency / Scale Details Booster - Adobe Photoshop Plug In"
  [98]: https://fixelalgorithms.co/products/detailizer3/ "Fixel Detailizer 3 - Multi Frequency / Scale Halos Free Details Booster - Adobe Photoshop Plug In"
  [99]: https://fixelalgorithms.co "Fixel Algorithms"
  [Figure001]: {{site.baseurl}}/news/images/FixelDetailizer3/Fixel Detailizer 3 - User Interface 001.png "Figure 001 - Fixel Detailizer 3 User Interface"
  [Figure002]: {{site.baseurl}}/news/images/FixelDetailizer3/Fixel Detailizer 3 - User Interface 002.png "Figure 002 - Fixel Detailizer 3 User Interface Sections"
  [Figure003]: {{site.baseurl}}/news/images/FixelDetailizer3/Fixel Detailizer 3 - User Interface 003.png "Figure 003 - Fixel Detailizer 3 User Interface (Settings Window)"
  [Figure004]: {{site.baseurl}}/news/images/FixelDetailizer3/Fixel Detailizer 3 - User Interface 004.png "Figure 004 - Fixel Detailizer 3 User Interface (Settings Window)"
  [Figure005]: {{site.baseurl}}/news/images/FixelDetailizer3/Fixel Detailizer 3 - User Interface 005.png "Figure 005 - Fixel Detailizer 3 User Interface (Settings Window)"
  [Figure006]: {{site.baseurl}}/news/images/FixelDetailizer3/FixelDetailizer3SclaesImage001.png "Figure 006 - Demonstration of Different Scales"
  [Figure007]: {{site.baseurl}}/news/images/FixelDetailizer3/FixelDetailizer3SclaesImage002.png "Figure 007 - Demonstration of Different Scales"
  [Figure008]: {{site.baseurl}}/news/images/FixelDetailizer3/FixelDetailizer3SclaesImage003.png "Figure 008 - Demonstration of Different Scales"
  [Figure009]: {{site.baseurl}}/news/images/FixelDetailizer3/FixelDetailizer3USMCompare.png "Figure 009 - Detailizer vs USM (Halos Comparison)"
  [Figure010]: {{site.baseurl}}/news/images/FixelDetailizer3/FixelDetailizer3ShowCase001.png "Figure 010 - Showcase Image"
  [Figure011]: {{site.baseurl}}/news/images/FixelDetailizer3/FixelDetailizer3ShowCase002.png "Figure 011 - Showcase Image"
  [Figure012]: {{site.baseurl}}/news/images/FixelDetailizer3/FixelDetailizer3ShowCase003.png "Figure 012 - Showcase Image"
  