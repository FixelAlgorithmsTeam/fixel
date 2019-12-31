---
title:  Fixel Contrastica 3 - User Guide
date: 	2019-12-26
author: Fixel Algorithms
layout: post
class:  news
hidden: true
---
![Fixel Contrastica 3 Smart and Simple Local and Global Contrast Intensifier Plug In for Adobe Photoshop][01]

# Fixel Contrastica 3 - Smart and Simple Local and Global Contrast Intensifier - User Guide

## Introduction

[Fixel Contrastica 3][98] is all about local and global contrast. If you want to intensify the local and global contrast in an intuitive and effective manner this is the Plug In you need.

[Fixel Contrastica 3][98] is the 3rd generation of the [Fixel Contrastica][97] family.  
This version adds the following features:

 *	Edge Preserving Engine  
	The new engine is built on a *Local Edge Preserving Filter* which combines speed and quality. It assists in reducing the artifacts and halos which are common in contrast enhancement.  
	The new engine gives the user the ability to push farther the local & global contrast intensification level with *Halos Free* stunning results.
 *	HTML Based UI  
	New UI for optimized and intuitive workflow build around *Adobe Photoshop*'s HTML Panel technology.  
	Unlike classic Plug In's [Fixel Contrastica 3][98] can be used as a side panel with the image always available for peaking, zooming and panning.  
	The new UI also adds *3 user adjustable presets* to allow user have more efficient workflow.

This user guide present [Fixel Contrastica 3][98] to the user with simple guidelines on how to use properly to achieve optimal results.

{% include note.html content="The new UI Technology requires Adobe Photoshop CC 2017 and above. For CS6 compatibility the user should use [Fixel Contrastica 2][02]." %}

## Installation
The installation is automated using the Windows and macOS installers.  
Please follow the following steps:

 *	Verify *Adobe Photoshop* is not running.
 *	Unzip the `ZIP` file downloaded on purchase.
 *	Run the installer inside the `ZIP` file:
	*	Windows - *Double Click* `Fixel Contrastica 3 - Windows Installer.exe` installer and follow instruction.  
		The user may be asked for *Administrator* privileges in order to install the Plug In.
	*	macOS - *Double Click* on `Fixel Contrastica - macOS Installer.dmg` disk image and follow instructions.  
		The user may be asked for *Administrator* privileges in order to install the Plug In.
 *	Start *Adobe Photoshop* and launch the UI (See below).

If any issues arise, please refer to [Fixel Contrastica 3 Installation Guide][03].

## Fixel Contrastica 3 UI

This section will show [Fixel Contrastica 3][98] User Interface (UI) and how to use it.

### Launching Contrastica 3 User Interface (Panel)

In order to launch the panel the user should:

 *	Open Photoshop.
 *	In Photoshop menu click on `Window -> Extensions -> Fixel Contrastica 3`.

Once done, the Contrastica 3 UI will present itself:

![][Figure001]{:class="center-img"}

The UI enable simple and intuitive operation of the local & global contrast intensification process.  
The panel allows the user to interact with the image while adjusting its parameters as it was any other native *Panel* of *Photoshop*.  
Namely you can zoom in, zoom out, do panning, change opacity or visibility while interacting with the panel.

### Main Window UI Components

This section elaborates on each UI Component.

![][Figure002]{:class="center-img"}

