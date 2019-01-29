---
layout: post
title: 'Workflow: How To Create Texture Map For Game Hair Cards Using XGen'
excerpt: In this article, I'm gonna quickly go over my workflow of creating texture
  maps for game hair cards as well as some tips on using Maya's excellent XGen system.
  I guess it's easier than what you think.
date: 2019-01-29 00:00:00 +0330
tags:
- article
- tutorial
- workflow
- maya
categories:
- tutorial
image: "/images/how_to_create_texture_map_for_game_hair_cards_using_xgen_header.jpg"
image-sm: "/images/how_to_create_texture_map_for_game_hair_cards_using_xgen_header.jpg"
featured: true
showtags: true

---
Game hair has always been an interesting topic to talk about because of all the challenges it produces along the way. Every artist have their own way of handling them. But in general, there are only a few methods in terms of creating the texture sheet. One robust and flexible workflow, is to use Maya's XGen system. I know, XGen may seem a bit tricky to understand at first glance, but once you're there, it's really easy to get the most out of it.

I have to say though, since it contains a lot of steps, I can only go over important parts. But, the good news is I share some tricks as well, which may help you troubleshoot your situation.

### The Ultimate Goal

In short, we need to render out an image like the one below:

We need thick hair, to create the silhouette and cover most of the head; thinner hair for adding breakups and tinier shapes, and finally some thin strand groups and flyaways to add more details to the hair.

### Overall Workflow

We're gonna use a simple plane geometry for every hair group to grow from, and then will hide them in the end. Then, go to an orthographic camera, like the front cam, and set the render output resolution to a square size. I'll go with 4K, which means -as you know- 4096*4096. Then assign an appropriate hair shader to my XGen descriptions, and add some lights. Then we will render from there, to see what we got, and adjust it eventually to get the look we want.

### General Tips On XGen

Before you jump into XGen, there are several general tips to be aware of:

* Make sure you use Maya's default materials on your geometry (in our case, the planes). So, for example only use Lambert, Blinn, etc. and don't use Arnold's materials. Because you're gonna have trouble seeing the maps you paint on you geometry.
* Make sure the name of the geometry you're using as a base for hairs to grow from, is unique.
* Make sure your mesh has UVs, and the UVs are on the first UDIM.
* On your geometry, Delete History and Freeze Transforms before going further.
* For more complex XGen usages, like using some nodes in Pixar's Renderman that are used to colorize the hair by a painted map, it's urgent that you have no spaces in anything related to your project, otherwise it won't work. For example, no space in the name of the geometry, in the name of the description and collection, and in the address of your project as well. So, in general, avoid space in all the names when using XGen in your project.
* Pick your rendering engine at the beginning and do a quick research about its integration with XGen. Some versions of Maya and rendering engines, have the issue of "Activating the rendering engine plugin before activating the XGen plugin." So, have an eye on that as well.

### Important Steps

Rotate the plane around 30 degrees in X direction (if you're gonna use front camera as your render cam). This way, we can kinda mimic the head, and give the feeling as if it's growing from somewhere.

Select the plane, and hit Create New Description. Pick a name name for your Description and Collection. Remember, no space.

The only option I change, is the Control the Primitives by, which I choose Placing and shaping Guides.

XGen needs at least 3 guides to create a preview. So, place an shape them however you please. Just remember, if you use Rotate on the guides, when you're done with it, click on  Bake Guide Vertices under the Guides menu in the XGen window.

Paint a simple mask for Density. Just under the Density slider in the Primitives tab. Remember to hit save every time you make changes to every mask in XGen system. That's how it works. If you forget to hit the save button, you won't see the changes, because the PTex file hasn't been generated.