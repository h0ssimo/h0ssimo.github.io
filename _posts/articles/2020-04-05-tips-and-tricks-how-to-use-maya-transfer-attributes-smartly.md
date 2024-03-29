---
layout: post
title: 'Tips and Tricks: How To Use Maya Transfer Attributes Smartly'
excerpt: In this article, I'm gonna explain how to get the most out of Maya's Transfer
  Attributes as a Character Artist, and I'll also show you guys some hopefully useful
  examples to demonstrate a variety of usages of TA.
date: 2020-04-05 00:00:00 +0430
tags:
- article
- TipsAndTricks
- Maya
- MarvelousDesigner
categories:
- articles
image: "/images/Tutorials/Tips_And_Tricks/Tranfer_Attributes/tips_and_tricks_on_transfer_attributes_header.jpg"
image-sm: "/images/Tutorials/Tips_And_Tricks/Tranfer_Attributes/tips_and_tricks_on_transfer_attributes_header.jpg"
featured: true
showtags: true

---
_Maya's Transfer Attributes_ function is probably something you should reconsider when it comes to using it your workflow. Because it's awesome, and sadly often underestimated!

So today I'm gonna try to show you guys some examples of how we can use this function to save ourselves some precious time and also the variety of the things we could do with _Transfer Attributes_. Hopefully it helps you along with your projects.

### How Maya Transfer Attributes Works

Much like other _Maya_ functions, _Transfer Attributes_ needs a target, and a source geometry. First, you have to select the **source** geometry, and then the **target** to which the transfer will be applied.

You can find _Transfer Attributes_ in _Modeling_ section under _Mesh_>_Transfer Attributes_. After you made your geometry selection click on the the _Transfer Attributes_ options to see the window below:

<img src="/images/Tutorials/Tips_And_Tricks/Tranfer_Attributes/01_transfer_attributes_options.jpg" alt="01_transfer_attributes_options" class="responsive">
_the default settings_

Think of the first part of the options as "WHAT" you want to transfer between geometries, and the second part as "HOW" you want the attributes to be transferred.

You can read the full documentation on each one of the options [_here_](https://knowledge.autodesk.com/support/maya/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/Maya-Modeling/files/GUID-76D5F064-C5A1-4310-B72A-788AB5C9A25B-htm.html "Transfer attributes between meshes").

On a daily basis, we have to keep an eye on a number of important stuff: _Component IDs_, _UVs_, _Topology Changes_, _Spacing_ _(world, local, etc.)_

I'm gonna explain more on a couple of examples:

##### Case #1: Transferring UVs Between Meshes

<img src="/images/Tutorials/Tips_And_Tricks/Tranfer_Attributes/02_transfer_attributes_case_1.jpg" alt="02_transfer_attributes_case_1" class="responsive">

There could be lots of scenarios, here's the basic one plus a bit of information on other scenarios:

Here I have two meshes with the same topology, one with the right _UVs_ and mouth closed, and the other, no _UVs_ and mouth open. I want to transfer the _UVs_ and also the shape to the other. Let's go through some of the options we need and why.

**_Vertex Position: On _**- I basically need this just because I want to make the lips closed in the new version. This option could be useful in combination with _Topology_ sample space when _Component IDs_ have changed, therefore you can't use _Blendshapes_.

**_UV Sets: All _**- So I want to transfer everything about _UVs_ from the old model to the new one, right?

**_Sample Space: Component_** - This is usually the make-or-break part of this whole transferring. In this case, since I have the same topology and _Component IDs_, I chose component. If the _Vertex IDs_ on models did not match each other, I'd use Topology option instead.

<img src="/images/Tutorials/Tips_And_Tricks/Tranfer_Attributes/03_transfer_attributes_case_1_options.jpg" alt="03_transfer_attributes_case_1_options" class="responsive">
_So these are the settings in this case._

##### Case #2: Transferring Vertex Normals

<img src="/images/Tutorials/Tips_And_Tricks/Tranfer_Attributes/04_transfer_attributes_case_2.jpg" alt="04_transfer_attributes_case_2" class="responsive">

In this case, I just want to showcase an example of how we could actually put this option to good use.

So I have a hair made of hair cards for game engines. As you create strips of polygon hair, each strip has its own normals, naturally. In order to make them seamlessly blend into each other like real hair would do, specially in terms of creating smooth highlights, we should use transfer attributes.

First of all, merge all your hair cards into one geometry (_target_ object), if you already haven't. Then create a somewhat cylindrical dome-alike object to nearly match the outline of the hair. Now divide the dome to have really hi-res geometry. Then freeze transforms on both source and target objects. This is important since we're gonna use _World_ sample space.

You should have something similar to the image below.

<img src="/images/Tutorials/Tips_And_Tricks/Tranfer_Attributes/05_transfer_attributes_case_2_target_source_geos.jpg" alt="05_transfer_attributes_case_2_target_source_geos" class="responsive">
_The hair geometry (target) is sitting right into the dome geometry (source)._

Now, for Transfer Attributes Options:

**_Vertex Normals: On_** - This is the main data that if transferred from the shape we just created, solves all the specular and seamlessness issues I mentioned before.

**_Sample Space: World_** - By choosing this option, "sampling normals" is done by evaluation of the absolute distance between the vertices. So, good for us!

**_Search Method: Closest To Point_** - This is the default option. Just make sure you don't have the other option (_Closest Along Normal_) is not activated. Because it could cause some artifacts.

<img src="/images/Tutorials/Tips_And_Tricks/Tranfer_Attributes/07_transfer_attributes_case_3.jpg" alt="07_transfer_attributes_case_3" class="responsive">
_These are the settings in the second case._

##### Case #3: Using Transfer Attributes In Marvelous Designer Workflow

<img src="/images/Tutorials/Tips_And_Tricks/Tranfer_Attributes/06_transfer_attributes_case_2_options.jpg" alt="06_transfer_attributes_case_2_options" class="responsive">

In this case I'm gonna demonstrate a cool trick to retopologize the clothes created in _Marvelous Designer_ for further use in the pipeline.

We're gonna need 3 geometries and 2 usages of _Transfer Attributes_.

<img src="/images/Tutorials/Tips_And_Tricks/Tranfer_Attributes/08_transfer_attributes_case_3_models.jpg" alt="08_transfer_attributes_case_3_models" class="responsive">
_These are the models we need._

So, now what we need to do, is to transfer UVs from the triangulated flat model (1) to the quads version (2). Then, we should be able to transfer vertex positions from the triangulated model (3) to the quad flat model (2). And that's it.

For the first "Transfer Operation," since our models are exactly on top on each other, we need to use World Sample Space to transfer the UVs.

For the second "Transfer Operation," since our models share the same UV sets, we could use UV Sample Space to transfer the Vertex Position.

And now you have the quad version of your clothes model with perfect UVs to use in your project.

That's all. Thanks for reading.
