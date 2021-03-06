---
title: 'Workflow: How to Create Roughness / Glossiness Map For Our Character'
date: 2019-01-06 00:00:00 +0000
layout: post
excerpt: In this article, I'm gonna go over my workflow on how I create a quick but
  good-looking Glossiness/Roughness Map for my characters. It's a solid starting point
  to build on.
tags:
- article
- tutorial
- workflow
categories:
- articles
image: "/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/How_to_Create_Roughness_Glossiness_Map_for_our_Character_Header.jpg"
image-sm: "/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/How_to_Create_Roughness_Glossiness_Map_for_our_Character_Header.jpg"
featured: true
showtags: true
permalink: "/tutorial/how-to-create-roughness-glossiness-map-for-our-character/"
---
OK, so you have your character sculpt ready for the next step. Most of the maps needed for real time renders or rendering engines like _Renderman_, _VRay_, _Arnold_, etc. are straight forward to create. I mean their processes are clear enough. However, creating roughness/glossiness map is probably not one of them for most artists. There are several ways of creating it, but first, let me quickly go over the little, confusing difference between the _glossiness map_ and the _roughness map_.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/01_head_sculpt.jpg" alt="01_head_sculpt" class="responsive">

### Glossiness Map VS. Roughness Map

It’s really simple, one is the inverted version of the other. Why don’t we just stick to one of them? Better ask the engineers working behind the rendering engines! So, for example if you create glossiness map, well, congrats, you have the other one as well. All it takes is to open it _Photoshop_, and press _Ctrl+I_. That’s it.

It’s the target engine that determines which one to use. For example, the _Unreal Engine 4_ (_UE4_), uses _Roughness_ as its standard workflow, and _Marmoset Toolbag_, uses _Glossiness_ as its standard.

In this article, I’m gonna show you a way to quickly create a good looking base for our glossiness map, then in the end, I’ll invert it to create roughness map as well.

### The Concept Behind This Workflow

Basically, all I do is to combine a specific version of the _displacement map_ of my character, and its _cavity map_. That’s about it.

The displacement map is used to cover the general areas of the head, and the cavity map is used to bring out those little sculpting details like skin pores, and helps to pop them out.

So, enough talking, let’s do this.

### Detailed Steps of Creating Glossiness Map

First, make sure you have no sculpting layers by baking all of them (if you have any). If you don’t do this step, probably you’re gonna have trouble painting your maps on your character.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/02_baking_layers.jpg" alt="02_baking_layers" class="narrowResponsive">

Then, fill your model with white color.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/03_fill_color.jpg" alt="03_fill_color" class="narrowResponsive">

First, we’re gonna create the _Cavity Map_. For that, click on _Mask By Cavity_ in _Masking_ menu. Then, _Ctrl+Click_ on an empty space to invert the mask.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/04_mask_by_cavity.jpg" alt="04_mask_by_cavity" class="narrowResponsive">

You should have something that looks like the image below. If you don’t get a similar result (though it really depends on your model), try to play with the _Cavity Map_ settings. Most important one of them being the _Cavity Profile_. And then try again.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/05_head_masked.jpg" alt="05_head_masked" class="narrowResponsive">

Now, all we need to do, is to fill the selected area in black.

This is how the _Cavity Map_ should look like. Later, other than what we do with it here, it will have an important role to play when it comes to rendering, whether real-time, or pre-processed.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/06_cavity_map.jpg" alt="06_cavity_map" class="narrowResponsive">

Now, it’s time to create it. But before that, remember that you should already have your final _UV Layout_. Also, in _ZBrush_, check you _UV Map_ resolution and make it the size that you want. I usually go for the maximum 8K.

OK, everything’s set. Click on _New From Polypaint_ under the _Texture Map_ menu.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/07_creating_texture.jpg" alt="07_creating_texture" class="narrowResponsive">

Then, you need to clone your texture to be able to export it. Click on _Clone Txtr_ to clone it.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/08_cloning_texture.jpg" alt="08_cloning_texture" class="narrowResponsive">

