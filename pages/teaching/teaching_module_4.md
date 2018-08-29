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

[Handout: Abstract Visualization / Color Organ](/handout_module_4.html)

The synaesthetic relationship between sound and vision continues to be explored by scientists artists working today. “Color scales,” dating back to Isaac Newton, attempt to scientifically correlate musical scales with colors. ”[Color Organs](https://en.wikipedia.org/wiki/Color_organ),” instruments that generate colors based on notes, date back to the 1850s and continue to be developed. [Wassily Kandinksy](https://en.wikipedia.org/wiki/Wassily_Kandinsky), one of the founders of non-objective painting, went so far as to create a color code for sounds. He intended for his pieces to be both seen and heard, titling them as “compositions.”

This week, we will create a shape-based color organ, creating and performing forms and colors that represent specific sounds using our inner synesthete.

### Lesson Overview

* Triggering content with sound/MIDI
* Manipulating color with sound/MIDI

### Special Equipment

Required downloads:
- Abstract Visualization / Color Organ ISF examples
- [SimpleSynth](http://notahat.com/simplesynth/) or comparable app
- [MIDI Monitor](https://www.snoize.com/MIDIMonitor/) or comparable app

### Lecture Notes

* What does is the color of a sound?

### Discussions

### Demonstrations

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
Note: This recreates the 'Audio to Color' template; if you are short on time, you can demonstrate this template and skip the setup.
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

[Handout:  Audio Visualizers](/handout_module_4.html)

### Lesson Overview

* What is the shape of a sound?
* Audio Visualizers:
* * VU Meters
* * Waveform and FFT Visualizers
* * Audio Spectrograms
* * ProjectMilkSyphon
* * Booba/Kiki ISFs

* Create two layers/media bins of shapes (i.e., Booba/Kiki): 
* * Organic 
* * Polygonal 
* Augment with audio visualizers (waveforms, FFT, spectrogram)

### Special Equipment

Required:
- Example audio tracks, eg [YouTube Royalty Free Library](https://www.youtube.com/audiolibrary/music)
- [Project Milk Syphon](https://docs.vidvox.net/freebies_project_milk_syphon.html)

Recommended:
- [Soundflower](https://github.com/mattingalls/Soundflower/releases)

### Lecture Notes

* What is the shape of a sound?

### Discussions

* Booba/Kiki

### Demonstrations

#### VU Meter
1. Step 1
- Note 1
2. Step 2
- Note 2

#### Waveform and FFT Visualizer
1. Step 1
- Note 1
2. Step 2
- Note 2

#### Audio Spectrograms
1. Step 1
- Note 1
2. Step 2
- Note 2

### Exercises

#### Exercise 1
1. Step 1
- Note 1
2. Step 2
- Note 2

#### Create two layers/media bins of shapes (i.e., Booba/Kiki)
1. Step 1
- Note 1
2. Step 2
- Note 2
* * Organic 
* * Polygonal 
* Link percussional frequencies to polygons and melodic frequencies to organic
* Link colors to musical tones (ref Kandinsky primer)
* * Melodic (cool)
* * Percussional (warm)
* Augment with audio visualizers (waveforms, FFT, spectrogram)


## Lesson 3: Generative Patterns

[Handout: Generative Patterns](/handout_module_4.html)

As discussed in Stills To Motion module, we are hardwired to find patterns in shapes that are similar and arranged closely together. In this module, we can explore pattern making as a synaesthetic device, influencing the frequency, amplitude and continuity of repetitive shapes and images to rhythmic effect.

### Lesson Overview

* Tile effects
* Patterns with code (ISF compositions eg Goto10)

* Use tiling effects and data-sources to create animated generative patterns.
* Syncing tile effects to music
* Time-delay video frames

### Special Equipment

Required:
- ISF pattern compositions

### Lecture Notes

### Discussions

* 
* 

### Demonstrations

#### Tile effects
1. Step 1
- Note 1
2. Step 2
- Note 2

#### Patterns with code (ISF compositions eg Goto10)
1. Step 1
- Note 1
2. Step 2
- Note 2

### Exercises

#### Use tiling effects and data-sources to create animated generative patterns
1. Step 1
- Note 1
2. Step 2
- Note 2

#### Syncing tile effects to music
1. Step 1
- Note 1
2. Step 2
- Note 2



