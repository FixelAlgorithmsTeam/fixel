---
title:  Fixel Zone Selector 2 - User Guide
date: 	2020-04-05
author: Fixel Algorithms
layout: post
class:  news
hidden: true

beforeafter: true
---

{% comment %}
The function assign can't interpolate variables hence this won't work:
{% assign imgBaseUrl = "{{site.baseurl}}/news/images/FixelZoneSelector2" %}
Below it is solved by prepend. It could also be solved by capture:
{% capture imgBaseUrl %}{{ site.baseurl }}/news/images/FixelZoneSelector2{% endcapture %}
{% endcomment %}
{% assign imgBaseUrl = "/news/images/FixelZoneSelector2" | prepend: site.baseurl %}

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
		For instance the user can choose the `Saturation` as source and push down `Zone 0` and `Zone 1` which means low saturation colors will be chosen.
	*	Auto Tone.  
		When set to `ON` the plug in optimizes the Luminosity Mask to take advantage of the whole dynamic range.
	*	Contrast Level.  
		Controls the roll off of the Luminosity Mask. Higher value means more focused mask with shaper transitions between selected zones to excluded zones in the tonal range.
 *	User Adjustable Presets.  
	6 presets to cover 99% of the use cases for Luminosity Mask. The middle button is user configurable. Setting it by a long click (*Click & Hold*) which freezes the current settings into a preset.
 *	Panel State Elements - *Composite*, *Mask* and *Reset*.  
	The `Composite` mode displays the current output of the masking procedure. The `Mask` mode displays the Luminosity Mask. The `Reset` button resets, on click, teh state of the panel to its default. 
 *	Home Page, Settings, User Guide and About Screen Link Buttons.  
	Home Page opens a browser with the Fixel Website, Settings opens the Settings Window (See below) of the Plug In, User Guide open a web browser with this address and the About icon opens a window with the version string of the Plug In.

The main feature of the Plug In is being able to include or exclude tonal ranges (Zones) form the output.  
While most Luminosity Masks Actions / Panels just automates Photoshop procedure [Fixel Zone Selector 2][98]'s algorithm is implemented by a proprietary Plug In. It is not constrained by the limitations of Photoshop's tools as described in [Luminosity Mask - How Does It (Really) Work][04]? and [Luminosity Mask Done Right][05]! posts.  
Hence the user, at most time, will easily achieve the results with the highest quality in the industry.

### Settings Window Parameters

Currently there are no user controlled settings.

## Using Fixel Zone Selector 2

This section describe how to use [Fixel Zone Selector 2][98].

### Workflow

[Fixel Zone Selector 2][98] is designed to give the user effortless ability to generate the Luminosity Masks with pinpoint accuracy.  
The recommended usage of Plug In is as following:

 *	Start a new session by launching the Panel.  
	Make sure the active layer is the layer to be used as reference for the mask generation.  
	The Plug In will add a Mask Channel automatically.
 *	Interact and adjust its parameters to taste.
 *	Toggle between `Composite` / `Mask` modes to evaluate result.
 *	Tweak parameters to adjust output to taste.

When done with the Plug In, continue working on Photoshop.  
You may return to the layer of interest to tweak result as needed.  

<!-- {% include note.html content="Changing the active layer or doing any destructive action (Anything but Zooming, Panning, Changing Visibility or Opacity) while working with the Panel will cause it to start a new session." %} -->

### Effect of Parameters

[Fixel Zone Selector 2][98] has few parameters to adjust with the main ones being the selection of zones.  
This section will focus on the different values of the main parameter of [Fixel Zone Selector 2][98].  
[Fixel Zone Selector 2][98] can target generate different mask targeting different tonal ranges quite easily.

<!-- Retina Display Support - https://stackoverflow.com/a/19186878/195787 
![][Figure006]{: class="center-img" srcset="{{site.baseurl}}/news/images/FixelZoneSelector2/FixelZoneSelector2RadiusImage@2x.png 2x"} -->
![][Figure006]{: class="center-img" width="900" height="600"}

In the above figure one could see 7 images: The big one as the input and 6 small ones represent the 6 presets ordered as in the top left corner.
As can be seen, the *presets* indeed generate the expected mask according to the applied preset. The masks are very smooth yet selective.

{% assign imgUrlBase = "FixelZoneSelectorContrastImage001.png|FixelZoneSelectorContrastImage002.png|FixelZoneSelectorContrastImage003.png|FixelZoneSelectorContrastImage004.png|FixelZoneSelectorContrastImage005.png" | split: "|" %}
{% assign imgCptnH = "" | split: "|" %}
{% assign imgCptnP = "Green Channel, Contrast: -100|Green Channel, Contrast: -50|Green Channel, Contrast: 0|Green Channel, Contrast: 50|Green Channel, Contrast: 100" | split: "|" %}
{% assign imgUrl = '' | split: '' %}
{% for simgUrl in imgUrlBase %}
		{% if simgUrl contains "http" %}
			{% assign tmpString = simgUrl %}
		{% else %}
			{% capture tmpString %}{{ imgBaseUrl }}/{{ simgUrl }}{% endcapture %}
		{% endif %}
		{% assign imgUrl = imgUrl | push: tmpString %}
{% endfor %}

