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

Color Grading is the "signature" step of a Retoucher working on his images. Usually it is one of the last steps to execute which gives the image a distinct look as its creator desired.  
Color Grading has become a hot topic lately and like painters each Retoucher / photographer and designer has his own Color Palette (See [Making Color Grading Easy Using Color Palettes](https://fstoppers.com/education/making-color-grading-easy-using-color-palettes-109061)) and "Brush" to do it.  
Though it has become very popular to talk about it, create tutorials, etc it was always there as one could see in [CINEMA PALETTES](https://twitter.com/CINEMAPALETTES) which shows the Color Palettes used in classic cinema movies.

So what is Color Grading?  
Basically it means remapping of colors.  
Where the target colors are composed from the Color Palette selected by the Retoucher / Photographer / Designer.
There are many way to do so (The most general mapping tool would be curves) using tools in Photoshop.  
Yet the most classic one is using [Gradient Map](https://helpx.adobe.com/il_en/photoshop/using/applying-special-color-effects-images.html#apply_a_gradient_map_to_an_image).  
The Gradient Map of remaps image colors based on their Luminosity Values.  

![][Figure001]{:class="center-img"}

As can be seen in Figure 001 the Grayscale Gradient was recolored by the Gradient Map (Built with certain color palette) according to the brightness of the gray color.  

Usually the Gradient Map Adjustment Layer is set to Soft Light or Overlay Blend Mode as one doesn't want full replacement of the colors but just a subtle .  
The colors which compose the Gradient Map are taken from the same Color Palette and are chosen according to the atmosphere one wants to create.

How do we create a good color palette?  
Well, some of us just has it, some used color palettes form others and some just guess.  
We had 2 things to say about it:

 1.	There are plenty of examples out there which are great example of a great Color Palette.
 2.	There are Machine Learning based algorithms to extract Color Palette from a good example.
 
Namely, given a good example, can we transfer its Color Style (Style Transfer) to our target image?  
Moreover, can we use it to create a Color Palette and use it when we want?
 
Indeed we can. All needed was to adapt those algorithms and fine tune them into the problem we started with.  
Namely, Analyze a Reference Image, Extract a Color Palette from it, Apply the Color Palette in the Color Grading process of the Target Image.  
Namely, Color Palette Transfer from any image which inspire you to any image you would like!

## Fixel Recolor 1 PS

So, ~4 years ago we started working on this problem - How to Extract a Color Palette from Reference Image and apply it on a Target Image.  
We wanted a fully Automatic Process based on Machine Learning algorithms.  
Some can do it manually, as seen in [CINEMA PALETTES](https://twitter.com/CINEMAPALETTES), but we wanted to be able to do it in a modern manner with smooth workflow within Photoshop.

### Under the Hood - Analyze, Extract, Use (Color Grading / Color Mapping / Style Transfer)

### User Interface (UI)
[Show UI and Explain Buttons]

### Tips & Tricks

[Number of Samples]  

The first instinct is to chose the highest number. we are all sold by higher and higher values.  
Yet a good rule of thumb before setting the number of Color Samples to extract (JUsing Image Analysis) into the Color Palette would be asking yourself - *If I had painted this image, how many different colors, which I know their names, would have I used?*.  
The emphasize here is on *colors I know their name*. This simple trick will get you much better results using [Fixel ReColor][98].

[Grab from Internet - Windows]  

There is a nice feature added into [Fixel ReColor][98] once it is used in Windows. Actually it is Windows' feature but still it is nice to know about.  
When the user sets the Mode (Source) to `File` and hit `Analyze` a File Picker Dialog is opened. This dialog window is the native File Picker of the operating system.  
Nice feature of the File Picker in Windows is being able to grab files from the Internet - HTTP Address.  
So let us say you like an image on the Internet and you want to use it as the Reference Image then:

 1.	Copy the HTTP address of the image.  
	For isnatnce, use the image of the [Eiffel Tower](https://en.wikipedia.org/wiki/Eiffel_Tower) from Wikipedia - `https://upload.wikimedia.org/wikipedia/commons/8/85/Tour_Eiffel_Wikimedia_Commons_%28cropped%29.jpg`.
 2.	Select the number of Color Samples to analyze in [Fixel ReColor][98].
 3.	Configure [Fixel ReColor][98] to use `File` as source.
 4.	Hit the `Analyze` button and paste the HTTP address in the File Picker address.

Once you do that the output Color Palette would be the result of the analysis of the image from the Internet.  
It doesn't work on macOS as the File Picker in macOS doesn't support inserting HTTP addresses.

[Editing and Shuffling Palettes / Colors]

We worked hard on the UI. Our motto was - Interactive Creative UI.  
It means that any the user can interact with any element of the UI - Palettes and Color Swatches.  
In our test group some (Minority) people missed some capabilities of the UI - Editing / Shuffling Palettes and Color Swatches.  
So let us notify you that the following can be done:

 1.	Palette Context Menu  
 	Using the 3 Dots button at the right end of each palette will open a menu with the option to shuffle the colors of the palette.  
 	It means that hitting this button will add randomness to each color of the palette - A random small shift of the color.  
	There also many other options in that menu (Well, Color Grading is there!).
 2.	Drag & Drop  
 	You may use Drag & Drop to reorder colors within a palette and even to move colors from one palette to another one.  
	You may also Drag & Drop to reorder the presets you saved.
 3.	Color Context Menu  
 	Use Right Click on the Color Swatches. It will allow you to edit the color, save it to Photoshop's swatch or, god forbidden, delete it.

## Real World Examples

[Show animation of the whole process]

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
 *  [Zeven Design - Color Grading with Gradient Maps in Photoshop](https://zevendesign.com/color-grading-gradient-maps-photoshop/).
 *  [Photoshop Cafe - How to Color Grade a Photo Using Gradient Maps in Photoshop](https://photoshopcafe.com/color-grade-photo-using-gradient-maps-photoshop/).
 *  [Retouching Academy - Using Gradient Maps to Color Grade Your Photographs](https://retouchingacademy.com/using-gradient-maps-to-color-grade-your-photographs/).
 *  [PHLEARN - How to Color Tone Using Gradient Maps](https://phlearn.com/tutorial/color-tone-using-gradient-maps/).
 *	[Do It Yourself (DIY) Photography - Add Different Looks to Your Photos Using Only Gradient Map Layer](https://www.diyphotography.net/add-different-looks-photos-using-gradient-map-layer/).
 *	[FStoppers - Quick Tips on How to Color Grade Your Photos Using Gradient Maps](https://fstoppers.com/education/quick-tips-how-color-grade-your-photos-using-gradient-maps-201756).
 *	[FStoppers - Making Color Grading Easy Using Color Palettes](https://fstoppers.com/education/making-color-grading-easy-using-color-palettes-109061).

Key Words: [Fixel Algorithms][99], [Fixel][99], [Fixel Recolor][98], [Color Grade][98], [Color Grading][98], [Color Mapping][98], [Style Transfer][98], [Color Palette][98], [Photoshop][99], [Plug In][99], [Photoshop Plug In][99].


<!-- This is commented out -->
  [01]: {{site.baseurl}}/news/images/LuminosityMask001/BlogPostIcon.png "Luminosity Mask 001"
  [02]: {{site.baseurl}}/products/zoneselector/ "Fixel Zone Selector 1 PS Product Page"
  [03]: {{site.baseurl}}/news/2018/03/luminosity-mask-001 "Luminosity Mask - How Does It (Really) Works?"
  [04]: http://fotographee.com/tutorial-image-editing-luminosity-masks/ "Luminosity Mask: The Complete Kickstarter’s Guide"
  [05]: https://www.youtube.com/watch?v=xvjno4d8uJ8 "How to Generate the Classic Luminosity Masks Using Mask / Channel Operations (Add, Subtract, Intersect [Multiply])"
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