As can be seen above, the Panel is composed of 4 main sections:

 *	Plug In Parameters
	*	Image Resolution Drop Down Menu.  
		Sets the *Local Contrast* effect according to the image resolution. User should experience with different values to see the different effect.
	*	Local Contrast Level Slider
		Sets the local contrast enhancement level. Higher values means stronger effect.
	*	Local Contrast Regularization Slider
		Sets the regularization level of the local contrast effect. Lower values means *Halos* are suppressed while higher values means local contrast is harsher.  
		Lower values means the *Edge Preserving* algorithm is more effective.
	*	Global Contrast Level Slider.  
		Sets the global contrast level. Higher values means stringer global contrast effect.
	*	Global Contrast Balance Slider.  
		Sets the balance between *Shadows and Highlights* in the global contrast effect.
	*	Intensity Slider.  
		Sets the overall intensity of the filter.
	*	High Quality Mode.  
		When set to `ON` the filter is using *High Quality Mode* which is little slower yet might reduce artifacts. Most of the times Standard Quality (When set to `OFF`) is good enough.
	*	Luminosity Mode.  
		When set to `ON` the filter is applied on the *Luminosity Channel* of the image (*Saturation* and *Hue* channels are untouched).
 *	User Adjustable Presets.  
	Allows the user to apply pre defined presets by clicking a preset button. Setting a preset is done by long click (*Click & Hold*) which freezes the current settings into a preset.
 *	Panel State Elements - *Apply*, *Cancel* and *Preview*.  
	In case the `Live View` is disabled one must click on `Apply` to run the filter. The button *Cancel* cancels the effect and restore the image into its original form. The *Preview* button toggles between seeing the input image and the output image.
 *	Home Page, Settings, User Guide and About Screen Link Buttons.  
	Home Page opens a browser with the Fixel Website, Settings opens the Settings Window (See below) of the Plug In, User Guide open a web browser with this address and the About icon opens a window with the version string of the Plug In.

The main feature of the Plug In is applying Local & Global Contrast in effective and intuitive way while controlling the details size and the shadows and highlights balance.  
Hence the user, at most time, will interact with the 2 upper sliders to adjust the Plug In effect to taste.

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

## Using Fixel Contrastica 3

This section describe how to use [Fixel Contrastica 3][98].

### Workflow

[Fixel Contrastica 3][98] is designed to give the user the experience of classic Plug In yet within Photoshop main window.  
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

[Fixel Contrastica 3][98] has few parameters to adjust in order to achieve the desired result.  
This section will focus on the effect of [Fixel Contrastica 3][98]'s parameters to enhance local and global contrast.  


[Contrastica][98] has few presets to handle different Local Contrast resolutions by the *resolution* parameter.

<!-- Retina Display Support - https://stackoverflow.com/a/19186878/195787 -->
![][Figure006]{: class="center-img" width="900" height="900"}

In the above figure one could see animation of 6 images where one is the *Original Image* and all the other are created by applying [Fixel Contrastica 3][98] with different *resolution* settings.
As can be seen, the *resolution* parameter create different local contrast effect for different values.

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

There are some simple guidelines to keep in order to maximize the effectiveness of using [Fixel Contrastica 3][98]:

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
This section displays images created by users of [Fixel Contrastica 3][98].

{% include image-user.html srcUrl="https://i.imgur.com/x9xKkVA.jpg" altString="spotshow13235" style="width: 900px; height: 900px;" content="Credit: [spotshow13235](https://flickr.com/photos/149616586@N06/26393322048/) by Ossst Dzesss" %}

## Summary
[Fixel Contrastica 3][98] is a new generation of local & global contrast intensifiers. It intensify local & global contrast by utilizing a unique algorithm which was specifically developed for this task. While [Fixel Contrastica 2][02] brought the concept of enhancing both local & global contrast in a single tool to the market being more effective and intuitive to use than any classic sharpening tool (*High Pass Sharpening*, *Unsharp Mask*, *Smart Sharpen*) [Fixel Contrastica 3][98] brings another jump forward - Edge Preserving Based & Halos Free Local & Contrast enhancement.  
It is intuitive and easy to use (Classic Plug In behavior within Photoshop *Main Window*) yet in utilizes state of the art algorithm which is proprietary to Fixel Algorithms after years of development.  
We listened to the feedback of many of [Fixel Contrastica 2][02] users and used it to create this step forward.  

We hope you'll find it useful as well and hope to hear your feedback to get even better with the upcoming iterations.

{% include important.html content="[Fixel Contrastica 3][98] & [Fixel Contrastica 2][02] have completely different local & global contrast enhancement engines which produce different results. Many find them to work greatly side by side as they find each one better for different images. [Fixel Contrastica 2][02] also provides *Adobe Photoshop CS6 Compatibility*. Hence any user of [Fixel Contrastica 3][98] can get [Fixel Contrastica 2][02] for 50% discount. See *Upgrade Policy* in the respective product pages or *Contact Us*." %}

