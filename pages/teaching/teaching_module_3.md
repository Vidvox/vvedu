---
title: Module 3 Lesson Plans
keywords: 
last_updated: August 24, 2018
tags: [lesson_plans, live_visuals]
summary: "Module 3: Motion Design"
sidebar: home_sidebar
permalink: teaching_module_3.html
folder: teaching
---

# Motion Design Overview

In addition to being a live video editor, a VJ might incorporate more abstract forms as respondents to music. Simple shapes and colors—how they originate, interact, and respond to music—can elicit an emotional response by connecting with our [innate sensory perception](https://www.khanacademy.org/science/health-and-medicine/nervous-system-and-sensory-infor/sensory-perception-topic/v/gestalt-principles) and ability to attribute human characteristics to objects (anthropomorphism). A quintessential example of shape relationships, both formal and emotional, is the legendary Chuck Jones’ [The Dot and The Line](https://www.youtube.com/watch?v=hgqUya0kGPA).

In order to successfully convey a theme, setting, and mood, you must bring your shapes to life through animation. We do this by designing motion. 

The fundamentals of [motion design](https://en.wikipedia.org/wiki/Motion_graphic_design) are described as the [12 Basic Principles of Animation](https://en.wikipedia.org/wiki/12_basic_principles_of_animation), first introduced in the book [The Illusion of Life: Disney Animation](https://www.amazon.com/Illusion-Life-Disney-Animation/dp/0786860707). The purpose of the principles was to produce an illusion of characters adhering to the basic laws of physics, but they also dealt with more abstract issues, such as emotional timing and appeal. No matter the style—be it hand drawn, 3D, generative, or experimental—the 12 principles can be seen in all forms of motion-based design.

In this module, you will learn a range of basic compositional and motion design principles, developing their timing skills as they develop sensitivity to successiveness, temporal order, and simultaneity. This will include using techniques such as contrasting clock-time with subjective time, duration, continuity, and the feelings of anticipation and expectation and the shifting of temporal perspectives.

## Lesson 1: Stills to Motion

[Handout: Stills to Motion](/vvedu/handout_module_3.html)

[Gestalt](http://graphicdesign.spokanefalls.edu/tutorials/process/gestaltprinciples/gestaltprinc.htm), a psychology term meaning “unified whole,” contains laws of visual perception developed by German psychologists in the 1920s. Its principles explain how we can perceive a succession of stills images as fluid reality.

To begin our exploration into motion design, we will start by implementing some of these laws, so that our compositions retain a sense of unity, as opposed to an assortment of random shapes with no immediate relationship to one another. 

According to the [laws of similarity and proximity](https://www.interaction-design.org/literature/article/the-law-of-similarity-gestalt-principles-1), our brains find pattern and unity when objects look similar to one another and are arranged closely together. So we will begin by evenly spacing and pacing three layers of the same shape.

We will then explore the [law of continuation](https://www.interaction-design.org/literature/article/laws-of-proximity-uniform-connectedness-and-continuation-gestalt-principles-2), by first applying the same linear movement to each shape, then by influencing its arc of motion in a relational way.

### Lesson Overview

* Animating basic shapes
* * ISF Shape Layers
* * Src controls and Layer Comps
* * Linear movement (left-right, up-down)
* * Using LFO’s to create arcs, etc

* Similarity/Proximity:
* * Create a composition using three white circles that are spaced evenly across the Canvas 
* Continuation:
* * Implement the same linear motion for each circle (position, zoom, et al)
* * Apply LFO’s to create a phased continuation (delay, etc)

### Special Equipment

Required:
- [Motion Design Play](https://s3.amazonaws.com/vidvox/vvedu/M3-L1.zip)

### Lecture Notes

- [Stills To Motion Lecture Video](https://vimeo.com/295228229)
- [Stills To Motion Lecture Slides](https://docs.google.com/presentation/d/16zkw1_xCrl2uQbStT3nbwuHxTOZ7FfQHrpaMm7UuIlc)

- Introduction to Gestalt principles
- - What is the “unified whole”?
- - - Visual perception and grouping
- - Similarity
- - Continuation
- - Closure
- - Proximity
- - Figure and Ground
- - Symmetry and order
- The Law of Similarity
- - Similarity is influenced by the shape, size and color of the elements
- - Designing with Similarity in Mind
- - Breaking the law of similarity
- The Law of Continuation
- - Perceived motion / flow
- - Negative space

### Discussions

- What are some examples of Gestalt Principles in the wild, such as company logos, iconography, and elsewhere in the world of design?

### Demonstrations

- [Stills To Motion Demonstration Video](https://vimeo.com/295263632)

#### Animating basic shapes
1. Load the Simple Player template as a starting point
- Add ISF Shape generator and trigger
2. Assigning control data
- From the Workspace Inspetor > Plugins, add an LFO plugin
- Assign the x position to the ramp data-source from the LFO 1
- Assign the y position to the cosine data-source from the LFO 1
- Demonstrate adjusting the rate of the LFO 1 plugin to control the rate of animation
- From the Workspace Inspetor > Plugins, add a second LFO plugin
- Assign the y position to the cosine data-source from the LFO 2
- Demonstrate adjusting the rate of LFO 1 and LFO 2 plugin to control the rates of animation on individual properties
- Assign x = sine, y = cosine; note this creates circles when at the same rate, and various arcing patterns when the rates do not match
- Adjust the min / max range handles on the x and y position sliders to limit the range of the animation on the receiving side

#### Similarity/Proximity/Continuation
1. Add two layers to the setup
- Open the layer source windows into their own windows
- Add copies of the shape generator ISF into the media bin (or make copies with the bin) and trigger to Layer 2 and Layer 3
2. Adding additional waveforms and modifying their values
- Inspect LFO 1
- - Add a second sine waveform
- - In the main LFO interface, click on the start point of Sine 2 and drag to 1/3 of the way into the time domain
- - Assign the x position of the Layer 2 shape to the Sine 2 data-source from the LFO 1
- - Add a third sine waveform
- - In the main LFO interface, click on the start point of Sine 3 and drag to 2/3 of the way into the time domain
- - Assign the x position of the Layer 3 shape to the Sine 3 data-source from the LFO 1
- Repeat above for LFO 2, using cosine instead of sine and the y position instead of x position
3. Add a 3rd LFO to adjust the size / zoom levels of the shapes

### Exercises

#### Animating basic shapes
1. Load the Simple Player template as a starting point
- Add ISF Shape generator and trigger
2. Adding control data
- From the Workspace Inspetor > Plugins, add an LFO plugin
- Assign the x position to the ramp data-source from the LFO 1
- Assign the y position to the cosine data-source from the LFO 1
- Demonstrate adjusting the rate of the LFO 1 plugin to control the rate of animation
- From the Workspace Inspetor > Plugins, add a second LFO plugin
- Assign the y position to the cosine data-source from the LFO 2
- Demonstrate adjusting the rate of LFO 1 and LFO 2 plugin to control the rates of animation on individual properties
- Try using different waveforms and playback to get different results:
- - x = sine, y = cosine creates circles when at the same rate, and various arcing patterns when the rates do not match
- - When the rates do not match, how long does it take for the LFOs to resync?
- - What happens when we use the value of one LFO to control the position or rate of another LFO?

#### Similarity/Proximity:
1. Add two layers to the setup
- Open the layer source windows into their own windows
- Add copies of the shape generator ISF into the media bin (or make copies with the bin) and trigger to Layer 2 and Layer 3
2. Add LFOs and waveforms to create the following compositions:
- Create a composition using three white circles that are spaced evenly across the Canvas 
- Implement the same linear motion for each circle (position, zoom, et al)
- Apply LFO’s to create a phased continuation (delay, etc)
3. Optional: Add a Movie Recorder plugin to capture the final output

## Lesson 2: Color and Choreography

[Handout: Color and Choreography](/vvedu/handout_module_3.html)

To create a more complex visual, a VJ will conceptualize and compose the choreography of various elements temporally (timing) and spatially (arrangement). By manipulating the basic shapes’ attributes over time and space using controlled animation, we can extend the motion design fundamentals into dynamic, [synaesthetic](https://www.dictionary.com/browse/synaesthetic) compositions. 

Early examples of choreography in film and animation can be seen in the work of [Busby Berkeley](https://en.wikipedia.org/wiki/Busby_Berkeley), where he used dancers, sets, and costumes to create mesmerizing, kaleidoscopic displays of bodies in motion. Designers such as [Saul Bass](https://en.wikipedia.org/wiki/Saul_Bass) choreographed layers of stylized forms to set the theme, setting and mood for film and TV title sequences. His sequences are most masterful in symbolizing pure emotion.

A major device for influencing the emotional, synaesthetic quality of an object is color. We will explore the musicality of color in the Visual Music module, but first we will its essential effect using the [additive color palette](https://en.wikipedia.org/wiki/Additive_color) of RGB, since red, green and blue are the primary colors of light.

Using the previous ‘Gestalt’ composition, we will refine the relationship between the shapes through controlled direction, velocity, and force to create a motion-based, [concentric circle](http://mathworld.wolfram.com/ConcentricCircles.html) composition using scale, position, rotation, and the RGB palette. 

We will then augment the color relationships by experimenting with layer modes (Add, Multiply, etcetera) to explore additive and [subtractive color](https://en.wikipedia.org/wiki/Tertiary_color) and the resulting tertiary forms. 

Finally, refine the timing of your final composition to music by syncing the motion to the clock (BPM), step sequencers, and/or the cue list for optimal control.

### Lesson Overview

* Animating shapes and colors using control plugins
* “Zooming” 
* Syncing motion to the Clock
* Dynamic form using Num FX and FX Chains
* Step sequencers

* Concentric RGB circles using “Zooming” 
* * Phasing in/out
* * Looping motion using math
* RGB circles using position/rotation LFO’s
* Refine timing to music using step sequencer

### Special Equipment

Required:
- [Motion Design Color Play](https://s3.amazonaws.com/vidvox/vvedu/M3-L2.zip)

### Lecture Notes

- Introduction to Color
- - [Additive color palette](https://en.wikipedia.org/wiki/Additive_color)
- - [Subtractive color](https://en.wikipedia.org/wiki/Tertiary_color)
- - Color and Gestalt principles
- [Choreography](https://en.wikipedia.org/wiki/Choreography)
- - Sequence design
- - Busby Berkeley
- - Saul Bass
- - [Death Cab for Cutie - You Are A Tourist, Official Video](https://www.youtube.com/watch?v=qkk5wViJo-I)

### Discussions

- What are some of your favorite modern title sequences from movies / music videos?

### Demonstrations

#### Animating shapes and colors using control plugins

1. Continuing from 3 animated circles project file...
2. Create concentric RGB circles using “Zooming”
- Set the shape colors of Layers 1-3 to Red, Green and Blue respectively from the Layer Source controls
- Disable animation for x/y parameters and set positions to center or the same corner position
- Animate only the size / zoom parameter to create a concentric RGB circles
3. Adding color animation
- From the Workspace Inspector > Plugins, add a Step Sequencer plugin
- From the inspector for the Step Sequencer, add a color track
- Control+drag from the color bar on the left-side of the Step Sequencer to the color swatch for Layer 1 shape color to create a connection
- Add 2 more color tracks from the Step Sequencer inspector
- Click on color swatches for Layer 2 and Layer 3 to demonstrate using the UI Inspector to manually create assignments for the 2nd and 3rd color tracks
- In the Step Sequencer main interface demonstrate:
- - Changing the color pattern sequence manually
- - Randomizing the color pattern sequence
- - Click on the color panels on the left side to adjust the published color on a per row basis
- - Using the 'Section Preset' bar to create presets
- In the Step Sequencer inspector demonstrate: 
- - Adjusting number of rows
- - Adjusting interpolation phase to fade between colors
4. Adjusting rates of multiple plugins together using Clocks
- From the Workspace Inspector > Plugins, inspect Clock 1
- - Note that each LFO / Step Sequencer is sync'd to the same clock plugin
- - Adjusting the BPM of the clock adjusts the rate of all sync'd plugins
- - Note that multiple clocks can be used in advanced setups
- - The clock can be synchronized with other software or analyze audio signals for automatic BPM detection
- In the main interface for the Step Sequencer plugin
- - To the right of the clock selection menu, change the duration from the default of 2 measures to 4 measures; note that the rate moves at half the speed, then adjust the number of measures to 1 and note that it is moving twice as fast as the original rate
- - Click on the 'clock' icon to disable clock sync
- - Note that the 'M' for duration switches from 'Measures' to 'S' for 'Seconds' allowing for independent timing control for individual plugins

### Exercises

#### Concentric RGB circles using “Zooming” 
1. Continuing from 3 animated circles project file...
2. Create concentric RGB circles using “Zooming”
- Set the shape colors of Layers 1-3 to Red, Green and Blue respectively from the Layer Source controls
- Disable animation for x/y parameters and set positions to center or the same corner position
- Animate only the size / zoom parameter to create a concentric RGB circles

####  Color animations
1. Continuing from above...
2. Add a Step Sequencer and use color tracks to animate the colors of each shape layer
- Optional: Use the other Step Sequencer track types, such as index and float, to control the size / zoom parameter instead of an LFO
3. Refine timing of LFO and Step Sequencer plugins using the concepts from the Rhythmic Sequence lesson:
* Regular rhythm: Intervals between sizes are the same in duration (i.e., one second per size)
* Progressive rhythm: The size of shapes are changed over a progression, getting faster towards the end (2 sec, 1 sec, ½ sec, and so on)
* Flowing (organic) rhythm: Occurs when the intervals are organic, used to create a feeling of visual polyphony. Think VJ’ing to wind chimes.