Before exporting, you need to flip the texture vertically. Because as you know, the UV workflow in _ZBrush_ is inverted vertically in comparison to what you have in other 3D packages like _Maya_, _3Ds Max_ and _Blender_.

Click on _Export_, and choose the format that you want. I’ll stick with ._PSD_ for now.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/09_exporting_texture.jpg" alt="09_exporting_texture" class="narrowResponsive">

So, the _Cavity Map_ is done. Now it’s time for the other map that we need; which is a _mid-value displacement map_.

Alright. Let me give you an idea about it all. The whole idea here is, to put your model’s SDiv near half of what you have, and create a _Displacement Map_ from there. My model has 6 subdivision levels and 14.2 million polygons. So I’m gonna put it on half-way through the subdivisions, like SDiv 3 and create the _Displacement Map_. This way, I prevent having too much (almost noisy details) in my _Glossiness Map_ and cover the bigger shapes of the head.

I hope I’m clear, but don’t worry if it’s not the case, it will make sense in the end.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/10_subdivision_level.jpg" alt="10_subdivision_level" class="narrowResponsive">

So, After putting the SDiv level of your model to half, click on _Create DispMap_ under the _Displacement Map_ menu.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/11_creating_disp_map.jpg" alt="11_creating_disp_map" class="narrowResponsive">

Now, like before, we need to clone it. Click on _Clone Disp_.

Before exporting _Displacement Map_, flip it vertically and then click on _Export_ and save it.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/12_exporting_disp_map.jpg" alt="12_exporting_disp_map" class="narrowResponsive">

This is where the magic happens! In _Photoshop_! Yup, it’s time to combine the two.

First, fill the _Background_ layer with **%60** grey. Then, import the _Displacement Map_ on top of it, and put the opacity to something like **%70**. Next, import the _Cavity Map_ and put the opacity to something like **%25**. Then add a _Levels_ adjustment specifically on top of it and input something around **1.50** on the _midtone_ section to make it a bit lighter in _midtone_ areas.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/13_photoshop_composite.jpg" alt="images/13_photoshop_composite" class="responsive">

After that, I usually group everything except the _Background_ layer and darken it a bit more using a _Brightness/Contrast_ adjustment layer. It’s usually enough to put the brightness value to somewhere around **-40**.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/14_photoshop_adjustment_layer.jpg" alt="14_photoshop_adjustment_layer" class="responsive">

That’s all. Now you have your _Glossiness Map_ ready to put to test. This is obviously a back-and-forth process, the numbers I mentioned are based on my experience and my workflow. You could always change some stuff in _Photoshop_ and then test it again to achieve what you really like. This method is usually good as a starting point; meaning for example if your character have scars or is sweaty, you could start creating a basic _Glossiness Map_ using the method that I talked about in this article, and then take it to a PBR painting program like _Substance Painter_, and paint the desired _Glossiness_ on top of the current one as the need arises.

This is how my final composited _Glossiness Map_ looks like. It's also worth mentioning that the empty space in the _UV layout_, is for the hands, which I did not cover in this article.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/15_glossiness_map.jpg" alt="15_glossiness_map" class="narrowResponsive">

As I mentioned earlier, to get the _Roughness Map_, it’s only a matter of inverting the colors of the _Glossiness Map_.

(_Flatten_ the image in _Photoshop_, and then press _Ctrl+I_ to invert it.)

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/16_roughness_map.jpg" alt="16_roughness_map" class="narrowResponsive">

Here’s the final real-time render I got in _Marmoset Toolbag 3.04_.

<img src="/images/Tutorials/Workflow/How_to_Create_Roughness_Glossiness_Map_for_our_Character/17_head_final_render.jpg" alt="17_head_final_render" class="responsive">

Thanks for reading this article everyone. I hope you got away with something out of all this.

Feel free to let me know your feedback and ask me your questions in the comments.

Cheers!