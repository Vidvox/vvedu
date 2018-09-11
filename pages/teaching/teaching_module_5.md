---
title: Module 5 Lesson Plans
keywords: 
last_updated: August 24, 2018
tags: [lesson_plans, live_visuals]
summary: "Module 5: Aesthetic Overview"
sidebar: home_sidebar
permalink: teaching_module_5.html
folder: teaching
---

# Aesthetic Overview Overview

The key challenge of visual performance design is to dynamically visualize the concept and story arc of the music and/or narrative. Defining a “point of view,” or overarching aesthetic can be helpful in maintaining cohesion throughout a set. 

For instance, the source material might vary greatly (bodies, objects, abstractions, landscapes), however, if they are treated and presented using similar textures, color palettes, framing, pacing, and even layering elements from multiple images can make the visual set appear more unified. 

Paintings or other, more 'worked,' visual forms, provide a second meaning to the subject matter—the denoted or representational meaning supplemented by the style or 'treatment' of the image. For example, [William Kentridge](https://en.wikipedia.org/wiki/William_Kentridge)’s theatrical designs, featuring his own charcoal drawings and animations, alter the perception of the images he portrays beyond that of a representational photograph.

Regardless of treatment, consider how the aesthetics influence the mood and meaning of the imagery, the tone and themes in the music, and your desired intent.

## Lesson 1: Styling Your Look

[Handout: Styling Your Look](/vvedu/handout_module_5.html)

We should consider how effects and digital manipulation influences the interpretation of our imagery. They will have their own connotations and history. For instance, effects that simulate an old VHS tape or an analogue synth may tie it to a certain era, e.g., the “Stranger Things” opening title.

### Lesson Overview

* Styling with LUTs
* Minimalism
* Retro
* Glitch
* 3D Graphics
* Samples
* * Live
* * Archival
* * Modern
* DJ / VJ Techniques
* * Mix / crossfade
* * Time jumping / scratching
* * Audio and Visual FX
* * 2 vs 4 channel setups

### Special Equipment

Required:
- 'Archival / Modern' sample set
- 

Recommended:
- 
- 

### Lecture Notes

- Aesthetic Overview

### Discussions

* 

### Demonstrations

#### Styling with LUTs and Color Effects

Note: Due to a GPU driver bug in 10.13, LUT based FX in VDMX may not work on some NVIDIA GPUs; similar styling can be achieved with other FX as demonstrated
1. Starting from the 'Simple Player' template
- Add archival / modern sample set to media bin
- Add live web-cam to media bin from the Media Browser
- Trigger a clip
2. In the Layer 1 FX controls:
- Add a 'LUT' FX
- Use the LUT selection menu in the LUT FX to demonstrate different stylings
- Delete the 'LUT' FX and replace with the 'LUT Mixer' FX
- Use the provided menus to select two different LUT styles
- Use the provided slider to fade between styles
- Demonstrate stacking LUT based FX in combination with:
- - Vignette (under Film FX)
- - Color Controls (under Color Adjustment)
3. Adding new LUTs
- From the Help menu, select 'Open Assets Folder in Finder'
- Locate and open the LUTs folder
- Add provided sample 'Zombies.cube' to the LUTS folder
- Note that .cube files containing color mappings can be created and exported from photo apps like Photoshop, and many pre-made LUTs can be found online
4. Similar FX:
- v002 Technicolor (Film) includes a few hard-coded styles similar to LUTs
- v002 Bleach Bypass (Film)
- Auto Levels (Color Adjustment)
- Color Monochrome / False Color (Color Effect)
- ComicBook
- Photo Effect Chrome / Fade / Noir / etc (Color Effect)

#### Stylizing with FX
1. Retro FX - Used to recreate FX common on older analog video mixers and other 'retro' era styles
- ASCII Art
- Bad TV
- Chroma Mask
- Color Posterize / Luminance Posterize
- Dither-Bayer
- Duotone / Triotone
- Hologram
- Interlace
- Night vision / Thermal Camera / X-Ray
- RGB Halftone
- Solarize
- v002 CRT Mask / v002 CRT Displacement (use these together, how does the order change the output?)
- VHS Glitch
- Zooming Feedback
2. Minimalism
- Duotone (Using black or white and one color) / Triotone (Using black and white and one mid color)
3. Glitch
- Bad TV
- Collage
- Convergence
- FashMosh
- Poly Glitch
- Random Freeze
- Replicate
- Resize Glitch
- Vertical Tearing
- VHS Glitch
- 3rd Party:
- - Bangnoise Datamosh 
- - v002 Glitch Analog
- - v002 Glitch FBO (on supported OS versions)
- - v002 Rutt Etra
4. Film / Cinematic
- Chroma Desaturation Mask
- Chroma Zoom
- Ghosting
- Glow
- Lens Flare
- Soft Blur
- v002 Technicolor
5. Psychedelic
- Bump Distortion
- Kaleidoscope
- Optical Flow Distort
- Radial Replicate
- Ripples
- RGB Trails
- Twirl
6. Reactive
- Shake
- Sliding Strips
- Waveform Displace

#### DJ / VJ Techniques

When performing with DJs, how can we style and mix video using techniques similar techniques?
1. Mixing / Crossfading
- Load the 'Simple Mixer' template
- Mixer plugin allows for cross-fading / cutting between videos at the same time as audio
2. Composition and FX 
- DJs use EQ to mix individual parts of songs together (low, mid, high); what visual equivalents can we use?
- - Masking FX to show only part of a video:
- - - Chroma Mask: Remove specified colors
- - - Layer Mask: Use grayscale 'mask' streams to create any custom masking
- - - Shape Mask: Mask using different shapes / patterns
- - Color mixing:
- - - RGB EQ can be used to fade / amplify individual color channels similar to sound EQs
3. Time jumping
- When using time based media (eg movie files)
- - Use the << >> time jump buttons in the Layer Source controls to jump back / forward in time
- - Adjust playback rate +/- 10% to match tempo / energy of music
- - Tip: For best results with time jumping in movies, use PhotoJPEG or HAP, avoid h.264
4. Many virtual DJ software, eg Serato and Tracktor use a 4-deck system
- Load the '4 Channel Mixer' template
- Demonstrate technique of create sub-mixes to crossfade between

#### How to create a retro Halloween visual style in VDMX

Note: This is based on [Halloween visual style in VDMX](https://vdmx.vidvox.net/tutorials/create-retro-halloween-visual-styles-in-vdmx)

1. Start from a new project
2. From the Workspace Inspector > Layers, create the following layers:
- glow
- graphics
- background
3. Configure the media bin
- Set target to 'graphics' layer
- Add the 'logos' media file set to the media bin page
- Trigger one of the example files
4. Configure the background style to create a dystopia cloud style
- From the workspace inspector, inspect the 'background' layer
- Use the 'Use Source' option from the Layer Source controls and select the ISF > Noise.fs
- - Set the 'cell size' parameter to 0
- - Set the threshold level to around 0.5
- - Set the color mode to B&W
- Tip: If using clips with alpha channels like our examples, try switching the 'graphics' layer to OpenGL Over mode
- Add FX to 'background' layer
- - False Color (adjust colors to match music, branding, or other appropriate qualities)
- - Dirty Lens (animate the 'dirt seed' with the clock time)
- - VVMotionBlur 3.0 (set level too 0.8 or higher)
- - Soft Blur
5. Configure the 'graphics' layer
- From the workspace inspector, inspect the 'graphics' layer
- Add FX to 'background' layer
- - Dirty Lens
- - Straighten
- - Shake
- - Zooming Feedback (adjust parameters)
6. Configure the 'glow' layer; this uses the 'graphics' layer as a source and composites additional styling with its own FX chain
- From the workspace inspector, inspect the 'glow' layer
- Use the 'Use Source' option from the Layer Source controls and select the Layers > graphics
- Add FX to 'glow' layer
- - Soft Blur
7. Animate FX params
- Add LFO and Step Sequencer plugins
- Use Step Sequencer to control rotation / straighten amount; created a jaggy curve using the interpolation feature
- Use the LFO to cycle the amount of shake (a small range near 0.0 - 0.1 is good, use min/max handles to adjust)
8. Apply FX to the main output for a final style pass
- VHS Glitching
- LUT FX (dystopia, zombies, etc)
- Color Controls (for adjusting overall brightness / contrast / saturation)
- v002 Vignette

### Exercises

#### Create Stylized FX Chains
1. Use the 'Simple Mixer' or '4 Channel Mixer' or '4 Layer VJ Starter' template
- Trigger the same media on each layer
- - Tip: You can set the source of a layer to be the content from another layer from the 'Use Source' menu
- Create a different FX style for each layer
- Save FX chains as assets for later use; rename, edit and manage from Workspace Inspector > Assets
2. Add a Movie Recorder plugin and capture still images of each different style applied to different source materials

#### DJ / VJ Techniques
1.  Use the 'Simple Mixer' or '4 Channel Mixer' template, along with DJ mix
- Use Shape Mask and RGB EQ FX to composite layers
- Make MIDI / keyboard mappings for instrumental control over parameters, such as the master opacity, EQ / mask levels and crossfader
- Practice crossfader techniques
2. Switch clips and FX chains to match musical changes; think about:
- What clips are needed for a general VJ library vs a specific show / idea?
- When to fade out the main output to black / a solid color for a 'pause' in the visuals?
- How can the crossfader data-source from the Two Channel mixer be used to automate parameters for FX?

#### Retro Halloween Visual Style
1. Follow the provided steps to create the project, or start from the pre-made project file.
2. Add your own 'logo' files – for the best results try using square images / videos that are black and white with alpha channels
- If using media with alpha, try switching the 'graphics' layer composition mode to OpenGL Over mode
- What techniques can be used to add alpha / transparency?
3. Try different FX combinations:
- How does changing the order / layering of the project change the output?
- What retro FX can be used?
- What FX could be used to create a more modern visual styling using the same source logo materials?
4. Try different data-source assignments:
- What other parameters can be automated using:
- - LFO and Step Sequencers
- - Audio Analysis
- - MIDI / OSC control

## Lesson 2: Mood board / storyboarding

[Handout: Mood board / storyboarding](/vvedu/handout_module_5.html)

A visual performer will need to plan out the theme, setting, and mood for a performance or a production before any editing, composing or programming begins. They will also want to plan out, or “[storyboard](https://en.wikipedia.org/wiki/Storyboard)” a script for choreographing various forms to music.

Start by creating a primer, or “[mood board](http://www.gomoodboard.com/),” for the overall style, palette, and patina for the visual design. This may include a collection of colors, graphics, textures, image references, screen grabs, etcetera. Lay them out using your preferred image viewer (Finder, Preview, Bridge, et al) or make a collage Photoshop. [Pinterest](https://www.pinterest.com/) is another resource for collecting images of a certain theme.

Next, storyboard the desired sequence for your music. In the animation industry, storyboards are comprised of “extremes and in-betweens.” Extremes are moments that set the exact mood, emotion, or key image in a sequence. In-betweens are the transitional frames that move from one extreme to the next.

### Lesson Overview

In this demonstration we'll be making a space themed mood board and evolve that into some sketches and a storyboard; teachers should feel free to swap in their materials for these exercises.

* Using VDMX as a sketchpad to work out ideas, create demos
* * Experimenting with camera angles for live shows
* * Using photos as a fake background in the canvas
* Screen grab or image capture stills 

* Creating “mood boards” to define style and general aesthetics 
* Storyboarding for pacing and spacing of visual events and transitions, i.e., “extremes and in-betweens”

### Special Equipment

Required:
- 

Recommended:
- Space Mood Board collection

### Lecture Notes

1. Moodboards
- Used to help define style, feeling and general aesthetics
- Usually an informal process. Start with using whatever tools you feel most comfortable with, then compile into a PDF or other collection for sharing with collaborators
- Can be made up of images, sounds, videos, gifs, text and any other media that helps describe the ideas
- Okay to use stock footage, snippits from films, images from the net; we are not going to use these materials, nor copy them, for the final product, but we can use them for inspiration, to describe particular styles and to better understand existing visual languages

2. Storyboard template and examples

### Discussions

* Example mood board: Space

### Demonstrations

#### Creating mood boards

Mood boarding: A primer, or “mood board,” is used to gather ideas for the overall style and palette for the visual design. This may include a collection of colors, graphics, textures, image references, screen grabs and sketches.

A project may have multiple mood boards that apply to different sections, or to create juxtapositions; for example, if working with a musician, you may create mood boards to go along with different songs within an album, or you may mix a few contrasting themes within a song.

1. Create an ad-hoc categorization of sub-ideas or themes. This can be a recursive process that changes as you collect more materials.

For this example we'll be using ‘space’ as our sample theme; this can cover a lot of areas, such as:
- space travel
- - life in space
- - spaceships
- stars, planets, moons and other celestial objects
- - viewed from afar
- - viewed from close up
- the void
- - dark matter
- - black holes
- - vortexes
- - unexplained phenomena 
- aliens / alien civilizations
- - alien bodies
- - alien culture
- - alien language
- - alien technology
- - first contact
2. Create an organizational structure for storing ideas.
- In this case we will start by creating in the Finder a folder for the mood board and include sub-folders for each of the top-level theme categories mentioned. The sub-categories can initially be used as a guide and later used to create more specific sub-folders if needed to help organize our thoughts.
- You can use whatever tool you are most comfortable with at this phase; [Pinterest](https://www.pinterest.com/), Google Drive and similar online tools can also be useful, particularly when working on collaborative mood boards.
- Links can be gathered as “url link files” in folders, or collected in text files, using google docs or similar tools
3. List some examples of available resources (on and offline) to collect ideas,
- Online:
- - [Google Image Search](https://images.google.com/) / [flickr](https://www.flickr.com/) / [Instagram](https://instagram.com)
- - [Pinterest](https://www.pinterest.com/)
- - [YouTube](https://youtube.com) / [Vimeo](https://vimeo.com)
- Offline:
- - Taking photos / shooting video in nature, cities, etc
- - Books (eg images, text – usually phrases, quotes, poetry or short stories)
- - Friends
4. Walkthrough making a ‘space’ mood board using the listed resources / as a class discussion, or use the pre-made collection available as a resource with this lesson

#### Using VDMX as a sketchpad: Creating a Stargate

Note: This tutorial is based on [Creating a Generative Stargate in VDMX](https://vdmx.vidvox.net/tutorials/create-a-generative-stargate)

1. Starting from our mood board images referencing from the work of legendary FX artist Douglass Trumbull. The general approach will be to replicate some of the look and feel from works Trumbull accomplished optically, such as,
- a “slit/scan” setup
- the “Jupiter Machine”
- the solarization effects found in the Stargate sequence of 2001: A Space Odyssey. 
2. Create basic stargate
- Load the 'Simple Player' template
- Add space images to the media bin and trigger an image
- - In the layer composition controls, set the sizing mode to “fill” so that the image is expanded to fill the entire frame when it does not match the aspect ratio of the canvas
- Group the layer and add FX to the group; using a group allows us to control the aspect ratio / render size of the vortex regardless of what media is used as the source
- Add FX to group
- - Film > Dirty Lens
- - Glitch > Bad TV
- - - Animate the scroll slider using the clock > measure position data-source (or a multi-bar variation for a slower effect)
- - Circle Wrap Distortion
- - Twirl
- - Lens Flare
- - - Adjust Bias, Scale, Source Gain and Halo Width properties
- - Optical Flow Distort
- Shockwave Pulse
- - Set center position, rate, magnitude
- - Use pulse button to create a pulse
- Optional: Add a 'Linear Gradient' and trigger
- - Adjust gradient colors to be purple hues (mix of red / blue, one light one dark)
- - Set gradient to vertical display
- - Animate the offset slider using the clock > measure position data-source (or a multi-bar variation for a slower effect)
- Add background image
- - Add background layer
- - Trigger photos to background layer
- - Use “fill“ sizing mode for background layer
- - Apply Geometry Adjustment > Side Scroller and Flip.fs to background layer to offset such that a dark section is in the middle
- - Set vortex layer to use GLSL > VVSourceAtop.fs composition mode (maintains alpha channel within groups), set Group to use OpenGL Over

Next, to soften the look, RGB Trails 3.0 is added along with a Twist and a Shockwave Pulse, to really sell the look of a high energy source.

#### Optional Demonstration: Using fake backgrounds for pre-visualization
1. Starting from the 'Simple Mixer' template
- Add Movie Recorder plugin
- Add 'Freeze Frame.fs' to each layer FX chain (in the Utilities category)
2. Experimenting with camera angles for live shows
- Add example set of photos taken from different angles
- What shots work the best for the desired visual style / mood?
3. Using photos as a fake background in the canvas
- From the Workspace Inspector > Plugins
- - Add a new media bin
- Add a new page to the bin and add venue background example images to project
- From the Workspace Inspector > Layers
- - Group the left and right layers
- - Set the blend mode of the group to OpenGL Over
- - Add a new background layer
- In the new media bin window, set the target to the new background layer
- Trigger venue example 1
- Use the Layer Composition controls from Group 1
- - Switch to 'quad' mode
- - Position handles to match projection location in background image

#### Creating storyboards

Storyboarding: A storyboard takes the elements derived from the mood board and places them in time, typically matching up events such as style changes with important moments in other elements of the show production, such as the music or theater scene changes.

For this demonstration we will continue building on the basic vortex.

1. For selected piece of music, 
- note the major changes in sections (can we tell this from looking at FFTs / waveform views?)
- create a color / characteristic / tone guide based on the feeling of each section
- what elements of the music move fast / slow?
- where are the transitions in the music?
- what elements of our media sketches can be animated?
- what translations / mappings between audio and video elements might be interesting?
2. For each note transition within the music
- what will the visual output be during the transition?
- - adjust the vortex until it looks appropriate
- - create a workspace preset
- - use the movie recorder to capture an image / video
- what will the visual output be after the transition?
- - adjust the vortex until it looks appropriate
- - create a workspace preset
- - use the movie recorder to capture an image / video
3. Use Adobe Photoshop / Illustrator, Affinity Designer / Photo or similar to lay out images for the storyboard and save as an image
- Use VDMX if you'd like!

### Exercises

#### Create a Vortex
1. Create the basic vortex as described above, or use the provided project and skip this step
2. Add your own image files
- What combinations of backgrounds and vortex images work well together?
3. Try different FX combinations:
- How does changing the order / layering of the FX change the output?
- What other FX can be used to create a similar style?
4. Try different data-source assignments:
- What parameters can be adjusted to fade the vortex in / out?
- What other parameters can be automated using:
- - LFO and Step Sequencers
- - Audio Analysis
- - MIDI / OSC control
5. Challenge: Adapt the 'Four Channel Mixer' template such that the left mix is the vortex and the right mix is the background image
- Tip: Don't forget to use the layer groups for FX

#### Create a mood board
1. Using described techniques, create two mood boards, each of at least 10 images. Suggested themes:
- Nature
- City
- Sports
- Glitch
- Animation

#### Create a story board
1. For a selected sound tone / sound effect / music section, create a story board using described techniques.



