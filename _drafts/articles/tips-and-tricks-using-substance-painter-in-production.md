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
image: ''
image-sm: ''
featured: true
showtags: true

---
_Substance Painter_ is firmly integrated into pipelines of many animation/VFX studios around the world. As a texturing/look development artist in those studios, you have to tackle _SP_ on a daily basis. I've been doing it, and decided to share 10 tips and tricks I picked up along the way.

 1. Work Non-Destructively

    The first one is really important, actually. You have to be flexible in terms of art-direction, like trying different looks rather quickly for the directors. To achieve that goal, you need to have control over every visual element you put on the screen. One of the best ways to get that control, is to let _masking_ be in charge wherever you can. A simple example would be instead of painting on a height channel, try painting a mask for a fill layer with height slider to control the depth whenever you want. You get the idea. Actually masking in Substance Painter could get really complex considering its powerful procedural system (even better when using Substance Designer along with SP) and the likes of Anchor Points. 
 2. Create Your Own Library

    Down the production pipeline, you will probably need the unique look you are spending your time on right now. Also sometimes there might be a gap between working on two similar assets. So try to create a library for yourself. Like you could save a smart material everytime you finish a new asset to develop a good habit.
 3. Create Your Own Output Template

    Depending on your SP shader and target rendering engine, you may need to add or remove exported maps. It's better to save multiple templates for different situations. It keeps the consistency in the project.
 4. Don't underestimate Anchor Points

    You can use Anchor Point to create complicated setups to have even more control over your look development project. The idea here is to connect different channels of a layer to another layer's, which opens to lots of possibilities.
 5. Keep Everything Organized

    Always prepare the files as if another artist would continue from tomorrow on, even if you know that's not the case. By doing so, your files will be readable, editable and reusable by anyone in a robust manner. By not keeping organized, you would lose track of the project sooner or later. No need to mention how confused other artists who will work on the project would be.
 6. Substance Painter Is A Preview

    Even with the same environment light, what you see may be different from what you render in Arnold. It's great for quick testing, but it shouldn't be relied on. So don't worry if what you see in other engines, differ. Technically, Substance Painter is all about getting the texture maps with the right colors, values and formats into the target platform.
 7. Check On Every Channel Separately

    Speaking of the right colors and values, checking each map separately will help you decide better on each one of them. It also helps to prevent further issues or debugging.
 8. Test Under Same Light Scenarios In Maya

    It seems obvious but can go a long way in terms of keeping the consistency and reliability of the overall look development and lighting of the project. In bigger studios, look development/lighting teams, would have specific lighting setups and testing environments provided by the supervisors.
 9. Color Correct And Tweak In Arnold
10. Stay Consistent