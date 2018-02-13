---
title: 'Luminosity Mask - How Does It (Really) Works?'
date: 	2017-11-30
author: Fixel Algorithms
layout: post
class:  news
---
![Small Luminosity Mask Icon][1]

Everywhere you go you hear Luminosity Masks.  
I'm really surprised it doesn't have its own Wikipedia Page (Maybe we'll take care of that).  
It is a truly great tool to have in your toolbox.

But how it works? Not in the sense how to create it, but really what happens?  
Well, let's try answering that and doing it deep (Hopefully interesting).

## The Basics

### Step 001 - It All Starts with a Grayscale Image
You can have image with all colors in the world but the first step in creating Luminosity Mask is by having a Grayscale image (Single Channel Image).
In most cases it means to calculate the Luminosity Channel of the given image.  
Each one with his recipe (Most actions / panels based solution uses Photoshop Luminosity selection - **Add Link**).

![Figure 001][Figure001]

By the way, any "Single Channel" image can do here. Namely one could use the Blue channel of RGB image as the base image for the creation of Luminosity Mask.  
Be crazy with that, anything can be a candidate (Yea, even the M channel in CMYK).

Well, in case of a grayscale image, one could just step over to Step 002.

### Step 002 - Apply Pixel Wise Transformation on the Grayscale Image

Now, this is the step you get to trick the system.  
The idea is very simple, given the Gray Scale image as input the output, per pixel, is a function only of its value.  
Well, this sentence might take some of us back to horrible school days but it is really simple when you think about it.  
Pixel comes in, says its value and get output value and voilà we have a Luminosity Mask.

![Figure 002][Figure002]

The above "Mask Generator" seems to be generating a "Midtones Mask" since the output values for Mid Tone Values is high value.  


**2 main approaches, Calculations / Curves [Show they are equivalent]**

Curves in Photoshop
Advantages
 *  No limits what so ever on the shape of the selection.
 *  Integration of multi selections can be done on the curve level (Less computation).
 *  Smoothness of the LUT is independent of the mode (8 / 16 / 32 Bit).

Disadvantages
 *  Less Smooth
    Usually the functions are parameterized by small number of control numbers
    Moreover Photoshop Curves are quantized into [Ask Davide] levels.
 *  fd

**Show **

![Fixel EdgeHancer Edge Mask][7]{:class="center-img"}
*Image Credit - [Image by Tanja Heffner][8]*.

The radius parameter controls the width of the effect on edge areas.  
Which is exactly what one would expect to achieve with such parameter.

Targeting edges directly is the special sauce of EdgeHancer which makes its end result different than traditional sharpening.  
This approach works beautifully on textures and images with pronounced edges.  
You really should try it by yourself.

Next time we'll cover Fixel EdgeHancer UI and settings.

Key Words: [Fixel Algorithms][2], [Fixel][2], [Fixel Zone Selector][2], [Luminosity Mask][2],  [Luminosity Masks][2], [Curves][2], [Levels][2], [Luminosity][2], [Photoshop][2].


<!-- This is commented out -->
  [1]: {{site.baseurl}}/news/images/FixelEdgeHancer2/FixelEdgeHancer2Icon150px.png "Fixel EdgeHancer 2"
  [2]: {{site.baseurl}}products/edgehancer/ "Fixel EdgeHancer 2 Product Page"
  [3]: http://www.davidebarranca.com "Davide Barranca - Photoshop, etc."
  [4]: http://www.davidebarranca.com/2012/09/decomposing_sharpening_part_1/ "Decomposing Sharpening #1 Introduction"
  [5]: http://www.davidebarranca.com/2013/01/double-usm-photoshop-sharpening-script-1-introduction/ "Double USM Photoshop Sharpening Script #1: Introduction"
  [6]: {{site.baseurl}}/news/images/FixelEdgeHancer2/SharpeningInputImageAnimated.png "Classic Image Sharpening"
  [7]: {{site.baseurl}}/news/images/FixelEdgeHancer2/EdgeMaskRadiusAnalysisAnimated.png "Fixel EdgeHancer Edge Mask"
  [8]: https://unsplash.com/photos/rNBYe4QlAIQ "Image by Tanja Heffner"
  [Figure001]: Diagram001.png "Figure 001 - Extracting Luminosity Channel from RGB Image"
  [Figure002]: Diagram002.png "Figure 002 - Mapping Grayscale Image into Luminosity Mask"
