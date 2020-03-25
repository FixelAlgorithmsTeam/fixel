---
title:  Fixel Zone Selector 2 - User Guide
date: 	2020-04-05
author: Fixel Algorithms
layout: post
class:  news
hidden: true
---
![Fixel Zone Selector 2 - Simple, Smart & Effective Zone System Luminosity Masks Generator Plug In for Adobe Photoshop][01]

# Fixel Zone Selector 2 - Simple, Smart & Effective Zone System Luminosity Masks Generator Plug In for Adobe Photoshop - User Guide

## Introduction

[Fixel Zone Selector 2][98] is a Luminosity Mask generator. It is implemented as a Plug In with the highest quality and accuracy in mind.  
The user experience was designed to mimic Ansel Adams's Zone System by dividing the tonal range into 11 zones. The user is able to generate a mask by any combination of the zones.  

[Fixel Zone Selector 2][98] is the 2nd generation of the [Fixel Zone Selector][97] family.  
This version adds the following features:

 *	Updated Algorithm  
	We have tweaked the algorithm to produce higher quality mask where we started with the highest quality to begin with.
 *	Source Channel Selection  
	The user can select the source channel for the mask: `Luminosity`, `R`, `G`, `B` or `Saturation`.  
	This allows farther ability to pin point the area / tonal range to select.
 *	Luminosity Mask Contrast (Focus / Roll Off Smoothness)  
	Control the smoothness of the generated mask. Higher contrast means sharper boundaries (In tonal range) between selected and not selected tonal zones.
 *	Auto Tone  
	Automatically stretches the mask to capture full dynamic range of mask.
 *	HTML Based UI  
	New UI for optimized and intuitive workflow build around *Adobe Photoshop*'s HTML Panel technology.  
	Unlike classic Plug In's [Fixel Zone Selector 2][98] can be used as a side panel with the image always available for peaking, zooming and panning.  
	The new UI also adds 7 presets to allow user have more efficient workflow. One of the presets (The middle) is user configurable.

This user guide presents [Fixel Zone Selector 2][98] to the user with simple guidelines on how to use properly to achieve optimal results.

{% include note.html content="The new UI Technology requires Adobe Photoshop CC 2017 and above. For CS6 compatibility the user should use [Fixel Zone Selector 1][02]." %}

## Installation
The installation is automated using the Windows and macOS installers.  
Please follow the following steps:

 *	Verify *Adobe Photoshop* is not running.
 *	Unzip the `ZIP` file downloaded on purchase.
 *	Run the installer inside the `ZIP` file:
	*	Windows - *Double Click* `Fixel Zone Selector 2 - Windows Installer.exe` installer and follow instruction.  
		The user may be asked for *Administrator* privileges in order to install the Plug In.
	*	macOS - *Double Click* on `Fixel Zone Selector - macOS Installer.dmg` disk image and follow instructions.  
		The user may be asked for *Administrator* privileges in order to install the Plug In.
 *	Start *Adobe Photoshop* and launch the UI by going `Window -> Extensions -> Fixel Zone Selector 2` (See below).

If any issue arises, please refer to [Fixel Zone Selector 2 Installation Guide][03].

## Fixel Zone Selector 2 UI

This section will show [Fixel Zone Selector 2][98] User Interface (UI) and how to use it.

### Launching Zone Selector 2 User Interface (Panel)

In order to launch the panel the user should:

 *	Open Photoshop.
 *	In Photoshop menu click on `Window -> Extensions -> Fixel Zone Selector 2`.

Once done, the Zone Selector 2 UI will present itself:

![][Figure001]{:class="center-img"}

The UI enable simple and intuitive operation of the edge enhancement process.  
The panel allows the user to interact with the image while adjusting its parameters as it was any other native *Panel* of *Photoshop*.  
Namely you can zoom in, zoom out, do panning, change opacity or visibility while interacting with the panel.

### Main Window UI Components

This section elaborates on each UI Component.

![][Figure002]{:class="center-img"}

