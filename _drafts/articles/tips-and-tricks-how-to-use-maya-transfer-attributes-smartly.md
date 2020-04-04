---
layout: post
title: 'Tips and Tricks: How To Use Maya Transfer Attributes Smartly'
excerpt: I this article, I'm gonna explain how to get the most out of Maya's Transfer
  Attributes as a Character Artist, and I'll also show you guys some hopefully useful
  examples to demonstrate a variety of usages of TA.
date: 2020-04-04 00:00:00 +0430
tags:
- article
- TipsAndTricks
- Maya
- ZBrush
- MarvelousDesigner
categories:
- articles
image: "/images/tips_and_tricks_on_transfer_attributes_header.jpg"
image-sm: "/images/tips_and_tricks_on_transfer_attributes_header.jpg"
featured: true
showtags: false

---
### How Maya Transfer Attributes Works

Much like other _Maya_ functions, _Transfer Attributes_ needs a target, and a source geometry. First, you have to select the **source** geometry, and then the **target** to which the transfer will be applied.

You can find Transfer Attributes in _Modeling_ section under _Mesh_>_Transfer Attributes_. After you made your geometry selection click on the the _Transfer Attributes_ options to see the window below:

![](/images/01_transfer_attributes_options.jpg)

_default settings_

Think of the first part of the options as "WHAT" you want to transfer between geometries, and the second part as "HOW" you want the attributes to transfer.

You can read the full documentation on each one of the options [_here_](https://knowledge.autodesk.com/support/maya/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/Maya-Modeling/files/GUID-76D5F064-C5A1-4310-B72A-788AB5C9A25B-htm.html "Transfer attributes between meshes").

On a daily basis, we have to keep an eye on a number of important stuff: _Component IDs_, _UVs_, _Topology Changes_, _Spacing_ _(world, local, etc.)_

I'm gonna explain more on a couple of examples:

##### Case: Transferring UVs Between Meshes

There could be lots of scenarios, here's the basic one plus a bit of information on other scenarios:

Here I have two identical meshes, all except _UVs_. I want to transfer the UVs from the left one (obvious, it has _Normal Map_!) to the other. Let's go through the options we need and why.

_Vertex Position: Off_ - I don't need that because my meshes are basically the same and no vertices were move or deformed. This option could be useful when you want to match the surfaces of two objects. Or when transferring data between high and low versions of a model. 