---
title: Module 4 Lesson Plans
keywords: 
last_updated: August 24, 2018
tags: [lesson_plans, live_visuals]
summary: "Module 4: Visual Music"
sidebar: home_sidebar
permalink: teaching_module_4.html
folder: teaching
---

# Visual Music Overview

Abstract visualizations, or “visual music”—generative patterns and audio responsive graphics that have a direct symbiotic relationship between image and sound—can evoke a sense of space, environment, rhythm and illuminate concepts in performance without representational imagery. In a live context of improvised music and improvised visuals, abstract visualization allows music and image to be partners in the creation of an aesthetically meaningful shared experience.

Visual music is an art form inspired by and in some cases driven by [synaesthesia](https://en.wikipedia.org/wiki/Synesthesia)—the production of a sense impression relating to one sense or part of the body by stimulation of another sense or part of the body. In common cases of synaesthesia, a person will associate a sound with a color.

There is a theory that we are all synesthetes on some level. Take for instance [Booba/Kiki effect](https://en.wikipedia.org/wiki/Bouba/kiki_effect), a non-arbitrary mapping between speech sounds and the visual shape of objects. This suggests that the human brain somehow attaches abstract meanings to the shapes and sounds in a consistent way.

## Lesson 1: Abstract Visualization / Color Organ

[Handout: Abstract Visualization / Color Organ](/vvedu/handout_module_4.html)

The synaesthetic relationship between sound and vision continues to be explored by scientists artists working today. “Color scales,” dating back to Isaac Newton, attempt to scientifically correlate musical scales with colors. ”[Color Organs](https://en.wikipedia.org/wiki/Color_organ),” instruments that generate colors based on notes, date back to the 1850s and continue to be developed. [Wassily Kandinksy](https://en.wikipedia.org/wiki/Wassily_Kandinsky), one of the founders of non-objective painting, went so far as to create a color code for sounds. He intended for his pieces to be both seen and heard, titling them as “compositions.”

This week, we will create a shape-based color organ, creating and performing forms and colors that represent specific sounds using our inner synesthete.

### Lesson Overview

* Triggering content with sound/MIDI impulse
* * Prev / next / rand
* * Triggering a specific clip
* * Quantized triggering
* Manipulating color with sound/MIDI
* * RGB vs HSV (HSB)
* * 'Audio Level to Color'
* * Color organ generator and sound synth

### Special Equipment

Required downloads:
- [Color Organ ISF examples](https://d3omao0uy1rjjh.cloudfront.net/vvedu/M4-L1.zip)
- [SimpleSynth](http://notahat.com/simplesynth/) or comparable app
- [MIDI Monitor](https://www.snoize.com/MIDIMonitor/) or comparable app

### Lecture Notes

- [Abstract Visualization / Color Organ Lecture Video](https://vimeo.com/298011493)
- [Color Organs Lecture Slides](https://docs.google.com/presentation/d/1CXTZIQMsFSYijJiDYXgIL2Lk0V4NThpMwxAFhXb1g00/)

- What does is the color of a sound / tone?
- - [Color Organs](https://en.wikipedia.org/wiki/Color_organ)
- - [Kandinksy](https://en.wikipedia.org/wiki/Wassily_Kandinsky)
- - Color scales
- - Translations between sounds and imagery
- Color representations – RGB vs HSV
- Color similarity
- - Complimentary colors (varying hue)
- - Shades (varying saturation / brightness)

### Discussions

- 

### Demonstrations

- [Abstract Visualization / Color Organ Demonstration Video](https://vimeo.com/298017047)

#### Triggering content with sound
1. Prepare base project
- Load the 'Simple Player' template
- Add the 'Kuleshov' clip set to the media bin
- Inspect the Media Bin and from the options tab, enable media pre-loading for low latency triggering
- From the Workspace Inspector > Plugins, add an Audio Analysis plugin to the project
- - Adjust any input / frequencies / gain settings
2. Prev / Next / Random on sound impulse
- Right+click on the '?' button in the Media Bin and set the data-source to audio analysis > filter 1
- Use the UI Inspector to inspect the '?' button
- - In the 'Receiving' tab, select the receiver for the audio filter
- - From the sub-inspector, adjust the threshold slider to adjust the point where the button is triggered
- In the Layer Source controls, switch the looping behavior to 'Cut to Black'
- When finished demonstrating, right+click on the '?' button and disable data-sources before moving on to the next step
3. Trigger a specific clip on sound impulse
- Inspect the Media Bin
- From the 'Triggers' tab
- Clear existing triggers
- Click the + button to manually add a new receiver
- - Note that these receivers work like button receivers
- - Use the assignment menu and select the data-source to audio analysis > filter 1
- - From the UI Inspector, adjust the threshold slider to adjust the point where the clip is triggered
- When finished demonstrating, clear the triggers before moving on to the next step
4. Quantizing triggers to sound impulse
- In the main Media Bin interface, switch the Trigger On (T:) menu from 'Immediately' to 'Manual'
- - A new button will appear for quantizing triggers to a data-source
- Trigger a clip in the media bin
- - Note that it does not immediately trigger
- - Click the manual quantize button to have the cued clip trigger
- Right+click on the manual quantize button in the Media Bin and set the data-source to audio analysis > filter 1
- Use the UI Inspector to inspect the manual quantize button
- - In the 'Receiving' tab, select the receiver for the audio filter
- - From the sub-inspector, adjust the threshold slider to adjust the point where the button is triggered
- - Note that this technique can be used with keyboard, MIDI, OSC or any other data-source, and can be used to synchronise triggers between multiple media bins
- When finished demonstrating, right+click on the manual quantize button and disable data-sources before moving on to the next step

#### Manipulating color with Audio/MIDI
1. Color Representations – RGB vs HSV
- Add a 'Solid Color.fs' generator to the media bin (right+click on the page or use the Media Browser) and replicate it 3x
- Trigger the 1st solid color generator
- - Map Red / Green / Blue sliders to filter 1-3 respectively
- - Note that audio frequency levels are mapped to color channel levels
- From the Workspace Inspector > Plugins, add a Control Surface plugin
- - From the Control Surface inspector, add a Color Wheel
- Trigger the 2nd solid color generator
- - Click on the color swatch in the layer source controls and use the UI Inspector to receive from the Control Surface color wheel (or control+drag from the color wheel to the swatch)
- - Map the Hue / Saturation / Brightness (aka Value) levels to audio filters 1-3 respectively
- - Note that audio frequency levels are controlling the color via HSV instead of RGB; how are these different?

2. 'Audio Level to Color'
- *Note: This recreates the 'Audio to Color' template; if you are short on time, you can demonstrate this template and skip the setup.*
- Continuing from above
- From the Workspace Inspector > Plugins, add a Step Sequencer plugin
- - Add a color track to the Step Sequencer
- Trigger the 3rd solid color generator
- - Click on the color swatch in the layer source controls and use the UI Inspector to receive from the Step Sequencer color track (or control+drag from the color track to the swatch)
- Set the 'rate' of the Step Sequencer to 0.0, or pause
- Right+click on the 'Time' slider in the Step Sequencer and set its data source to 'Audio Analysis 1/Peak Frequency Magnitude'
- Adjust colors, steps, interpolation and time slider range such that the color transitions from black to green to yellow to red to white

3. Color Organ
- Launch SimpleSynth and MIDI Monitor
- Use the included project file, or the steps below,
- Add the 'Color Scales.fs' generator to the media bin and trigger (ref Kandinsky primer)
- Use the Notes slider and Author controls to demonstrate color palettes
- Optional: Open 'Color Scales.fs' in a text editor or ISF Editor to show its code for remixing
- Click on the 'Note' slider and use the UI Inspector
- - Switch to the 'Marks' tab
- - Add 12 'marks' and set them to 0, 1, 2, ... 10, 11
- - Use the 'detect' option to assign top row of 12 keys (or MIDI keyboard) for the marks
- - Switch to the 'Send'
- - Add a sender and set to 'MIDI' with the target of 'SimpleSynth'
- - Use the sub-inspector to set the MIDI sender:
- - - 'Note Range' tab
- - - Send note ons from 60 (Middle C) to 71
- - - Optional: 'Send Noteoffs' – disabled or enabled? try both, with different instruments selected in SimpleSynth
- - Demonstrate using keyboard to play sound and colors
- - - Use MIDI Monitor as a debug, values should go from C3 C#3 D3 D#3 E3 F3 F#3 G3 G#3 A3 A#3 B3 for each corresponding color 
- Inspect the 'Author' pop-up menu and assign keyboard shortcuts / MIDI notes to switch the color palette selection

### Exercises

#### Triggering content with sound
1. Start from 'Simple Player' template
- Challenge: Use the 'Simple Mixer' template or a project that has multiple media bins that can be configured:
- - With the same audio triggers
- - Different audio triggers
- - Using a Control Surface plugin interface button as a master control
2. If needed, add Audio Analysis plugin
3. Configure prev/next/rand to trigger on sound impulse
- Adjust threshold level using UI Inspector
4. Configure media bin trigger specific clip on sound impulse from Media Bin inspector
- Adjust threshold level using UI Inspector
5. Configure media bin Quantize Triggering for:
- Sound impulse
- Keyboard / MIDI input

#### Color organ
1. Launch SimpleSynth and MIDI Monitor
2. Start from 'Simple Player' template (or use the pre-made template and skip the setup steps 3 & 4 below)
3. Add the 'Color Scales.fs' generator to the media bin and trigger
4. Prepare the Notes slider for input and output using the UI Inspector
- Add 12 'marks' and set them to 0, 1, 2, ... 10, 11
- Assign keyboard / MIDI triggers to each mark
- Add a sender and set to 'MIDI' with the target of 'SimpleSynth'
- - Send note ons from 60 (Middle C) to 71
5. Use the Notes slider and Author controls to demonstrate color palettes
- Optional: Assign shortcuts for switching between color palettes
- Optional: Use SoundFlower and the Movie Recorder plugin to capture; use the Audio Analysis pass-thru option to preview the sound if needed
- Challenge: Modify the 'Color Scales.fs' to include your own color palette creation

## Lesson 2: Audio Visualizers and the Shape of Sounds

[Handout:  Audio Visualizers](/vvedu/handout_module_4.html)

### Lesson Overview

* What is the shape of a sound?
* Audio Visualizers:
* * VU Meters
* * Waveform and FFT Visualizers
* * Audio Spectrograms
* * ProjectMilkSyphon
* * Booba/Kiki ISFs
* * Rutt Etra

* Create two layers/media bins of shapes (i.e., Booba/Kiki): 
* * Organic 
* * Polygonal 
* Augment with audio visualizers (waveforms, FFT, spectrogram)

### Special Equipment

Required:
- [VU Meter + Booba/Kiki Example ISF](https://d3omao0uy1rjjh.cloudfront.net/vvedu/M4-L2.zip)
- Example audio tracks, eg [YouTube Royalty Free Library](https://www.youtube.com/audiolibrary/music)
- [Project Milk Syphon](https://docs.vidvox.net/freebies_project_milk_syphon.html)

Recommended:
- [Soundflower](https://github.com/mattingalls/Soundflower/releases)

### Lecture Notes

- [The Shape of Sound Lecture Video](https://vimeo.com/299289480)
- [The Shape of Sound Lecture Slides](https://docs.google.com/presentation/d/1giyeLz_rahweklOKErqaniub83oKtCK51acqb7LU2qo/)

- What is the shape of a sound?
- - [Booba/Kiki effect](https://en.wikipedia.org/wiki/Bouba/kiki_effect)
- - Waveform visualization
- - FFT visualization
- - Audio Spectrograms
- - Rutt Etra

### Discussions

* How do we describe shapes? (what words do we use?)
* Along the lines of Booba vs Kiki, are there particular shapes that you think correspond to different types of sounds or words?

### Demonstrations

- [The Shape of Sound: Demonstration Video](https://vimeo.com/299322555)

For the below demonstrations, begin by,
1. Start from 'Simple Player' template
2. Add the provided sample media visualizers to the project
3. Add an audio analysis plugin from the Workspace Inspector > Plugins
4. Optional: Configure Audio Analysis to use SoundFlower and an input and enable sound play-thru for using audio from other software

or use the pre-made project file.

#### VU Meter
1. Trigger the VU Meter ISF
2. Assign the level meter to 'Audio Analysis 1/Peak Frequency Magnitude'
3. Adjust ISF parameters

#### Waveform and FFT Visualizer
1. Add the built-in source 'FFT Color Lines.fs' to the media bin from the media browser and trigger
2. Set the waveImage and fftImage to receive from the Audio Analysis plugin
- What are FFTs? What are audio waveforms?
3. Demonstrate adjusting ISF parameters
4. Optional: Open 'FFT Color Lines.fs' in a text editor or ISF Editor to demonstrate remixability; right+click > reveal selected files in finder to locate file on disk

#### Audio Spectrograms
1. Add 'FFT Spectrogram.fs' and 'Radial Spectrogram.fs'
- Trigger each and set fftImage input to use Audio Analysis 1
2. Demonstrate the way different types of music look different when visualized with FFTs

#### Booba/Kiki Shapes
1. Booba/Kiki shape generators
- Trigger the Booba generator
- - Link parameters to audio data-sources
- Trigger Kiki generator
- - Link parameters to audio data-sources
- Trigger Booba/Kiki hybrid generator
- - Link parameters to audio data-sources
- Demonstrate audio reactivity with different soundtracks / music: which work and which feel wrong?
- - Rhythmic
- - Tonal
- - Soft
- - Glitchy
- - Abstract / Arrhythmic (wind chimes)
2. Animating Booba/Kiki image sets with FX
- Add Zoom and Rotation FX
- Link zoom and rotation controls to audio frequencies
- Optional: Use the File Inspector to have zoom / rotation FX on specific images / clips
- - From the Workspace Inspector in the Files tab
- - - Select one or more image clips
- - - In the FX tab, enable the 'Use Custom FX-Chain' toggle
- - - Add zoom / rotation FX and link parameters
- - - Click Apply
3. Use the 'Color Scores Tint.fs' FX to adjust coloring of images / generators using our Color Organ palettes

#### ProjectMilkSyphon
1. Launch ProjectMilkSyphon
- Configure input settings if needed
2. In VDMX, use the Media Browser > Syphon inputs to add the ProjectMilkSyphon to the media bin
3. Trigger the ProjectMilkSyphon feed
4. Demonstrate audio reactivity with different soundtracks: Which work and which feel wrong? Which visualizer modes work with which kinds of music?

### Exercises

#### Basic Visualizers
1. Load the 'Simple Player' template
2. Add an Audio Analysis plugin
- Configure if needed
3. Configure a VU Meter generator
4. Waveform and FFT Visualizer
5. Visualize different types of music using a spectrogram

#### Booba/Kiki
1. Load the 'Simple Mixer' template
2. Add Audio Analysis plugin
3. Create and mix between two layers of shapes and visual FX using different music on the following themes:
- Organic / Polygonal; Linking percussive (warm) frequencies to polygons and melodic (cool) frequencies to organic
- Linking colors to musical tones (ref Kandinsky primer / color organs)
4. If using generators with alpha channels / transparency, experiment with using OpenGL Add vs OpenGL Over for blending vs composition
5. Augment with audio visualizers (waveforms, FFT, spectrogram) and color organs
6. Optional: Use the Movie Recorder plugin to capture audio/video streams

## Lesson 3: Generative Patterns

[Handout: Generative Patterns](/vvedu/handout_module_4.html)

As discussed in Stills To Motion module, we are hardwired to find patterns in shapes that are similar and arranged closely together. In this module, we can explore pattern making as a synaesthetic device, influencing the frequency, amplitude and continuity of repetitive shapes and images to rhythmic effect.

### Lesson Overview

* Tile effects
* Patterns with code (eg Goto10, Sol LeWitt)
* Introduction to the ISF Editor / GLSL (optional, advanced)
* * Making a solid color generator
* * Making a basic pattern generator (strips, checkerboards)
* * Remixing compositions

* Use tiling effects and data-sources to create animated generative patterns.
* Syncing tile generators / effects to music

### Special Equipment

Required:
- [ISF Pattern Examples](https://d3omao0uy1rjjh.cloudfront.net/vvedu/M4-L3.zip)

Recommended:
- [Soundflower](https://github.com/mattingalls/Soundflower/releases)

### Lecture Notes

- [Generative Patterns Lecture Video](https://vimeo.com/300620381)
- [Generative Patterns Lecture Slides](https://docs.google.com/presentation/d/1XK6XZoEVUJylwANOwnqy4-Fsg_s24-IkM3v_DB3ljEs/)

- [Patterns](https://en.wikipedia.org/wiki/Pattern)
- - Properties of patterns
- - - Symmetry
- - - Rotation
- - - Chaos, flow, meanders
- - - Fractals
- - Patterns in nature
- - - Snowflakes
- - - Spirals
- - - Waves, dunes
- - - Bubbles, foam
- - - Cracks
- - - Spots and stripes
- - Geometric patterns
- - - Tiling
- - - Visual motifs 
- - - Kaleidoscope
- - Music Patterns
- - - Temporal
- - - Harmonic
- - - Melodic
- Introduction to GLSL (optional)
- - What are shaders?
- - Why are they fast?
- - Tools for writing shaders
- - Examples of patterns made with GLSL

### Discussions

* 

### Demonstrations

- [Generative Patterns Demonstration Video](https://vimeo.com/300632634)

#### Tile effects
1. Start from the 'Simple Player' template
- Add test media files
- Add LFO and Step Sequencer plugins and Audio Analysis
2. Using the Layer 1 FX 'Load Asset' menu, add Tiling FX to create patterns; use LFO / Clock / Step Sequencer to automate properties such as angle / rotation / size
- Mirror Edge
- Kaleidoscope / Kaleidoscope Tile
- Parallelogram Tile
- Fourfold Reflected/Rotated Tile, Sixfold Reflected/Rotated Tile, etc
- Replicate / Radial Replicate
- Shape Mask (under Masking) – how can masks be used to create and composite patterns on multiple layers?
3. Demonstrate different media types with each Tile FX
- No motion (stills or paused video)
- - Tip: The Utility > Freeze Frame.fs FX can be used to hold on a frame; be sure to place before any animated tiling FX
- Slow motion
- - Tip: The Blurs > VVMotionBlur.fx FX can be used to slur visuals; try before and after tiling FX
- Fast motion
4. Syncing tile effects to music, reviewing prior techniques:
- BPM Sync in Clock plugin
- Using Clock / LFO / Step Sequencer to drive parameters
- Color adjustments / selection
- Changing patterns (clips) on sound impulse vs clock control
- Refine timing of LFO and Step Sequencer plugins using the concepts from the Rhythmic Sequence lesson:
- - Regular rhythm: Intervals between sizes are the same in duration (i.e., one second per size)
- - Progressive rhythm: The size of shapes are changed over a progression, getting faster towards the end (2 sec, 1 sec, ½ sec, and so on)
- - Flowing (organic) rhythm: Occurs when the intervals are organic, used to create a feeling of visual polyphony. Think VJ’ing to wind chimes.

#### Patterns with code
1. Start from the 'Simple Player' template
- Add ISF Pattern example generator files
2. Trigger each pattern example and discuss

#### Introduction to GLSL / ISF (optional, advanced)
1. Introduction to toolset
- Using a text editor (eg BBEdit or TextMate)
- ISF Editor for macOS
- Online ISF Editor
2. Examining the 'Solid Color.fs' example
- The anatomy of an ISF:
- - JSON at the top describes the inputs and other metadata
- - GLSL at the bottom contains the code for rendering
- How does GLSL work?
- - main() function is executed for each pixel
- - Vary the algorithms used to determine the color based on pixel location to make patterns
3. Examining basic pattern generators
- Strips: Varying based on x or y position, but not both
- Checkerboards: Varying based on x and y
- Gradients: Fading across x and / or y
4. Remixing compositions
- In the Finder, duplicate one of the example pattern generators to remix
- Open the copy using the ISF Editor or a text editor (such as BBEdit or TextMate)
- Pick a parameter that is not a variable and change it to a variable
- Adjust the JSON section at the top to add a new parameter to the ISF composition for the new variable
- Save the document and load into VDMX

### Exercises

#### Use tiling effects and data-sources to create animated generative patterns
1. Start from the 'Simple Mixer' template
- Add test media files
- Add LFO and Step Sequencer plugins
- Add Movie Recorder plugin
2. Create compositions using Tiling FX
- Try using different source material with different FX combinations
- Try stacking multiple Tiling FX
- Try using OpenGL Over Mode on Layer 1 and Masking > Shape Mask.fs
3. Refine timing and control of LFO and Step Sequencer plugins using the concepts from the Rhythmic Sequence, Color Organ and other lessons
- Think about temporal patterns in addition to visual patterns
4. Use Movie Recorder to capture video / still images

#### Patterns with code
1. Continuing from above exercise...
- Add ISF Pattern example generator files
2. Continue to create compositions using pattern generators and tile effects
3. Use Movie Recorder to capture video / still images

#### Introduction to GLSL / ISF (optional, advanced)
1. In the Finder, duplicate one of the example pattern generators to remix
2. Open the copy using the ISF Editor or a text editor (such as BBEdit or TextMate)
3. Pick a parameter that is not a variable and change it to a variable
4. Adjust the JSON section at the top to add a new parameter to the ISF composition for the new variable
5. Save the document and load the composition into VDMX to use alongside other pattern generators

