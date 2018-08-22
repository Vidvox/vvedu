---
title: Motion Design Handout
keywords: 
last_updated: August 22, 2018
tags: [handouts]
summary: "Handout for Introduction to Motion Design"
sidebar: home_sidebar
permalink: handout_module_3.html
folder: handouts
---

# Introduction to Motion Design

In addition to being a live video editor, a VJ might incorporate more abstract forms as respondents to music. Simple shapes and colors—how they originate, interact, and respond to music—can elicit an emotional response by connecting with our [innate sensory perception](https://www.khanacademy.org/science/health-and-medicine/nervous-system-and-sensory-infor/sensory-perception-topic/v/gestalt-principles) and ability to attribute human characteristics to objects (anthropomorphism). A quintessential example of shape relationships, both formal and emotional, is the legendary Chuck Jones’ [The Dot and The Line](https://www.youtube.com/watch?v=hgqUya0kGPA).

In order to successfully convey a theme, setting, and mood, you must bring your shapes to life through animation. We do this by designing motion. 

The fundamentals of [motion design](https://en.wikipedia.org/wiki/Motion_graphic_design) are described as the [12 Basic Principles of Animation](https://en.wikipedia.org/wiki/12_basic_principles_of_animation), first introduced in the book [The Illusion of Life: Disney Animation](https://www.amazon.com/Illusion-Life-Disney-Animation/dp/0786860707). The purpose of the principles was to produce an illusion of characters adhering to the basic laws of physics, but they also dealt with more abstract issues, such as emotional timing and appeal. No matter the style—be it hand drawn, 3D, generative, or experimental—the 12 principles can be seen in all forms of motion-based design.

In this module, you will learn a range of basic compositional and motion design principles, developing their timing skills as they develop sensitivity to successiveness, temporal order, and simultaneity. This will include using techniques such as contrasting clock-time with subjective time, duration, continuity, and the feelings of anticipation and expectation and the shifting of temporal perspectives.

# Lesson 1: Stills to Motion

[Gestalt](http://graphicdesign.spokanefalls.edu/tutorials/process/gestaltprinciples/gestaltprinc.htm), a psychology term meaning “unified whole,” contains laws of visual perception developed by German psychologists in the 1920s. Its principles explain how we can perceive a succession of stills images as fluid reality.

To begin our exploration into motion design, we will start by implementing some of these laws, so that our compositions retain a sense of unity, as opposed to an assortment of random shapes with no immediate relationship to one another. 

According to the [laws of similarity and proximity](https://www.interaction-design.org/literature/article/the-law-of-similarity-gestalt-principles-1), our brains find pattern and unity when objects look similar to one another and are arranged closely together. So we will begin by evenly spacing and pacing three layers of the same shape.

We will then explore the [law of continuation](https://www.interaction-design.org/literature/article/laws-of-proximity-uniform-connectedness-and-continuation-gestalt-principles-2), by first applying the same linear movement to each shape, then by influencing its arc of motion in a relational way. 

## Lesson Overview

* Animating basic shapes
* * ISF Shape Layers
* * Src controls and Layer Comps
* * Linear movement  (left-right, up-down)
* * Using LFO’s to create arcs, etc

* Similarity/Proximity:
* * Create a composition using three white circles that are spaced evenly across the Canvas 
* Continuation:
* * Implement the same linear motion for each circle (position, zoom, et al)
* * Apply LFO’s/Num FX to create a phased continuation (delay, etc)

## Reference Links

* [Variations on a Circle](https://www.youtube.com/watch?v=TnU88XWYjEs&index=22&t=65s&list=PL9C7F0FD297628D28)

## Resources

* ISF shape generator examples

## Related Tutorials and Case Studies

* [Animating Properties of GLSL Shaders in VDMX](https://vdmx.vidvox.net/tutorials/animating-properties-of-glsl-shaders-in-vdmx)
* [Pixel Spirit Deck](https://vdmx.vidvox.net/blog/pixel-spirit-deck-table)

## Homework

* Create and record three black and white shape-based sequences using variations of the Gestalt principles
* * ~10 seconds without music
* * ~10 seconds with music, adjusting timing for tempo

# Lesson 2: Color and Choreography

To create a more complex visual, a VJ will conceptualize and compose the choreography of various elements temporally (timing) and spatially (arrangement). By manipulating the basic shapes’ attributes over time and space using controlled animation, we can extend the motion design fundamentals into dynamic, [synaesthetic](https://www.dictionary.com/browse/synaesthetic) compositions. 

Early examples of choreography in film and animation can be seen in the work of [Busby Berkeley](https://en.wikipedia.org/wiki/Busby_Berkeley), where he used dancers, sets, and costumes to create mesmerizing, kaleidoscopic displays of bodies in motion. Designers such as [Saul Bass](https://en.wikipedia.org/wiki/Saul_Bass) choreographed layers of stylized forms to set the theme, setting and mood for film and TV title sequences. His sequences are most masterful in symbolizing pure emotion.

A major device for influencing the emotional, synaesthetic quality of an object is color. We will explore the musicality of color in the Visual Music module, but first we will its essential effect using the [additive color palette](https://en.wikipedia.org/wiki/Additive_color) of RGB, since red, green and blue are the primary colors of light.

Using the previous ‘Gestalt’ composition, we will refine the relationship between the shapes through controlled direction, velocity, and force to create a motion-based, [concentric circle](http://mathworld.wolfram.com/ConcentricCircles.html) composition using scale, position, rotation, and the RGB palette. 

We will then augment the color relationships by experimenting with layer modes (Add, Multiply, etcetera) to explore additive and [subtractive color](https://en.wikipedia.org/wiki/Tertiary_color) and the resulting tertiary forms. 

Finally, refine the timing of your final composition to music by syncing the motion to the clock (BPM), step sequencers, and/or the cue list for optimal control.

## Lesson Overview

* Animating shapes using control plugins
* “Zooming” 
* Syncing motion to the Clock
* Dynamic form using Num FX and FX Chains
* Step sequencers

* Concentric RGB circles using “Zooming” 
* * Phasing in/out
* * Looping motion using math
* RGB circles using position/rotation LFO’s
* Refine timing to music using step sequencer and cue list

## Reference Links

* [Busby Berkeley clip](https://www.youtube.com/watch?v=kIO9y1xMPIA)
* [The Dot and The Line](https://www.youtube.com/watch?v=hgqUya0kGPA)
* [How Saul Bass Changed Film and TV Forever](https://www.wired.com/2016/10/design-legend-saul-bass-changed-film-tv-forever/)
* [Death Cab for Cutie - You Are A Tourist, Official Video](https://www.youtube.com/watch?v=qkk5wViJo-I)

## Resources

* Bouncing out of phase RGB circles driven by LFOs 

## Related Tutorials and Case Studies

* [Step Sequencer Color Tracks](https://vdmx.vidvox.net/tutorials/step-sequencer-color-tracks)
* [Mixing, Adjusting and Generating Complementary Color Data-Sources in VDMX](https://vdmx.vidvox.net/tutorials/generating-complementary-colors-in-vdmx-with-qc)

## Homework

* Create three RGB circle comps with background layer
* * Concentric “Zooming”
* * Position / rotation using LFOs 
* * Step Sequencer to music

# Lesson 3: Collaborating with Musicians

In the case where visuals and lighting are being performed live along with music, there is the possibility for both sides to respond and react, in the way the members of a band can improvise or riff off each other, or create an informal jam session to try out new ideas.

When collaborating with musicians directly on the creation of new work, visual artists have an opportunity to influence the way that the sound and imagery are connected in time and feeling. For live performances this also allows for the possibility of sharing timecode and other control information between systems for an added level of synchronization.

## Lesson Overview

* The Control Surface plugin
* MIDI software
* OSC / OSCQuery

* Creating custom interface layouts with the Control Surface plugin
* Advanced MIDI synchronization
* * MIDI Clock sync from Ableton Live to VDMX
* * Ableton Link
* * Sending MIDI triggers and control values from Ableton Live to VDMX
* OSCQuery in VDMX
* * Web page control
* * OSCQuery Client plugin
* * Using OSCQuery Helper and MIDI OSCQuery Helper

## Reference Links

* History of MIDI
* About OSCQuery

## Resources

* [MIDI OSCQuery Helper](https://docs.vidvox.net/freebies_midi_oscquery_helper.html)
* [OSCQuery Helper](https://docs.vidvox.net/freebies_oscquery_helper.html)
* Ableton Live sample project

## Related Tutorials and Case Studies

* [The ECLECTIC METHOD REMIX, Part Three - Working with Ableton Live](https://vdmx.vidvox.net/tutorials/the-eclectic-method-remix-part-three-working-with-ableton-live)
* [Using Ableton Link with VDMX](https://vdmx.vidvox.net/tutorials/ableton-link-in-vdmx)
* [Receiving MIDI Clock from Ableton Live](https://vdmx.vidvox.net/tutorials/receiving-midi-clock-from-ableton-live-in-vdmx)
* [Receiving MTC from QLab in VDMX](https://vdmx.vidvox.net/tutorials/receiving-midi-smpte-time-code-mtc-in-vdmx)
* [Syncing the playback of multiple movies in VDMX over a network using OSC](https://vdmx.vidvox.net/tutorials/syncing-the-playhead-of-multiple-movies-in-vdmx)
* [More fun audio analysis techniques](https://vdmx.vidvox.net/tutorials/more-fun-audio-analysis-techniques)
* [How to Turn an Old Building into an Interactive Driving Range ](https://vdmx.vidvox.net/tutorials/how-to-turn-an-old-building-into-an-interactive-driving-range-by-lumenal-code)

## Homework

* Create a 5 minute improvised piece using three different shapes and a background choreographed to music using audio reactivity and MIDI/OSC control.