---
title: 'Fixel PixelGear 2 - Quick Start Guide'
date: 	2019-04-13
author: Fixel Algorithms
layout: post
class:  news
hidden: true
---
![Fixel PixelGear 2 Photoshop Plug In][01]

# Fixel PixelGear 2 Photoshop Plug In

## Background

Fixel collaborate with other teams in order to create the perfect products. Fixel main contribution is its unique algorithms.  
Sometimes such collaboration comes to an end and a decision must be made about the joint product.  
This is the case of [Fixel PixelGear 2][98] which used to be called [PSKiss PixelGear 2][02].  
Since many users use this product daily, instead of archiving we decided to bring it back home.  
We intend to continue develop it and make it better each generation.  
Yet before that, we just picked it as it was (Wonderful!), fixed few bugs, optimized performance and renamed is - [**Fixel PixelGear 2**][98].

[Fixel PixelGear 2][98] is all about Keep It Simple and Smart. It integrates a simple and intuitive workflow yet utilizes advanced algorithms.  
This post is a redo of [PSKiss PixelGear 2 Quick Start Guide][02].

## Introduction

[Fixel PixelGear 2][98] is composed of 3 filters:

 1.	SkinGear – A professional skin retouch filter.
 2.	ToneGear – A professional Shadows, Highlights and Global contrast enhancement filter.
 3.	EdgeGear – A professional edge enhancer.

All filters based on original algorithms, specially designed for this panel.

In this tutorial we will use a portrait photo in order to emphasize SkinGear’s advantage in skin retouch. You can use PixelGear 2 on any kind of photos.  
After installing `PixelGear 2` (See [Fixel PixelGear 2 Installation Guide][03]) panel and filters and presenting the panel, open a photo you wish to edit.

In this tutorial we'll be using the following photo (By *Yair Tsriker*) as reference:

![][Figure001]{:class="center-img"}

## Launching PixelGear 2 User Inteface (Panel)

In order to launch the panel the user should:

 *	Open Photoshop.
 *	In Photoshop menu click on `Window -> Extensions -> Fixel PixelGear`.

Once done, the PixelGear 2 UI will present itself:

![][Figure002]{:class="center-img"}

As can be seen above, the Panel is composed of 3 Tabs for 3 Filters.  
By default the first Filter / Tab presented in PixelGear 2 panel is SkinGear. If you want to use EdgeGear or ToneGear, simply click them at the bottom of the panel.

## Retouch Skin With SkinGear

To start the retouch process, you need first to create a selection of the skin areas.

Click on the `Color Range` button to open the Color Range dialog box.

![][Figure003]{:class="center-img"}

Select `Skin Tones` from the drop-down menu inside the `Color Range` dialog box:

![][Figure004]{:class="center-img"}

Use the Fuzziness slider to include or exclude skin tones.

![][Figure005]{:class="center-img"}

When done, click `OK`. This will mark a selection on your image (*Marching Ants*):

![][Figure006]{:class="center-img"}

To convert this selection into a layer mask, click the `Create Mask` button.

![][Figure007]{:class="center-img"}

This will automatically duplicate the Background layer, add a layer mask based on your selection and activate the layer itself, so you can apply the filter in the next step (Do not change the layer’s name, it is necessary for future editing):

![][Figure008]{:class="center-img"}

PixelGear has advanced Preset manager. Click on the Presets Menu button in the PixelGear panel in order to open it.

![][Figure009]{:class="center-img"}

Select the preset you need for this retouch (More about presets in the bottom of this post).

![][Figure010]{:class="center-img"}

The filter is activated automatically with the preset’s parameters. The panel is updated to display those parameters as well.

![][Figure011]{:class="center-img"}

### Retouching Skin with SkinGear Sliders / Parameters

 *	Use `Smart Smooth` to soften the overall “feel” of the skin. Higher values mean softer skin. This slider should have the largest value of the first 4 sliders.
 *	Use `Preserve Skin` Features to threshold smoothing strength. Higher values means more original details are maintained. Lower values mean smoother skin.
 *	Use `Remove Skin Defects` to smooth small skin details.
 *	Use `Overall Restore` to control how much detail will be preserved. Higher values mean more details. Lower values mean less details.
 *	Use `Intensity` to control the impact of the filter. Higher values mean significant smoothing. Lower values mean milder influence.

