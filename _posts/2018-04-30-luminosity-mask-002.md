---
title: 'Luminosity Mask Done Right!'
date: 	2018-04-30
author: Fixel Algorithms
layout: post
class:  news
hidden: true
---
![Luminosity Mask 001][1]

In our previous post [Luminosity Mask - How Does It (Really) Works?][3] we explained the theory behind Luminosity Mask.  
Which basically sums to the fast that Luminsoity Mask is a remapping of values of a graysacle imgae.

In this post, as promised in the end of previous post, we will explore what happens behind Photoshop's Luminosity Mask generators.  
We will see that utilizing Photoshop's engine to create Lumijnsoity Masks in the method used by most create some artifact we better avoid.  
In orde to show how to avoid them we'll suggest an idea and an implementation in the form of a Photoshop Plug In named - Fixel Zone Selector.

We will also talk about the trade off in the essence of each Luminsoity Mask - Smooth vs. Narrow.

## Refrence Image
This tutorial will include many tests in Photoshop.  
Hence a Reference Image is needed.

![](https://i.imgur.com/DFBCk5C.png){:class="center-img"}

The image a bove is a perfect Grayscale Gradient of 8 Bit Image made programmatically.  
It contains all values {0, 1, 2, ..., 254, 255}. The red box contians the line which will be processed as one dimensional function. This will assist us analyze what heppens exactly on every single Photoshop operation done.

[Grayscale Gradient]

[Base Image (From previous post)]

## Grayscale and Coloe Modes Gamma Settings in Photoshop

![](https://i.imgur.com/IeyrYna.png){:class="center-img"}

[sGray Color Mode](http://retrofist.com/sgray/)

Output comparison

![](https://i.imgur.com/mcnGYL4.png)

## The Classic Luminosity Masks

[Show each of the 15 Luminosity Masks - Photoshop vs. Theory]
[Show Photoshop's artifacts]

## Image Credit
 *  [Lighthouse Image](https://www.flickr.com/photos/magnetismus/8399258607/) - Credit to [magnetismus](https://www.flickr.com/people/magnetismus/).
 *  [Schwaigsee Lake](https://www.freeimages.com/photo/schwaigsee-lake-1342788) - Credit to [Alfred Borchard](https://www.freeimages.com/photographer/Alfi007-51075).
 *  [Simple Living](https://www.flickr.com/photos/lightsamples/22552453147) - Credit to [Malcolm Carlaw](https://www.flickr.com/photos/lightsamples/).


## Resources
 *  [Luminosity Mask: The Complete Kickstarter’s Guide](http://fotographee.com/tutorial-image-editing-luminosity-masks/).
 *  [Video - How to Generate the Classic Luminosity Masks Using Mask / Channel Operations (Add, Subtract, Intersect [Multiply])](https://www.youtube.com/watch?v=xvjno4d8uJ8).
 *  [Video - How to Generate the Classic Luminosity Masks Using Calculations (16 Bit Mode)](https://www.youtube.com/watch?v=43JbFIOckrM).
 *  [Video - Selecting Using Luminosity Masks (Using Curve Tool)](https://www.youtube.com/watch?v=la-zWPwjuQw).


<!-- This is commented out -->
[comment]: # (https://fstoppers.com/education/how-create-luminosity-masks-better-retouching-111111 for Luminosity Mask using Calculations.)
[comment]: # (https://www.capturelandscapes.com/introduction-to-luminosity-masks/.)
[comment]: # (https://fstoppers.com/composite/create-seamless-selections-using-luminosity-masks-159068.)
[comment]: # (https://www.psdbox.com/tutorials/complex-masking-using-channels-and-calculations.)
[comment]: # (https://www.youtube.com/watch?v=t3zSUK7KK7c)
[comment]: # (https://www.youtube.com/watch?v=htuf4yaanBI)
[comment]: # (http://play.macprovideo.com/photoshop-102-selection-masking-techniques/12)
[comment]: # (https://www.youtube.com/watch?v=QUkIgdmnBaE)
[comment]: # (http://fotographee.com/luminosity-masks-gradient/ See shortcuts for operations on Masks)
[comment]: # (https://www.youtube.com/watch?v=XGe_YC5dIwI Gamma in Luminosity Masks)

Key Words: [Fixel Algorithms][2], [Fixel][2], [Fixel Zone Selector][2], [Luminosity Mask][2],  [Luminosity Masks][2], [Saturation Mask][2], [Saturation Masks][2], [Curves][2], [Levels][2], [Luminosity][2], [Photoshop][2], [Plug In][2].


<!-- This is commented out -->
  [1]: {{site.baseurl}}/news/images/LuminosityMask001/BlogPostIcon.png "Luminosity Mask 001"
  [2]: {{site.baseurl}}/products/zoneselector/ "Fixel Zone Selector 1 PS Product Page"
  [3]: {{site.baseurl}}/news/2018/03/luminosity-mask-001 "Luminosity Mask - How Does It (Really) Works?"
  [Figure001]: {{site.baseurl}}/news/images/LuminosityMask001/GrayScaleImageGeneration.png "Figure 001 - Extracting Luminosity Channel from RGB Image"
  [Figure002]: {{site.baseurl}}/news/images/LuminosityMask001/MaskGenerator.png "Figure 002 - Mapping Grayscale Image into Luminosity Mask"
  [Figure003]: {{site.baseurl}}/news/images/LuminosityMask001/LuminosityMaskShowCaseAnimated.png "Figure 003 - Luminosity Mask Generation"
  [Figure004]: {{site.baseurl}}/news/images/LuminosityMask001/PhotoshopCurveTool.png "Figure 004 - Photoshop Curve Tool"
  [Figure005]: {{site.baseurl}}/news/images/LuminosityMask001/LuminosityMaskRecipesAnimated.png "Figure 005 - Luminosity Masks Recipes"