As can be seen above, the Panel is composed of 4 main sections:

 *	Plug In Parameters
	*	11 Zone Buttons.  
		Each button sets whether to include (Pushed down) or exclude the specific tonal range zone in the output mask.  
	*	Source Channel Buttons.  
		Sets the source channel for the generation of the Luminosity Mask.  
		For instance the user can choose the Saturation as source and push down `Zone 0` and `Zone 1` which means low saturation colors will be chosen.
	*	Auto Tone.  
		When set to `ON` the plug in optimizes the Luminosity Mask to take advantage of the whole dynamic range.
	*	Contrast Level.  
		Controls the roll off of the Luminosity Mask. Higher value means more focused mask with shaper transitions between selected zones to excluded zones in the tonal range.
 *	User Adjustable Presets.  
	6 presest to cover 99% of the use cases for Luminosity Mask. The middle button is user configurable. Setting it by a long click (*Click & Hold*) which freezes the current settings into a preset.
 *	Panel State Elements - *Composite*, *Mask* and *Reset*.  
	The `Composite` mode displays the current output of the masking procedure. The `Mask` mode displays the Luminosity Mask. The `Reset` button resets, on click, teh state of the panel to its default. 
 *	Home Page, Settings, User Guide and About Screen Link Buttons.  
	Home Page opens a browser with the Fixel Website, Settings opens the Settings Window (See below) of the Plug In, User Guide open a web browser with this address and the About icon opens a window with the version string of the Plug In.

The main feature of the Plug In is being able to include or exclude tonal ranges (Zones) form the output.  
While most Luminosity Masks Actions / Panels just automates Photoshop procedure [Fixel Zone Selector 2][98]'s algorithm is implemented by a proprietary Plug In. It is not constrained by the limitations of Photoshop's tools as described in [Luminosity Mask - How Does It (Really) Work][04]? and [Luminosity Mask Done Right][05]! posts.  
Hence the user, at most time, will easily achieve the results with the highest quality in the industry.

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
	*	`Active Layer` (Default) - The Plug In will work on the current layer (Given it is a Bit Map / Rasterized Layer) of Photoshop and will adjust it according to parameters.
	*	`Stamp Visible` - The Plug In will create a new layer from the current view and will use it as input image.
 *	Reset Presets  
	Reset the presets of the panel to their default values.

The defaults should imitate behavior of a classic plug in's.  
The settings are saved in a user preference file and kept between Photoshop sessions.

## Using Fixel Zone Selector 2

This section describe how to use [Fixel Zone Selector 2][98].

### Workflow

[Fixel Zone Selector 2][98] is designed to give the user the experience of classic Plug In yet within Photoshop main window.  
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

[Fixel Zone Selector 2][98] has few parameters to adjust.  
This section will focus on the ability of [Fixel Zone Selector 2][98] (Basically the whole [Fixel Zone Selector][97] family) to enhance edges.  
[zoneselector][98] can target different sizes (*Radius*) of edges by adjusting its parameters.

<!-- Retina Display Support - https://stackoverflow.com/a/19186878/195787 -->
![][Figure006]{: class="center-img" srcset="{{site.baseurl}}/news/images/FixelZoneSelector2/FixelZoneSelector2RadiusImage@2x.png 2x"}

In the above figure one could 6 images where one is the *Original Image* and all the other are created by applying [Fixel Zone Selector 2][98] with different *radius* as written.
As can be seen, the *radius* parameter allows targeting different size of edges to enhance.

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure007]{: class="center-img" width="900" height="600"}

The above figure is displays the effect of the *Threshold Level* parameter.  
The *Threshold Level* parameter allows regulating the effect in order to prevent noise and artifact amplifications.  
As can be seen above, with higher regulation the over sharpened edged are regulated and the effect is limited on those.

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure008]{: class="center-img" width="900" height="600"}

