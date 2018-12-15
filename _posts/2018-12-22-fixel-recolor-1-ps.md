---
title: 'Fixel ReColor 1 PS'
date: 	2018-12-22
author: Fixel Algorithms
layout: post
class:  news
hidden: true
---
![Fixel ReColor Photoshop Plug In][1]

# Fixel ReColor 1 PS Photoshop Plug In

## Background

Engineering is all about defining a problem (Supposedly interesting and solvable) and solve it.  
At Fixel, each one of the team is also a Photography Enthusiastic.  
Hence each of has encountered the following situation - Looking at great image and thinking, "*How can I recreates this colors in my image?*".  
Since we're also engineers, it seemed to us as a legitimate problem to define and try to solve.  

More than that, it is solvable and we call the solution [Fixel Recolor][98].


## Color Grading, Color Palette & Style Transfer

Color Grading is the "signature" step of a retoucher working on his images. Usually it is one of the last steps to execute which gives the image a distinct look as its creator desired.  
Color Grading has become a hot topic lately and like painters each retoucher / photographer and designer has his own Color Palette (See [Making Color Grading Easy Using Color Palettes](https://fstoppers.com/education/making-color-grading-easy-using-color-palettes-109061)) and "Brush" to do it.  
Though it has become very popular to talk about it, create tutorials, etc it was always there as one could see in [CINEMA PALETTES](https://twitter.com/CINEMAPALETTES) which shows the Color Palettes used in classic cinema movies.

So what is Color Grading?  
Basically it means remapping of colors.  
Where the target colors are composed from the Color Palette selected by the Retoucher / Photographer / Designer.
There are many way to do so (The most general mapping tool would be curves) using tools in Photoshop.  
Yet the most classic one is using [Gradient Map](https://helpx.adobe.com/il_en/photoshop/using/applying-special-color-effects-images.html#apply_a_gradient_map_to_an_image).  

![][Figure001]{:class="center-img"}

The Gradient Map of an image re maps color of the image based on their Luminosity Values.  
Usually the Gradient Map Adjustment Layer is set to Soft Light or Overlay Blend Mode.  
The colors which compose the Gradient Map are taken from the same Color Palette and are chosen according to the atmosphere one wants to create.

## Fixel Recolor 1 PS

### Under the Hood - Analyze, Extract, Use (Color Grading / Color Mapping / Style Transfer)

### User Interface (UI)
[Show UI and Explain Buttons]

### Tips & Tricks

[Number of Samples]  
[Grab from Internet - Windows]  
[Editing and Shuffling Palettes / Colors]

## Real World Examples





As one could see in the figure above, [Fixel Zone Selector][2] can generate Luminosity Masks which are arbitrary to the user will while being:
 * 	Focused - Can target specific luminosity level.
 *	Smooth - The curve is smooth (Using 32 Bit Float calculations regardless of the image) with no quantization error.
 *	Direct - Works directly on the image without overhead of calculations or sensitivity to the Gray Scale Color Profile of Photoshop.

Namely, [Fixel Zone Selector][2], by utilizing its own Luminosity Mask Generator, can overcome all issues mentioned above in Photoshop.  
Since it has a simple, intuitive, yet powerful UI, the user can have an effective tool to totally control the Luminosity Mask generation process.

## Summary
[Fixel Recolor 1 PS][98] introduces a new functionality which has never been available in Photoshop before - Automatic, Machine Learning Powered, analysis of image Color Palette.  
Once the user (Be a Photographer or Designer) has such a functionality it can be used in many ways.  
We tried making the UI of [Fixel Recolor 1 PS][98] intuitive and supportive of a user friendly workflow to use this capability to create user presets for Color Palettes, Integrate Colors into Photoshop (Swatches) and most of all - Recolor / Color Grade / Style Transfer the image.



**Remark**  

## Image Credit
 *  [Lighthouse Image](https://www.flickr.com/photos/magnetismus/8399258607/) - Credit to [magnetismus](https://www.flickr.com/people/magnetismus/).
 *  [Schwaigsee Lake](https://www.freeimages.com/photo/schwaigsee-lake-1342788) - Credit to [Alfred Borchard](https://www.freeimages.com/photographer/Alfi007-51075).
 *  [Simple Living](https://www.flickr.com/photos/lightsamples/22552453147) - Credit to [Malcolm Carlaw](https://www.flickr.com/photos/lightsamples/).


## Resources
 *  [LZeven Design - Color Grading with Gradient Maps in Photoshop](https://zevendesign.com/color-grading-gradient-maps-photoshop/).
 *  [Photoshop Cafe - How to Color Grade a Photo Using Gradient Maps in Photoshop](https://photoshopcafe.com/color-grade-photo-using-gradient-maps-photoshop/).
 *  [Retouching Academy - Using Gradient Maps to Color Grade Your Photographs](https://retouchingacademy.com/using-gradient-maps-to-color-grade-your-photographs/).
 *  [PHLEARN - How to Color Tone Using Gradient Maps](https://phlearn.com/tutorial/color-tone-using-gradient-maps/).
 *	[Do It Yourself (DIY) Photography - Add Different Looks to Your Photos Using Only Gradient Map Layer](https://www.diyphotography.net/add-different-looks-photos-using-gradient-map-layer/).
 *	[FStoppers - Quick Tips on How to Color Grade Your Photos Using Gradient Maps](https://fstoppers.com/education/quick-tips-how-color-grade-your-photos-using-gradient-maps-201756).
 *	[FStoppers - Making Color Grading Easy Using Color Palettes](https://fstoppers.com/education/making-color-grading-easy-using-color-palettes-109061).

Key Words: [Fixel Algorithms][99], [Fixel][99], [Fixel Recolor][98], [Color Grade][98], [Color Grading][98], [Color Mapping][98], [Style Transfer][98], [Color Palette][98], [Photoshop][99], [Plug In][99], [Photoshop Plug In][99].


<!-- This is commented out -->
  [1]: {{site.baseurl}}/news/images/LuminosityMask001/BlogPostIcon.png "Luminosity Mask 001"
  [2]: {{site.baseurl}}/products/zoneselector/ "Fixel Zone Selector 1 PS Product Page"
  [3]: {{site.baseurl}}/news/2018/03/luminosity-mask-001 "Luminosity Mask - How Does It (Really) Works?"
  [4]: http://fotographee.com/tutorial-image-editing-luminosity-masks/ "Luminosity Mask: The Complete Kickstarter’s Guide"
  [5]: https://www.youtube.com/watch?v=xvjno4d8uJ8 "How to Generate the Classic Luminosity Masks Using Mask / Channel Operations (Add, Subtract, Intersect [Multiply])"
  [98]: https://fixelalgorithms.co/products/recolor/ "Fixel ReColor - Recoloring, Color Grading and Style Transfer for Photographers and Designers - Adobe Photoshop Plug In"
  [99]: https://fixelalgorithms.co "Fixel Algorithms"
  [Figure001]: {{site.baseurl}}/news/images/FixelReColor1Ps/PhotoshopGradientMap.png "Figure 001 - Photoshop Gradient Map Tool & Color Palette"
  [Figure002]: {{site.baseurl}}/news/images/FixelReColor1Ps/SimpleLiving.png "Figure 002 - Real World Reference Image"
  [Figure003]: {{site.baseurl}}/news/images/FixelReColor1Ps/PhotoshopColorSettings.png "Figure 003 - Photoshop Color Profile Settings"
  [Figure004]: {{site.baseurl}}/news/images/FixelReColor1Ps/ColorProfileOutputValue.png "Figure 004 - Photoshop Color Profile - Pixel Values"
  [Figure005]: {{site.baseurl}}/news/images/FixelReColor1Ps/GeneratingLightDarkMidCorrectColorSpace.png "Figure 005 - Luminosity Masks Light, Dark and Mid Under Correct Color Profile Settings"
  [Figure006]: {{site.baseurl}}/news/images/FixelReColor1Ps/GeneratingLightDarkMidWrongColorSpace.png "Figure 006 - Luminosity Masks Light, Dark and Mid Under Wrong Color Profile Settings"
  [Figure007]: {{site.baseurl}}/news/images/FixelReColor1Ps/PhotoshopDotGainVsFixelLuminosityMaskAnimated.png "Figure 007 - Luminosity Masks - Photoshop (Color Profile - Dot Gain 20%) vs. Theory (Fixel)"
  [Figure008]: {{site.baseurl}}/news/images/FixelReColor1Ps/PhotoshopSGrayVsFixelLuminosityMaskAnimated.png "Figure 008 - Luminosity Masks - Photoshop (Color Profile - sGray) vs. Theory (Fixel)"
  [Figure009]: {{site.baseurl}}/news/images/FixelReColor1Ps/FixelZoneSelectorParametersAnimated.png "Figure 009 - Luminosity Masks - Fixel Zone SelectorMask Generation Capabilities"
