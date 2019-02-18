---
layout: post
title: 'Workflow: Controlling Sewing Lines Using ZBrush And Substance Painter'
excerpt: In this article I'm gonna give you an overview of my sewing workflow, in
  which you have full control over them when it comes to texturing.
date: 2019-02-22 00:00:00 +0330
tags:
- article
- workflow
- tutorial
categories:
- articles
image: ''
image-sm: ''
featured: true
showtags: true

---
Having control over the sewing lines you sculpt in your character's clothing, is crucial; because when it comes to texturing part of the pipeline, it will be important to be able to deal with them separate from the main clothing. By using this workflow, you can assign different color, material, dirt, etc. to the sewing lines separately, in _Substance Painter_.

### The Concept

The whole idea, is simply to create a mask while sculpting in _ZBrush_. Then, when you import your model to _Substance Painter_, it's just a matter of applying the created mask to the desired material. And _BOOM_! You are in the driving seat!

### Important Notes Before Starting

* Your mesh has to have proper **_UV_**s.
* We create the mask while sculpting, so if you already have your sculpt ready, this is not gonna work, naturally.
* If you needed to change/optimize the mesh's _UV_s after doing the sculpture, there's nothing to worry about. The mask will be projected to your new mesh along with the sculpting details.

### The Workflow

Before doing any sort of sewing line sculpting, bring the alpha of your brush\[es\] to _Photoshop_, and create a simple mask by painting white only on the sewing lines and leaving everything else black.

An example of creating the right mask for the sewing brush\[es\]:

Then import the created mask to the texture section of _ZBrush_ and apply it to the texture of your brush.

Then fill your mesh with black (pick black color, then go to _Color_ -> _FillObject_, with _RGB_ _ON_ on any brush), and turn on the _RGB_ of your sewing brush, and sculpt while a white color is chosen. This way, when applying the sewing lines to the mesh, the white color will automatically be applied right on top of the sewing lines. This will ultimately be our mask that we're gonna export to _Substance Painter_.

If you have trouble seeing your sculpting process, while in black, just click on the little "brush" button under the _Subtool_ menu, beside the thumbnail of your mesh, to turn polypaint preview off. Now, you don't see the white being painted, but don't worry, it's painting as long as you keep your _RGB_ button _ON_ while using your brush. You can click on that little "_brush_" button again, to make sure it's painting.

When you finished sculpting, it's time to export the mask. Before that, select your desired _UV_ resolution under the _UV Map_ in _Tool_ palette. Go with maximum to have more control later. To export the map, click on _New From Polypaint_ under the _Create_ sub-menu under the _Texture Map_ menu in _Tool_ palette. Then click on _Clone Txtr_. After that, click on _Flip V_ under the _Texture_ palette and then export. The exported image is the one we use in _Substance Painter_.

Import the mesh and the exported map from _ZBrush_ into _Substance Painter_. Add the material you want to use for the sewing lines, then right click on the assigned material, and click on "_Add bitmap mask_," then select the imported mask. That't it, now the material only works on your sewing lines.

### Conclusion

I like this workflow because it's fast and doesn't need extra _UDIM_ _tiles_.

Also, this showcased workflow, could be used for any sorts of similar things, like zippers; then you can assign metal material to that section in _Substance Painter_.

That's it everyone. Thanks for reading. I hope you got something useful out of this article. Let me hear what you have to say. Getting feedback is what gets me going faster.

Cheers!