The above image displays the effect of the *Luminosity Mode* parameter.  
The *Luminosity Mode* toggles whether to run the effect on Luminosity Channel only (When set to `On`) or on each of the `RGB` channels (When set to `Off`).  
As can be seen above, When set to `Off` the result is more saturated yet with more color shift which is a balance to be chosen by the user.  
Pay attention that when set to `Off` it means the filter is running 3 times, which, trivially, takes more time.

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure009]{: class="center-img" width="900" height="675"}

The above image displays the effect of the *Edge Preserving Mode* parameter.  
The *Edge Preserving Mode* toggles whether to use Edge Preserving algorithm (When set to `On`) or use the classic algorithm (When set to `Off`).  
As can be seen above, When set to `On` the **Halos** are almost completely eliminated. The result is more subtle.  
The Edge Preserving engine is a new feature in version 3 and creates completely new effect.

### Tips & Tricks

There are some simple guidelines to keep in order to maximize the effectiveness of using [Fixel Zone Selector 2][98]:

 *	The *Radius* parameter should match the size of the edges one wants to enhance.
 *	By turning on the *Edge Preserving Mode* one could achieve more subtle effect.
 *	When using high values one might want to use `Luminosity Mode` set to `OFF` in order to prevent reduction in saturation. In most cases one should set `Luminosity Mode` to `OFF` for no color shift and faster execution.
 

## Showcase

This section shows few images with *Before & After* animation. Under each image one could see the settings used to generate result.

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure010]{: class="center-img" width="900" height="500"}
{% include callout.html type="info" content="`Edge Radius = 3`, `Threshold Level = 0`, `Intensity Level = 90`, `Edge Preserving Mode = OFF`, `Luminosity Mode = ON`" %}

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure011]{: class="center-img" width="900" height="600"}
{% include callout.html type="info" content="`Edge Radius = 12`, `Threshold Level = 15`, `Intensity Level = 75`, `Edge Preserving Mode = OFF`, `Luminosity Mode = ON`" %}

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure012]{: class="center-img" width="900" height="675"}
{% include callout.html type="info" content="`Edge Radius = 2`, `Threshold Level = 0`, `Intensity Level = 100`, `Edge Preserving Mode = OFF`, `Luminosity Mode = OFF`" %}

### Users Showcase  
This section displays images created by users of [Fixel Zone Selector 2][98].

{% include image-user.html srcUrl="https://i.imgur.com/x9xKkVA.jpg" altString="spotshow13235" style="width: 900px; height: 900px;" content="Credit: [spotshow13235](https://flickr.com/photos/149616586@N06/26393322048/) by Ossst Dzesss" %}

## Summary
[Fixel Zone Selector 2][98] is a different kind of a sharpener. It enhance edges by utilizing a unique algorithm which was specifically developed for this task. While [Fixel Zone Selector 2][02] brought the concept of targeting edges specifically surpassing any classic sharpening tool (*High Pass Sharpening*, *Unsharp Mask*, *Smart Sharpen*) [Fixel Zone Selector 2][98] brings another jump forward - Edge Preserving Based & Halos Free Edge Enhancement.  
It is intuitive and easy to use (Classic Plug In behavior within Photoshop *Main Window*) yet in utilizes state of the art algorithm which is proprietary to Fixel Algorithms after years of development.  
We listened to the feedback of many of [Fixel Zone Selector 2][02] users and used it to create this step forward.  

We hope you'll find it useful as well and hope to hear your feedback to get even better with the upcoming iterations.

{% include important.html content="[Fixel Zone Selector 2][98] have extended [Fixel Zone Selector 2][02] to have Edge Preserving Engine. Yet when the option is disabled their output is very similar. Hence if you have [Fixel Zone Selector 2][98] you have no reason to buy [Fixel Zone Selector 2][02] unless *Adobe Photoshop CS6* compatibility is needed. Any user of [Fixel Zone Selector 2][98] can get [Fixel Zone Selector 2][02] for 50% discount. See *Upgrade Policy* in the respective product pages or *Contact Us*." %}

## Resources
 *  [Fixel Zone Selector 2 Product Page][98].
 *  [Fixel Zone Selector 2 Installation Guide][03].
 *  [Fixel Zone Selector 2 Product Page][02].