{% include image-carousel.html idString="ContrastImage" imgWidth="800px" dataInterval="false" imgUrl=imgUrl imgCptnH=imgCptnH imgCptnP=imgCptnP %}

The above image carousel shows the effect of the parameter `Contrast`. The parameter can be used to change how harsh the transition between included tonal range to those which are excluded.  
The higher the contrast the sharper the transition. Intuitive way to think about it is how focused one wants the mask to be.

{% assign imgUrlBase = "FixelZoneSelectorChannelsImage001.png|FixelZoneSelectorChannelsImage002.png|FixelZoneSelectorChannelsImage003.png" | split: "|" %}
{% assign imgCptnH = "" | split: "|" %}
{% assign imgCptnP = "Shadows|Midtones|Highlights" | split: "|" %}
{% assign imgUrl = '' | split: '' %}
{% for simgUrl in imgUrlBase %}
		{% if simgUrl contains "http" %}
			{% assign tmpString = simgUrl %}
		{% else %}
			{% capture tmpString %}{{ imgBaseUrl }}/{{ simgUrl }}{% endcapture %}
		{% endif %}
		{% assign imgUrl = imgUrl | push: tmpString %}
{% endfor %}

{% include image-carousel.html idString="ChannelsImage" imgWidth="800px" dataInterval="false" imgUrl=imgUrl imgCptnH=imgCptnH imgCptnP=imgCptnP %}

The above image carousel shows the effect of the parameter `Source Channel`. In each image one could see the different channels of `RGB` for different tonal ranges - Shadows, Midtones and Highlights.  
In many cases working on different channels can generate the perfect selection as we add color information to the tonal range.
As one could see, in some cases the tool can even generate interesting grayscale look (*High Key*).

{% comment %}
<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure007]{: class="center-img" width="900" height="600"}
{% endcomment %}

### Tips & Tricks

There are some simple guidelines to keep in order to maximize the effectiveness when using [Fixel Zone Selector 2][98]:

 *	Start with the given presets and add or remove specific zones as needed.
 *	Explore different channels as sometimes the information is in the color and not only in the Luminosity.
 *	Use the `Contrast` parameter as the final step to tweak the output mask.
 

## Showcase

This section shows few images with different parameters applied on them.

{% assign imgUrlBase = "ShowCase001Image001.png|ShowCase001Image002.png|ShowCase001Image003.png|ShowCase001Image004.png|ShowCase001Image005.png|ShowCase001Image006.png|ShowCase001Image007.png" | split: "|" %}
{% assign imgCptnH = "" | split: "|" %}
{% assign imgCptnP = "Input Image|Shadows|Midtones|Highlights|Shadows & Highlights|Shadows & Midtones|Highlights & Midtones" | split: "|" %}
{% assign imgUrl = '' | split: '' %}
{% for simgUrl in imgUrlBase %}
		{% if simgUrl contains "http" %}
			{% assign tmpString = simgUrl %}
		{% else %}
			{% capture tmpString %}{{ imgBaseUrl }}/{{ simgUrl }}{% endcapture %}
		{% endif %}
		{% assign imgUrl = imgUrl | push: tmpString %}
{% endfor %}

{% include image-carousel.html idString="ShowCase001" imgWidth="900px" dataInterval="false" imgUrl=imgUrl imgCptnH=imgCptnH imgCptnP=imgCptnP %}

In the above show case (Click on Left / Right to scroll the images) one could see the results of each 6 presets.  
The image is fairly complicated with high dynamic range to show the quality and accuracy of [Fixel Zone Selector 2][98].

{% capture img1Url %}{{ imgBaseUrl }}/ShowCase002Image001.png{% endcapture %}
{% capture img2Url %}{{ imgBaseUrl }}/ShowCase002Image002.png{% endcapture %}
{% include image-twentytwenty.html img1Url=img1Url img2Url=img2Url imgWidth="900"  imgHeight="600" %}
{% include callout.html type="info" content="`Preset - Highlights & Midtones`, `Channel = R`, `Contrast = 0`, `Auto Tone = ON`" %}

<!-- Retina Display Support - https://stackoverflow.com/a/13746012/195787 -->
![][Figure007]{: class="center-img" width="900" height="600"}
{% include callout.html type="info" content="`Preset - Shadows`, `Channel = B`, `Contrast = 25`, `Auto Tone = ON`" %}