Think of these sliders as if they were “layering” the face from large details to small texture details.
For best results, keep values of the first 4 sliders in descending order. Namely `Smart Smooth` has the highest value, `Preserve Skin` is next, then `Remove Skin Defects` and the lowest value is `Overall Restore`.  
The basic thumb rule is – the larger the gap between `Smart Smooth` and `Preserve Skin` the smoother the skin.

In the above sample we used our “Beauty” preset.

### Fine Tuning of the Mask

After applying the filter, you might find out that some areas, such as eyes, lips and hair, need to be excluded from the filter’s influence. In addition, some skin areas might need to be added to the effected areas.

In order to edit the mask, do as following:

 1.	`Alt` / `Option` Click on the mask thumbnail in the layers panel to present the mask.  
![][Figure012]{:class="center-img"}
![][Figure013]{:class="center-img"}
 2.	Choose the `Paint Brush` tool.
![][Figure014]{:class="center-img"}
 3.	Set the `Foreground` / `Background` colors to default.
![][Figure015]{:class="center-img"}
 4.	Paint with white on places you want to add to the effected areas; Paint with black on places you want to exclude (use the “X” key to exchange between them).
![][Figure016]{:class="center-img"} 
 5.	`Alt` / `Option` Click the mask thumbnail to present the colored image. If needed, keep working on the mask. Pay attention to important “character” details, such as smile wrinkles and nostrils. In this example we also excluded the hair.
![][Figure017]{:class="center-img"} 

### Final Retouch of Skin Defects

Some defects can’t be removed by the filter and must be removed manually.  
In order manually remove these defects do as following:

 1. Activate the layer (Instead of the mask) by clicking its thumbnail in the Layers panel.
![][Figure018]{:class="center-img"}
 2.	Choose the appropriate retouch tool, the `Spot Healing Brush`, the `Healing Brush` or the `Clone Stamp Tool`.
![][Figure019]{:class="center-img"}
 3.	Zoom in and remove the defects.
![][Figure020]{:class="center-img"}

### Adding Grain
Sometimes, after smoothing a portrait, the image might not look *realistic* enough. One way to prevent this is adding some grain to the retouched areas.  
In order to do this withing the `SkinGear` workflow is as follows:

 1.	Drag the Grain slider to add grain to the image.
![][Figure021]{:class="center-img"}
 2.	A `Grain` layer will be added automatically.
![][Figure022]{:class="center-img"}
 3.	Note that the grain layer effects only retouched areas (It uses a duplicated mask of the `SkinGear` layer).
 4.	If you would like to use a different grain level, simply drag the slider to a different value.