## Resources
 *  [Fixel Contrastica 3 Product Page][98].
 *  [Fixel Contrastica 3 Installation Guide][03].
 *  [Fixel Contrastica 2 Product Page][02].

Key Words: [Fixel Algorithms][99], [Fixel][99], [Fixel Contrastica][98], [Image Enhancement][98], [Image Contrast][98], [Image Sharpening][98], [Image Sharpening][98], [Detail Enhancement][98], [Contrast Enhancement][98], [Detail Boosting][98], [Local Contrast][98], [Global Contrast][98], [Contrast Filter][98], [Photoshop][99], [Plug In][99], [Photoshop Plug In][99].


<!-- This is commented out -->
  [01]: {{site.baseurl}}/news/images/FixelContrastica3/FixelContrastica3Icon150px.png "Fixel Contrastica 3 Icon"
  [02]: {{site.baseurl}}/products/contrastica2 "Fixel Contrastica 2"
  [03]: {{site.baseurl}}/support/fixel-contrastica-3-installation-guide.html "Fixel Contrastica 3 Installation Guide"
  [97]: https://fixelalgorithms.co/products/contrastica/ "Fixel Contrastica - Smart and Simple Local and Global Contrast Intensifier - Adobe Photoshop Plug In"
  [98]: https://fixelalgorithms.co/products/contrastica3/ "Fixel Contrastica 3 - Smart and Simple Local and Global Contrast Intensifier - Adobe Photoshop Plug In"
  [99]: https://fixelalgorithms.co "Fixel Algorithms"
  [Figure001]: {{site.baseurl}}/news/images/FixelContrastica3/Fixel Contrastica 3 - User Interface 001.png "Figure 001 - Fixel Contrastica 3 User Interface"
  [Figure002]: {{site.baseurl}}/news/images/FixelContrastica3/Fixel Contrastica 3 - User Interface 002.png "Figure 002 - Fixel Contrastica 3 User Interface Sections"
  [Figure003]: {{site.baseurl}}/news/images/FixelContrastica3/Fixel Contrastica 3 - User Interface 003.png "Figure 003 - Fixel Contrastica 3 User Interface (Settings Window)"
  [Figure004]: {{site.baseurl}}/news/images/FixelContrastica3/Fixel Contrastica 3 - User Interface 004.png "Figure 004 - Fixel Contrastica 3 User Interface (Settings Window)"
  [Figure005]: {{site.baseurl}}/news/images/FixelContrastica3/Fixel Contrastica 3 - User Interface 005.png "Figure 005 - Fixel Contrastica 3 User Interface (Settings Window)"
  [Figure006]: {{site.baseurl}}/news/images/FixelContrastica3/FixelContrastica3ResolutionImage.png "Figure 006 - Demonstration of Different Resolutions"
  [Figure007]: {{site.baseurl}}/news/images/FixelContrastica3/FixelContrastica3ThresholdImage.png "Figure 007 - Demonstration of Threshold Effect"
  [Figure008]: {{site.baseurl}}/news/images/FixelContrastica3/FixelContrastica3LuminosityImage.png "Figure 008 - Demonstration of Luminosity Mode"
  [Figure009]: {{site.baseurl}}/news/images/FixelContrastica3/FixelContrastica3EdgePreservingImage.png "Figure 009 - Demonstration of Edge Preserving Mode"
  [Figure010]: {{site.baseurl}}/news/images/FixelContrastica3/FixelContrastica3ShowCase001.png "Figure 010 - Showcase Image"
  [Figure011]: {{site.baseurl}}/news/images/FixelContrastica3/FixelContrastica3ShowCase002.png "Figure 011 - Showcase Image"
  [Figure012]: {{site.baseurl}}/news/images/FixelContrastica3/FixelContrastica3ShowCase003.png "Figure 012 - Showcase Image"
  