{% comment %}
### Users Showcase  
This section displays images created by users of [Fixel Zone Selector 2][98].

{% include image-user.html srcUrl="https://i.imgur.com/x9xKkVA.jpg" altString="spotshow13235" style="width: 900px; height: 900px;" content="Credit: [spotshow13235](https://flickr.com/photos/149616586@N06/26393322048/) by Ossst Dzesss" %}
{% endcomment %}

## Summary
[Fixel Zone Selector 2][98] is a different kind of a Luminosity Mask generator. It prioritizes the accuracy and quality of the mask with the simplest user experience in order to be effective. The idea is a tool that does one thing but does it very well.  
[Fixel Zone Selector 2][98] utilizes state of the art algorithm which is proprietary to Fixel Algorithms which was improved in version 2 of the Plug In. [Fixel Zone Selector 2][98] also improves the UI and give the user more choices: Presets, Source Channel and Contrast in a modern HTML5 based UI.  
We listened to the feedback of many of [Fixel Zone Selector 2][02] users and used it to create this step forward.  

We hope you'll find it useful as well and hope to hear your feedback to get even better with the upcoming iterations.

{% include important.html content="[Fixel Zone Selector 2][98] have extended [Fixel Zone Selector 1][02] with many new features. Yet [Fixel Zone Selector 2][98] doesn't support Photoshop CS6. Hence if you have [Fixel Zone Selector 2][98] you have no reason to buy [Fixel Zone Selector 1][02] unless *Adobe Photoshop CS6* compatibility is needed. Any user of [Fixel Zone Selector 2][98] can get [Fixel Zone Selector 1][02] for 50% discount. See *Upgrade Policy* in the respective product pages or *Contact Us*." %}

## Resources
 *  [Fixel Zone Selector 2 Product Page][98].
 *  [Fixel Zone Selector 2 Installation Guide][03].
 *  [Fixel Zone Selector 1 Product Page][02].

Key Words: [Fixel Algorithms][99], [Fixel][99], [Fixel Zone Selector][98], [Image Enhancement][98], [Luminosity Mask][98], [Saturation Mask][98], [Tonal Range Selection][98], [Photoshop][99], [Plug In][99], [Photoshop Plug In][99].


<!-- This is commented out -->
  [01]: {{site.baseurl}}/news/images/FixelZoneSelector2/FixelZoneSelector2Icon150px.png "Fixel Zone Selector 2 Icon"
  [02]: {{site.baseurl}}/products/zoneselector1 "Fixel Zone Selector 1"
  [03]: {{site.baseurl}}/support/fixel-zoneselector-2-installation-guide.html "Fixel Zone Selector 2 Installation Guide"
  [04]: {{site.baseurl}}/news/2018/03/luminosity-mask-001/index.html "Luminosity Mask - How Does It (Really) Work?"
  [05]: {{site.baseurl}}/news/2018/11/luminosity-mask-002/index.html "Luminosity Mask Done Right!"
  [97]: https://fixelalgorithms.co/products/zoneselector/ "Fixel Zone Selector - Simple, Smart & Effective Edge Enhancer Filter - Adobe Photoshop Plug In"
  [98]: https://fixelalgorithms.co/products/zoneselector2/ "Fixel Zone Selector 2 - Simple, Smart & Effective Edge Enhancer Filter - Adobe Photoshop Plug In"
  [99]: https://fixelalgorithms.co "Fixel Algorithms"
  [Figure001]: {{imgBaseUrl}}/Fixel Zone Selector 2 - User Interface 001.png "Figure 001 - Fixel Zone Selector 2 User Interface"
  [Figure002]: {{imgBaseUrl}}/Fixel Zone Selector 2 - User Interface 002.png "Figure 002 - Fixel Zone Selector 2 User Interface Sections"
  [Figure003]: {{imgBaseUrl}}/Fixel Zone Selector 2 - User Interface 003.png "Figure 003 - Fixel Zone Selector 2 User Interface (Settings Window)"
  [Figure004]: {{imgBaseUrl}}/Fixel Zone Selector 2 - User Interface 004.png "Figure 004 - Fixel Zone Selector 2 User Interface (Settings Window)"
  [Figure005]: {{imgBaseUrl}}/Fixel Zone Selector 2 - User Interface 005.png "Figure 005 - Fixel Zone Selector 2 User Interface (Settings Window)"
  [Figure006]: {{imgBaseUrl}}/FixelZoneSelectorPresets.png "Figure 006 - Demonstration of Different Zones"
  [Figure007]: {{imgBaseUrl}}/ShowCase003.png "Figure 007 - Demonstration of Threshold Effect"
  