### Using SkinGear Presets
`SkinGear` comes with 3 pre defined presets.  
In order to use the *Presets* follow these steps:

 1.	Accessing the *Presets Menu* is done by click on the 3 stripes button ([Hamburger Menu](https://en.wikipedia.org/wiki/Hamburger_button)) at the top of the `PixelGear` panel.
![][Figure023]{:class="center-img"}
 2.	Click on the preset you want to use.
![][Figure024]{:class="center-img"}

The *Pre Defined Presets* are as following:

 *	**Editorial** – Uses low smoothing values and basic intensity. Suitable for official portraits and editorial usage.
 *	**Beauty** – Uses medium smoothing values and higher intensity. Suitable for commercial beauty and fashion photos.
 *	**China Doll** – Uses high smoothing values and high intensity. Use this one when you want that “China Doll” face effect.

The user can create his own presets as well:

 1.	Set the filter sliders directly in the panel to taste (Following the guide line of course).
 2.	Open the *Preset Menu* as described above.
 3.	In the *Text Box* write the *Preset Name* and click on the `+` button.
![][Figure025]{:class="center-img"}
![][Figure026]{:class="center-img"}
 4.	To remove a preset from the list, click the `–` button next to its name.
![][Figure027]{:class="center-img"}
 5.	Click `OK` and it will be removed from the presets list. 
![][Figure028]{:class="center-img"}

## Shadows, Highlights and Global Contrast Enhancement with ToneGear
`ToneGear` is the tool to have a full control on the tonality of the image. It allows the user easily adapt any tonal style wanted.  
Basic workflow to utilize `ToneGear` is:

 *	Select the `ToneGear` filter, by clicking its name at the bottom of `PixelGear` panel.
![][Figure029]{:class="center-img"}
 *	Click on the `Presets Menu` button in the `ToneGear` panel and select the preset to apply.
![][Figure030]{:class="center-img"}
 *	This will automatically create a new layer based on a merge of the current layers in your image. The new layer will be named `Tone Gear` (Do not change this name, it is necessary for future editing).
![][Figure031]{:class="center-img"}
 * 	Now make the needed adjustments using the sliders.

{% include note.html content="You can create the new `Tone Gear` layer by dragging one of `ToneGear`’s sliders. Using a preset to initiate the process is not mandatory." %}

<!--<div markdown="span" class="alert alert-info" role="alert"><i class="fa fa-info-circle"></i> <b>Note:</b> Test!</div>-->

### Control Contrast with ToneGear

 *	`Shadows Contrast` edits contrast in darker parts of the image. Higher value means lighter shadows.
 *	`Shadows Range` sets the tonal range for shadows. Higher value increases tonal range of shadows and more areas will be effected by Shadows Contrast changes.
 *	`Highlights Contrast` edits contrast in brighter parts of the image. Higher value means darker highlights.
 *	`Highlights Range` sets the tonal range for highlights. Higher value increases tonal range of highlights and more areas will be effected by Highlights Contrast changes.
 *	`Global Contrast` edits contrast of the entire tonal range of the image. Higher value means more contrast.
 *	`Global Balance` determines the general influence on image. Higher value means overall darkening.

Adding some *Drama* is simple:

| ![][Figure032] 	| ![][Figure033] 	|
{:align="center" style="margin: 0px auto;"}

### Using ToneGear Presets
`ToneGear` comes with 2 pre defined presets.  
In order to use the *Presets* follow these steps:

 1.	Accessing the *Presets Menu* is done by click on the 3 stripes button ([Hamburger Menu](https://en.wikipedia.org/wiki/Hamburger_button)) at the top of the `PixelGear` panel.
![][Figure034]{:class="center-img"}
 2.	Click on the preset you want to use.
![][Figure035]{:class="center-img"}

The *Pre Defined Presets* are as following:

 *	**Base** – Adding gentle touch of contrast.
 *	**Deep** – Adding contrast to the deep shadows and highlights.

The user can create his own presets as well:

 1.	Set the filter sliders directly in the panel to taste (Following the guide line of course).
 2.	Open the *Preset Menu* as described above.
 3.	In the *Text Box* write the *Preset Name* and click on the `+` button.
![][Figure036]{:class="center-img"}
![][Figure037]{:class="center-img"}
 4.	To remove a preset from the list, click the `–` button next to its name.
![][Figure038]{:class="center-img"}
 5.	Click `OK` and it will be removed from the presets list. 
![][Figure039]{:class="center-img"}

## Sharpen and Enhance Edges with EdgeGear
`EdgeGear` is the nifty little tool to give the image edge above all others :-).  `EdgeGear` is smart and simple utilizing proprietary algorithm to enhance image edges.  
Basic workflow to utilize `EdgeGear` is:

 *	Select the `EdgeGear` filter, by clicking its name at the bottom of `PixelGear` panel.
![][Figure040]{:class="center-img"}
 *	Click on the `Presets Menu` button in the `EdgeGear` panel and select the preset to apply.
![][Figure041]{:class="center-img"}
 *	This will automatically create a new layer based on a merge of the current layers in your image. The filter also adds a layer mask. It is an inverted version of Skin Gear’s mask, so only non smoothed areas will be sharpened. The new layer will be named `Edge Gear` (Do not change this name, it is necessary for future editing).
![][Figure042]{:class="center-img"}
 * 	Now make the needed adjustments using the sliders.
 
{% include note.html content="You can create the new `Edge Gear` layer by dragging one of `EdgeGear`’s sliders. Using a preset to initiate the process is not mandatory." %}
 
### Enhancing Edges with EdgeGear 

 *	`Intensity` – Sets the intensity of edge enhancement. Higher values mean stronger influence of filter.
 *	`Radius` – Sets width of edges effected by filter. Higher values mean wider edges are effected.
 *	`Threshold` – Sets filter less affect noise. Lower values mean all image is effected. Higher values direct the filter to skip noise and work on edges only. Use this slider with high ISO images.

### Using EdgeGear Presets
`EdgeGear` comes with 3 pre defined presets.  
In order to use the *Presets* follow these steps:

 1.	Accessing the *Presets Menu* is done by click on the 3 stripes button ([Hamburger Menu](https://en.wikipedia.org/wiki/Hamburger_button)) at the top of the `PixelGear` panel.
![][Figure043]{:class="center-img"}
 2.	Click on the preset you want to use.
![][Figure044]{:class="center-img"}

The *Pre Defined Presets* are as following:

 *	**Low** – Subtle setup of edge enhancement; Recommended for online images.
 *	**Medium** – Stronger edge enhancement; Recommended for printed images (offset or digital).
 *	**High** – Quite a rough setup. Recommended for newspaper printed images or for special effects.

The user can create his own presets as well:

 1.	Set the filter sliders directly in the panel to taste (Following the guide line of course).
 2.	Open the *Preset Menu* as described above.
 3.	In the *Text Box* write the *Preset Name* and click on the `+` button.
![][Figure045]{:class="center-img"}
![][Figure046]{:class="center-img"}
 4.	To remove a preset from the list, click the `–` button next to its name.
![][Figure047]{:class="center-img"}
 5.	Click `OK` and it will be removed from the presets list. 
![][Figure048]{:class="center-img"}

The following image was created using `Medium` preset:

![][Figure049]{:class="center-img"}

### Sharpening vs. Enhancement
When you use small Edge `Radius` values and high `Intenisty` values, you sharpen the edges as demonstrated in the image above. If you flip the order, you get edge enhancement instead:

| ![][Figure050] 	| ![][Figure051] 	|
{:align="center" style="margin: 0px auto;"}


## Summary
Integrating all 3 filters yields:

![][Figure052]{:class="center-img"}


All the above is also available in a video:

<!--See https://jekyllrb.com/docs/includes/ https://shopify.github.io/liquid/tags/control-flow/-->
{% include youtube-embed.html id="tbUB7NWQtHw" width=960 height=540 class="center-iframe" %}

<!--<iframe class="center-iframe" width="800" height="450" src="https://www.youtube.com/embed/tbUB7NWQtHw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>-->


## Resources
 *  [Fixel PixelGear 2 Installation Guide][03].
 *  [PSKiss Blog Post - *Color and Retouch – Fast Solutions*](https://pskiss.com/color-and-retouch-fast-solutions-2/).
 *  [PSKiss Blog Post - *PSKiss PixelGear 2 – QuickStart Guide*](https://pskiss.com/retouch-pixelgear-2-quickstart-guide/).
 *  [PSKiss Blog Post - *PSKiss Pixel Gear Pro 1.5 – Free Tutorial*](http://pskiss.com/pskiss-pixel-gear-pro-free-tutorial/).  
	Tutorial about the previous version of `PixelGear`. Yet everything is still valid.

Key Words: [Fixel Algorithms][99], [Fixel][99], [Fixel PixelGear][98], [Image Enhancement][98], [Image Contrast][98], [Image Sharpening][98], [Skin Retouching][98], [Skin Smoothing][98], [Tonal Enhancement][98], [Contrast Enhancement][98], [Edge Enhancement][98], [Edge Sharpening][98], [Photoshop][99], [Plug In][99], [Photoshop Plug In][99].


<!-- This is commented out -->
  [01]: {{site.baseurl}}/news/images/FixelPixelGear2/Fixel PixelGear 2 Logo.png "Fixel PixelGear 2 Icon"
  [02]: https://pskiss.com/retouch-pixelgear-2-quickstart-guide/ "PSKiss PixelGear 2 - Quick Start Guide"
  [03]: {{site.baseurl}}/support/fixel-pixelgear-2-installation-guide.html "Fixel PixelGear 2 Installation Guide"
  [98]: https://fixelalgorithms.co/products/pixelgear/ "Fixel PixelGear 2 - Keep It Smart and Simple Tools for Photographers and Retouchers - Adobe Photoshop Plug In"
  [99]: https://fixelalgorithms.co "Fixel Algorithms"
  [Figure001]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide001.jpg "Figure 001 - Reference Image"
  [Figure002]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide002.png "Figure 002 - PixelGear 2 User Interface (UI)"
  [Figure003]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide003.png "Figure 003 - PixelGear 2 User Interface (UI) - Color Range Button"
  [Figure004]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide004.png "Figure 004 - PixelGear 2 User Interface (UI) - Color Range Dialog Box"
  [Figure005]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide005.png "Figure 005 - PixelGear 2 User Interface (UI) - Color Range Dialog Box"
  [Figure006]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide006.png "Figure 006 - PixelGear 2 Skin Selection (Marching Ants)"
  [Figure007]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide007.png "Figure 007 - PixelGear 2 User Interface (UI) - Create Mask Button"
  [Figure008]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide008.png "Figure 008 - PixelGear 2 Skin Mask in Layers Panel"
  [Figure009]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide009.png "Figure 009 - PixelGear 2 SkinGear Preset Menu"
  [Figure010]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide010.png "Figure 010 - PixelGear 2 SkinGear Preset Menu"
  [Figure011]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide011.png "Figure 011 - PixelGear 2 SkinGear Parameters"
  [Figure012]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide012.png "Figure 012 - PixelGear 2 Fine Tuning Skin Mask"
  [Figure013]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide013.jpg "Figure 013 - PixelGear 2 Fine Tuning Skin Mask"
  [Figure014]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide014.jpg "Figure 014 - PixelGear 2 Fine Tuning Skin Mask"
  [Figure015]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide015.png "Figure 015 - PixelGear 2 Fine Tuning Skin Mask"
  [Figure016]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide016.jpg "Figure 016 - PixelGear 2 Fine Tuning Skin Mask"
  [Figure017]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide017.jpg "Figure 017 - PixelGear 2 Fine Tuning Skin Mask"
  [Figure018]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide018.png "Figure 018 - PixelGear 2 Removing Skin Defects"
  [Figure019]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide019.jpg "Figure 019 - PixelGear 2 Removing Skin Defects"
  [Figure020]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide020.png "Figure 020 - PixelGear 2 Removing Skin Defects"
  [Figure021]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide021.png "Figure 021 - PixelGear 2 Adding Grain"
  [Figure022]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide022.png "Figure 022 - PixelGear 2 Adding Grain"
  [Figure023]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide023.png "Figure 023 - PixelGear 2 Using Presets"
  [Figure024]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide024.png "Figure 024 - PixelGear 2 Using Presets"
  [Figure025]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide025.png "Figure 025 - PixelGear 2 Using Presets"
  [Figure026]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide026.png "Figure 026 - PixelGear 2 Using Presets"
  [Figure027]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide027.png "Figure 027 - PixelGear 2 Using Presets"
  [Figure028]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide028.png "Figure 028 - PixelGear 2 Using Presets"
  [Figure029]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide029.png "Figure 029 - PixelGear 2 ToneGear"
  [Figure030]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide030.png "Figure 030 - PixelGear 2 ToneGear"
  [Figure031]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide031.png "Figure 031 - PixelGear 2 ToneGear"
  [Figure032]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide032.png "Figure 032 - PixelGear 2 ToneGear"
  [Figure033]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide033.jpg "Figure 033 - PixelGear 2 ToneGear"
  [Figure034]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide034.png "Figure 034 - PixelGear 2 ToneGear"
  [Figure035]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide035.png "Figure 035 - PixelGear 2 ToneGear"
  [Figure036]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide036.png "Figure 036 - PixelGear 2 ToneGear"
  [Figure037]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide037.png "Figure 037 - PixelGear 2 ToneGear"
  [Figure038]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide038.png "Figure 038 - PixelGear 2 ToneGear"
  [Figure039]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide039.png "Figure 039 - PixelGear 2 ToneGear"
  [Figure040]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide040.png "Figure 040 - PixelGear 2 EdgeGear"
  [Figure041]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide041.png "Figure 041 - PixelGear 2 EdgeGear"
  [Figure042]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide042.png "Figure 042 - PixelGear 2 EdgeGear"
  [Figure043]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide043.png "Figure 043 - PixelGear 2 EdgeGear"
  [Figure044]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide044.png "Figure 044 - PixelGear 2 EdgeGear"
  [Figure045]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide045.png "Figure 045 - PixelGear 2 EdgeGear"
  [Figure046]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide046.png "Figure 046 - PixelGear 2 EdgeGear"
  [Figure047]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide047.png "Figure 047 - PixelGear 2 EdgeGear"
  [Figure048]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide048.png "Figure 048 - PixelGear 2 EdgeGear"
  [Figure049]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide049.jpg "Figure 049 - PixelGear 2 EdgeGear"
  [Figure050]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide050.png "Figure 050 - PixelGear 2 EdgeGear"
  [Figure051]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide051.jpg "Figure 051 - PixelGear 2 EdgeGear"
  [Figure052]: {{site.baseurl}}/news/images/FixelPixelGear2/PixelGearQuickStartGuide052.jpg "Figure 052 - PixelGear 2 Final Image"
  