Key Words: [Fixel Algorithms][99], [Fixel][99], [Fixel Zone Selector][98], [Image Enhancement][98], [Image Contrast][98], [Image Sharpening][98], [Image Sharpening][98], [Detail Enhancement][98], [Contrast Enhancement][98], [Detail Boosting][98], [Edge Enhancement][98], [Edge Filter][98], [Photoshop][99], [Plug In][99], [Photoshop Plug In][99].


<!-- This is commented out -->
  [01]: {{site.baseurl}}/news/images/FixelZoneSelector2/FixelZoneSelector2Icon150px.png "Fixel Zone Selector 2 Icon"
  [02]: {{site.baseurl}}/products/zoneselector1 "Fixel Zone Selector 1"
  [03]: {{site.baseurl}}/support/fixel-zoneselector-2-installation-guide.html "Fixel Zone Selector 2 Installation Guide"
  [04]: {{site.baseurl}}/news/2018/03/luminosity-mask-001/index.html "Luminosity Mask - How Does It (Really) Work?"
  [05]: {{site.baseurl}}/news/2018/11/luminosity-mask-002/index.html "Luminosity Mask Done Right!"
  [97]: https://fixelalgorithms.co/products/zoneselector/ "Fixel Zone Selector - Simple, Smart & Effective Edge Enhancer Filter - Adobe Photoshop Plug In"
  [98]: https://fixelalgorithms.co/products/zoneselector2/ "Fixel Zone Selector 2 - Simple, Smart & Effective Edge Enhancer Filter - Adobe Photoshop Plug In"
  [99]: https://fixelalgorithms.co "Fixel Algorithms"
  [Figure001]: {{site.baseurl}}/news/images/FixelZoneSelector2/Fixel Zone Selector 2 - User Interface 001.png "Figure 001 - Fixel Zone Selector 2 User Interface"
  [Figure002]: {{site.baseurl}}/news/images/FixelZoneSelector2/Fixel Zone Selector 2 - User Interface 002.png "Figure 002 - Fixel Zone Selector 2 User Interface Sections"
  [Figure003]: {{site.baseurl}}/news/images/FixelZoneSelector2/Fixel Zone Selector 2 - User Interface 003.png "Figure 003 - Fixel Zone Selector 2 User Interface (Settings Window)"
  [Figure004]: {{site.baseurl}}/news/images/FixelZoneSelector2/Fixel Zone Selector 2 - User Interface 004.png "Figure 004 - Fixel Zone Selector 2 User Interface (Settings Window)"
  [Figure005]: {{site.baseurl}}/news/images/FixelZoneSelector2/Fixel Zone Selector 2 - User Interface 005.png "Figure 005 - Fixel Zone Selector 2 User Interface (Settings Window)"
  [Figure006]: {{site.baseurl}}/news/images/FixelZoneSelector2/FixelZoneSelector2RadiusImage.png "Figure 006 - Demonstration of Different Radius"
  [Figure007]: {{site.baseurl}}/news/images/FixelZoneSelector2/FixelZoneSelector2ThresholdImage.png "Figure 007 - Demonstration of Threshold Effect"
  [Figure008]: {{site.baseurl}}/news/images/FixelZoneSelector2/FixelZoneSelector2LuminosityImage.png "Figure 008 - Demonstration of Luminosity Mode"
  [Figure009]: {{site.baseurl}}/news/images/FixelZoneSelector2/FixelZoneSelector2EdgePreservingImage.png "Figure 009 - Demonstration of Edge Preserving Mode"
  [Figure010]: {{site.baseurl}}/news/images/FixelZoneSelector2/FixelZoneSelector2ShowCase001.png "Figure 010 - Showcase Image"
  [Figure011]: {{site.baseurl}}/news/images/FixelZoneSelector2/FixelZoneSelector2ShowCase002.png "Figure 011 - Showcase Image"
  [Figure012]: {{site.baseurl}}/news/images/FixelZoneSelector2/FixelZoneSelector2ShowCase003.png "Figure 012 - Showcase Image"
  