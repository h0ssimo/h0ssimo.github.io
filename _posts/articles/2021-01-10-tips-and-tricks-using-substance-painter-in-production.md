---
layout: post
title: 'Tips and Tricks: Using Substance Painter In Production'
excerpt: In this article, I'm gonna go over 10 tips and tricks for getting the most
  out of SP along with Arnold for Maya in production environment.
date: 2021-01-10 22:10:00 +0330
tags:
- article
- TipsAndTricks
- Substance Painter
- Arnold
categories:
- articles
image: "/images/tips_and_tricks_on_substance_painter.jpg"
image-sm: "/images/tips_and_tricks_on_substance_painter.jpg"
featured: true
showtags: true

---
_Substance Painter_ is firmly integrated into pipelines of many animation/VFX studios around the world. As a texturing/look development artist in those studios, you have to tackle _SP_ on a daily basis. I've been doing it, and decided to share 10 tips and tricks I picked up along the way.

<img src="/images/look_development_01.jpg" alt="look_developement_hossimo.com" class="narrowResponsive">

 1. **Work Non-Destructively**

    The first one is really important, actually. You have to be flexible in terms of art-direction, like trying different looks and explore ideas rather quickly for the directors. To achieve that goal, you need to have control over every visual element you put on the screen. One of the best ways to get that control, is to let _masking_ be in charge wherever you can. A simple example would be instead of painting directly on _height_ channel, try painting a _mask_ for a _fill layer_ with _height_ slider to control the depth whenever you want. Actually masking in _Substance Painter_ could get really complex considering its powerful procedural system (even better when using _Substance Designer_ along with _SP_) and the toolsets like of _Generators_ or _Anchor Points_.
 2. **Create Your Own Library**

    Down the production pipeline, you will probably need the unique look you are currently spending your time on, again. Also sometimes there might be a gap between working on two similar assets. There could be lots of situations and possibilities in which you need your works from the past, so to keep ot short, try to create a library for yourself. Like you could save a _smart material_ everytime you finish a new asset to develop a good habit.
 3. **Create Your Own Output Template**

    Depending on your _SP_ shader and target rendering engine, you may need to add or remove channels and the exported maps. It's better to save multiple _templates_ for different situations. It helps with consistency in the project.
 4. **Don't underestimate Anchor Points**

    You can use _Anchor Point_ to create complicated setups to have even more control over your look development project. The idea here is to connect different _channels_ of a layer to another layer's, which opens to lots of possibilities.
 5. **Keep Everything Organized**

    Always prepare the files as if another artist would continue on your work from tomorrow on, even if you know that's not the case. By doing so, your files will be readable, editable and reusable by anyone in a robust manner. By not keeping organized, you would lose track of the project sooner or later. No need to mention how confused other artists who will work on the project would be.

    <img src="/images/look_development_01.jpg" alt="look_developement_hossimo.com" class="narrowResponsive">
 6. **Substance Painter Is A Preview**

    Even with the same _environment_ light, what you see may be different from what you render in _Arnold_. It's great for quick testing, but it shouldn't be relied on. So don't worry if what you see in other render engines, is different from _SP_. Technically, _Substance Painter_ is all about getting the _texture maps_ with the right colors, values and formats into the target platform.
 7. **Check On Every Channel Separately**

    Speaking of the right colors and values, checking each _map_ separately will help you decide better on each one of them. For example see if there's appropriate variation in actual _roughness_ values. Checking each _map_ also helps to prevent further issues or to debug.
 8. **Test All Assets Under Same Light Scenarios In Maya**

    The eight tip could go a long way in terms of keeping the consistency and reliability of the overall _look development and lighting_ of the project. In larger studios, look development/lighting teams, would have defined lighting setups and testing environments provided by the supervisors.
 9. **Add Final Touches In Maya**

    Depending on the pipeline, you can leave some of exaggerations, fine-tunings and adding variations to colors and values, for _Arnold_ or generally speaking, rendering engines. Most changes of these natures, follows along while shading the assets.
10. **Stay Consistent**

    This is really important in production; mainly because it gets much more readable to other people in the pipeline, and it makes toubleshooting or editing/directing much more predictable at anytime.