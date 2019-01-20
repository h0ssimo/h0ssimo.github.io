---
title: 'Quick Tips: How To Create Cloth Material In ZBrush'
date: 2019-01-12 15:46:26 +0330
layout: post
excerpt: In this quick article, I'm gonna go over how to create a cloth material in
  ZBrush for your presentations. It really helps to sell your concepts to your directors.
tags:
- article
- quick-tips
- tutorial
categories:
- tutorial
image: "/images/Tutorials/Quick_Tips/How_to_Create_Cloth_Material_in_ZBrush/how_to_create_cloth_material_in _zbrush_header.jpg"
image-sm: "/images/Tutorials/Quick_Tips/How_to_Create_Cloth_Material_in_ZBrush/how_to_create_cloth_material_in _zbrush_header.jpg"
featured: true
showtags: true

---
It's really a good idea to present our characters before going further in the pipeline. This way, the directors in charge, can have a clearer idea of how it's gonna look in the end, and change some stuff if they need to. It's much easier to change stuff at this stage anyways.

In bigger production pipelines, it's a crucial task to check the concepts regularly. However, while it's totally acceptable to even share a _ZBrush_ screenshot, or a quick _BPR_ render, it's more appealing to present the art in style.

One aspect is the materials. Here, I'm gonna go step by step, over how I create cloth material for my concept presentations. Hope it comes handy for you guys as well.

### The Concept Behind This Method

It's really simple: pop out the cloth details, and make a **_fresnel_** look in your material. While _ZBrush_ is not a real rendering engine, it has its own tools to help us create what we want.

### Step By Step Guide

OK, so you have your cloth sculpt/simulation imported in _ZBrush_. Make sure that you have a nice _UV layout_ for your cloth piece. It's only needed for the cloth details, so don't worry if you only need to use the material I'm gonna talk about.

<img src="/images/Tutorials/Quick_Tips/How_to_Create_Cloth_Material_in_ZBrush/01_base_cloth_sculpt_simulation.jpg" alt="01_base_cloth_sculpt_simulation" class="narrowResponsive">

First, let's add cloth texture on top of what we have, using the _Noise_ maker under the _Surface_ menu. You need proper _UV layout_, and a good tileable _displacement_ texture map for this step. Open the _NoiseMaker_, the plug the disp image on the bottom left, where it says _Alpha On/Off_. Then, zero out the _Mix Basic Noise_ slider to get rid of the unwanted noise. Then play with the sliders to get your desired _Strength_ and _Scale_. The important part here could be underestimating the power of _ColorBlend_ slider. Put it to a negative value to add more depth to your cloth's look.

These are the settings I have in the _NoiseMaker_ window:

<img src="/images/Tutorials/Quick_Tips/How_to_Create_Cloth_Material_in_ZBrush/02_noise_maker_settings.jpg" alt="02_noise_maker_settings" class="narrowResponsive">

Now, the real trick; the material. With your _BasicMaterial_ selected, go to the _Material_ menu, and click on _CopySH_ under the _Modifiers_ sub-menu, to copy the shader. Now, choose _DoubleShade1_ material in the _Standard Materials_ palette.

If you have troubles previewing the material on your model, just make sure that the little brush button is turned off the _Subtool_ menu. Now, you're on track.

Next, while the _DoubleShade1_ active, click on _PasteSH_ under the _Modifiers_ sub-menu in the _Material_ menu. Note that since this is a double shader, you have two slots named _S1_ and _S2_. Click on _S2_, and _PasteSH_ again. After that, with _S2_ selected, crank up the _Diffuse_ slider and go to the _Mixer_ menu, then crank up the _Fresnel_ slider as well. _BOOM_! That's the trick! Now, it's only a matter of playing with _Diffuse_, _Specular_ and _Ambient_ sliders of the slot 1 (_S1_) to get what you're looking for. Usually, I keep all of them low.

<img src="/images/Tutorials/Quick_Tips/How_to_Create_Cloth_Material_in_ZBrush/03_double_shader_settings.jpg" alt="03_double_shader_settings" class="narrowResponsive">

Just so you know, you can use other multiple shaders as well; just turn off the extra slots and the rest is the same as explained.

This is the _ZBrush_ screenshot of what I got:

<img src="/images/Tutorials/Quick_Tips/How_to_Create_Cloth_Material_in_ZBrush/04_zbrush_screenshot.jpg" alt="04_zbrush_screenshot" class="narrowResponsive">

This is a quick _BPR_ render I composited in _Photoshop_:

<img src="/images/Tutorials/Quick_Tips/How_to_Create_Cloth_Material_in_ZBrush/05_final_render.jpg" alt="05_final_render" class="narrowResponsive">

Remember, if you're gonna render it using _BPR_, apply the noise to the mesh, and colorize the cavities to pop the details out in the render as well.

That's it. Thanks for reading another article of mine. Hope it's worth your time.

Cheers!