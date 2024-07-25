---
title: Module 1 Lesson Plans
keywords: 
last_updated: August 24, 2018
tags: [lesson_plans, live_visuals]
summary: "Module 1: Live Visuals"
sidebar: home_sidebar
permalink: teaching_module_1.html
folder: teaching
---

# “Live” Visuals Overview

VJ’ing stems from “[Projection Design](https://www.svenortel.com/projection-design-as-design-discipline/),” a term chosen by scenic artists to refer to designers who worked with film and video projectors in theatre. The title has since grown beyond the technical. It now includes LED fixtures, TV monitors, computer screens, interactive visual instruments, Pepper's Ghosts and Eyeliners to creative holographic images, and so on. Our field now generally involves putting an image on the stage that is ephemeral and changeable.

The input and output of your images will have a great influence on content, context, aesthetics, and meaning. It is also a great way to play with “practical” effects, by having the materiality of the “screen” and/or the inherent aesthetics of the input device help further define your art.

## Lesson 1: Input to Output

[Handout: Input To Output](/vvedu/handout_module_1.html#lesson-1-video-input-to-output)

In this lesson we will explore the three most basic parts of our VJ toolkit – inputs, filters and outputs.

The inputs, or sources, are the materials that contain the content of our work, whether they be pre-rendered files, live feeds or real-time computer generated visuals.

This imagery is then processed by “filters” also commonly known as effects or FX, which modify the stream of pictures to change the aesthetics and overall feeling associated with them.

Finally the result is sent to a place where it can be viewed, output to a screen, projector, a movie file on a hard drive or streamed to the Internet.

One of the most powerful aspects of working with “live” video is the ability to experiment with the addition of live-camera feeds into your project. Consider how the live presence of your face/body influences the meaning of your imagery. You are now part of the subject matter, so consider your relationship to the pre-existing forms.

### Lesson Overview

* What is a video signal?
* What are the different types of media files for live visuals?
* What is a video codec?
* What is video videoinstrumentalism?

* Inputs / Sources in VDMX
* * Pre-rendered files
* * * Movies, animated gifs, PDFs
* * * Still images
* * Interactive generators
* * * ISF, Quartz Composer, CoreImage, Vuo
* * * Custom apps (connected by Syphon)
* * "Live" feeds
* * * Cameras
* * * Capture devices
* * * NDI® (network streaming)
* * * Syphon (share video between apps)
* * * Screen / window capture
* * * Internal feedback loops
* FX and Composition
* * Adding filters between input and output
* * Compositing layers
* * * Blend modes
* * * Mixing
* * * Groups
* Outputs
* * Previews
* * Fullscreen output
* * * Using projectors / displays
* * * System Preferences: Displays
* * * Color calibration
* * Recording movies
* * * Capture to h.264 for uploads to YouTube, Vimeo
* * * Capture to PhotoJPEG / HAP for live remixing
* Saving your work
* * Use cmd+s to save a snapshot of the current workspace to disk
* * Use 'Workspace Inspector' > 'Presets' to create multiple setups in a single project file

### Special Equipment

- [Sample Media files](https://d3omao0uy1rjjh.cloudfront.net/vvedu/M1-L1.zip)

Though not required for this lesson, the following extra equipment can be used for in class demos and exercises as described below:
- Blackmagic Input / Output devices (or similar)
- External monitors or projectors (and appropriate cables) for fullscreen outputs
- An ethernet switch or router (and appropriate cables) for NDI® video stream sharing
- An account on YouTube or Vimeo

### Lecture Notes

- [Input to Output Lecture Video](https://vimeo.com/289316023)
- [Input to Output Lecture Slides](https://docs.google.com/presentation/d/12Arx326oMkRXVu9xjnftlviyvkbhXMy1qJ31yW3yVuc)

- What are visuals? A historical context.
- - Theater
- - Light projections
- - Film
- - Video
- What is video?
- - What is a video signal?
- - - How is video different from film?
- - - Analog (eg NTSC, PAL) vs Digital
- - How is video transmitted and stored?
- - - Types of cables
- - - Physical media and digital files
- What is a media codec?
- - How do image / video codecs work?
- - What image / video codecs are commonly used today?
- Video generators
- - Analog synthesizers
- - Digital video synthesizers: Using code to create interactive imagery
- What is video videoinstrumentalism?

### Discussions

* Why live visuals?
* What shows / artists / music / movies / and other media has inspired you?

### Demonstrations

[Input to Output Demonstration Video](https://vimeo.com/289319159)

In this demonstration you will walk through the basic steps for loading a template, trying different media source types, adding FX, using fullscreen output and recording a movie to disk.

#### Introduction to sources
1. New project in VDMX
2. Load 'Simple Player' or 'Simple Mixer' from Templates menu.
3. Load sample set of clips into media bin (includes movies, animated GIFs, PDFs, still images, ISF and Quartz Composer examples)
- Trigger movie file and explain movie source controls
- Trigger animated GIF, PDF
- Trigger still image
- Trigger ISF / Quartz Composer
- Explain interactive controls
- Shift+click on media files to select them, drag selected files to re-arrange
- Right+click to find 'close gaps' and other useful options
4. Open Media Browser (cmd+3) window
- Add Live Inputs to project
- Close browser window
5. Trigger live input / webcam
6. Launch Syphon demo apps: Simple Server, Project Milk Syphon
- Select option from Layer Source menu
- Add to media bin from media browser or right+click menu
7. If available, demonstration using Blackmagic capture
8. If multiple computers are available, use NDI® test apps or another copy of VDMX to demonstrate NDI send / receive

#### Introduction to FX and Composition
Continuing from above.
1. Use 'Load Asset' menu from the Layer 1 FX window to add FX.
- Load the 'Color Effect' > 'Duotone.fs' filter
- Demonstrate usage of input parameters, Wet/Dry slider
- Load the 'Color Adjustment' > 'Color Controls.fs' filter
- Adjust 'Color Controls' parameters
- Drag the 'Color Controls' to before the 'Duotone' filter
- Adjust 'Color Controls' parameters to demonstrate the difference when the order has changed
- Click '+' button to store an FX preset
2. Click the 'Preview FX' button in the Layer FX window to open the 'Workspace Inspector' in the 'Assets' tab
- Preview the '3D Rotate.fs' FX
- Adjust parameters of '3D Rotate'
- Drag '3D Rotate' from Workspace Inspector into the Layer 1 FX chain
3. Demonstrate blend / composition modes
- From the Workspace Inspector > Layers
- Add a second layer
- - Use the Use Source: menu to select a video source for Layer 2
- Select Layer 1 in the list of layers and demonstrate Layer Composition controls
- - Adjust the size and position of Layer 1
- - Adjust the opacity of Layer 1
- - Demonstrate difference between OpenGL Add and OpenGL Over when adjusting opacity
- - Note that other compositions modes and related topics will be covered in depth later
4. Mixing between layers
- Load the Simple Mixer example from the Templates menu and demonstrate using a mixer to:
- - Transition between layers manually or automatically
- - Preview content before having it go 'live' to the output
- - Borrow stylistic techniques from DJing
- Load the 4 Channel Mixer template and demonstrate using the 4 Channel Mixer setup to:
- - Prepare and preview mixes before having it go 'live' to the output
- Note that there are many ways to work with multiple layers depending on the use case or preferences of the performers
- - Load the 4 Layer VJ Starter template
- - Optional: If matching MIDI equipment is available, demonstrate the APC Mini or nanoKONTROL Example templates

#### Introduction to outputs
Continuing from above.
1. Fullscreen output (for projectors, displays)
- In VDMX, open the Fullscreen outputs window (cmd+f)
- Switch from 'Window' tab to 'Fullscreen' tab
- Demonstrate enabling / disabling fullscreen display on the main monitor and / or external screen
2. System configuration
- Launch System Preferences
- Switch to 'Displays' settings
- Demonstrate 'Gather Windows' for external displays
- Explain difference between 'extended desktop' and 'mirroring' modes
- Point out the color calibration options (perform demonstration if time permits)
- Switch to 'Mission Control' settings
- Point out disabling 'displays have separate spaces' for hiding the menubar on external screens
3. Recording to disk
- Switch back to VDMX, open the Workspace Inspector to the Plugins tab
- Add a 'Movie Recorder' plugin
- Walk through 'Movie Recorder' main interface controls and inspector panel
- - What source / layer is being recorded? Before or after FX are applied?
- - Is audio being recorded? Which audio input is being captured?
- - What codec is being used for capture? What are the trade-offs?
- - What frame rate is being used for capture?
- - Are the files going to be automatically added to the media bin?
- - Where are the files being stored on disk? (default is "~/Movies")
- Click the 'Image' button to capture an image
- Set the video codec to h.264 to capture a movie for upload
- Click the 'Record' button to begin recording a movie
- Click the 'Stop' button to finish recording a movie
- Locate the movie file on disk (if using auto load to the media bin, right+click on the file and use the 'Reveal in Finder' option)
- Upload file to youtube, vimeo, or social media site (if using Chrome you may need to change the file extension to .mp4 for some sites)
4. Syphon / NDI® output
- Switch back to VDMX, open the Workspace Inspector to the Plugins tab
- Add a Syphon Output plugin and an NDI® Output plugin
- Demonstrate receiving Syphon in the Simple Client demo app
- Demonstrate receiving NDI – if possible on another computer
- What is the difference between Syphon and NDI? When do we use one vs the other?
- - Syphon is faster and higher quality, but only works between software on the same computer. NDI can be used over a local network.

### Exercises

#### Working with sources
1. Download or access 'Example Media File Types' collection.
2. Load the VDMX 'Simple Player' template.
- Launch VDMX
- Choose 'New Project'
- From the 'Templates' menu, choose 'Simple Player'
3. Drag the 'Example Media File Types' folder into the Media Bin
- Trigger clips and adjust playback parameters
4. Open 'Media Browser' Window
- Drag built-in sources and live inputs into Media Bin
- Trigger live inputs

#### Working with FX
1. Use 'Load Asset' menu from the Layer 1 FX window to add FX.
- Try various FX that look interesting
- Reorder FX to see how stacking changes the results
- Click the '+' button to save FX-chains for quick switching
- Click the 'Save Asset' button to save FX-chains to use globally
- Click the 'Preview FX' button to use the Workspace Inspector / Assets section to preview FX before adding them to a layer.

#### Working with outputs
1. Open System Preferences
- In Displays section, configure resolutions for main screen / external displays
- In Displays section, use the color calibration option (time permitting)
2. In VDMX, open Fullscreen settings window (cmd+f)
- Switch between floating window and fullscreen modes
- If multiple displays are connected, set to using 2nd screen for display
- In Workspace Inspector under Layers, use the 'MASTER FADER' slider to fade the final video in and out
3. In VDMX, open the Workspace Inspector under Plugins and add a Movie Recorder plugin
- Set the option to record to h.264 in the inspector
- Disable audio recording if desired
- Use the 'Image' and 'Record' options to capture several still images and videos with different FX applied to the live camera
- Pick your favorite images / videos and upload to youtube / vimeo / instagram / facebook / twitter / etc
- - On most social media sites, video clips less than 6 seconds long will automatically loop.
- - You may need to change the file extension from .mov to .mp4 before uploading for some sites. Note that this does not recompress the video, just changes the file extension to trick the uploader. The actual video codec must be h.264 for this trick to work.
4. In VDMX, open the Workspace Inspector under Plugins and add an NDI® Output plugin
- Select a video signal and optional audio device to stream
- Use NDI® Video Monitor test app to confirm stream
- If students are on a local area network via ethernet, practice sending and receiving streams from computers, applying FX and sending them back for others to remix further.

## Lesson 2: Responsiveness

[Handout: Responsiveness](/vvedu/handout_module_1.html#lesson-2-responsiveness)

VJ’ing design is a [cybernetic](https://en.wikipedia.org/wiki/Cybernetics) art form; we are essentially creating a visual instrument. The goal of many visual performers is to have a close and immediate interface with computers, to make them expressive. Their goal is to use these machines to emote, thereby making the computer's presence invisible. 

For live performance, particularly for live music, the element of improvisation and responsiveness matches the energy and ephemeral quality of the performance in a way that pre-rendered and cued/time coded imagery cannot. 

In addition, the imagery and its delivery systems (playback software, MIDI controllers, analog mixers, and so on) can be refined and tweaked over time, similar to way music may evolve during rehearsals on a tour—fusing a symbiotic relationship between the musicians and the visualist.

The presence of real-time effects and audio-responsive imagery increases the synaesthetic relationship between image and sound, thereby creating a more “live” experience for the audience.

This week, we will explore interactive concepts that extend the moving image beyond the timeline to real-time interactive expression, using data mappings from physical interfaces such as keyboards, MIDI, OSC and DMX lighting boards.

### Lesson Overview

* What is responsiveness?
* What is a cybernetic artform?
* What are physical and sensory inputs?
* What are MIDI, DMX and OSC? In what ways are they different?

* Add audio reactivity to FX and layer parameters
* Add MIDI control to FX and layer parameters
* Add OSC control to FX and layer parameters
* Media bin setup
* * Keyboard / MIDI / OSC triggers
* * Enabling media preloading
* Control surface plugin
* * Adding UI items
* * Control from webpage - for situations where a MIDI / OSC controller is not available, custom interfaces can be created with the Control Surface and controlled from a smart phone or tablet

### Special Equipment

- [Sample project](https://d3omao0uy1rjjh.cloudfront.net/vvedu/M1-L2.zip)

Though not required for this lesson, the following extra equipment can be used for in class demos and exercises as described below:
- One or more MIDI controller
- iOS Device with TouchOSC or Lemur installed
- A USB audio interface

### Lecture Notes

- [Responsiveness Lecture Video](https://vimeo.com/290539286)
- [Responsiveness Slides Notes](https://docs.google.com/presentation/d/1Dd04BLD53DW9HhfK7iyAmnumrnaLyUA8HimJAjkzSrY)

- What is responsiveness?
- What is a cybernetic artform?
- What physical interfaces are used to “perform” with computers / machines?
- What are MIDI, DMX and OSC? In what ways are they different?
- - What is MIDI?
- - What is DMX?
- - What is OSC?
- - A comparison of MIDI / DMX / OSC
- - Choosing a MIDI / DMX / OSC controller
- What are sensory inputs?
- - Sound
- - Visual

### Discussions

* Why is responsiveness an important part of live visuals?
* Why use MIDI and OSC instruments / controllers for live performance?

### Demonstrations

[Responsiveness Demonstration Video](https://vimeo.com/290573189)

For these demonstration, begin from using the modified 'Simple Player' template project from the previous lesson.

#### Audio Analysis
1. From the Workspace Inspector under Plugins, add an Audio Analysis plugin
2. Use the Audio Analysis inspector to select an audio device that has an incoming signal; this can be a built-in microphone, soundflower or other interface
- If it will not cause a feedback loop of sound, optionally also set the audio play-thru option for previewing the audio stream
3. Right+click on the threshold slider control in the Duotone FX and select an audio analysis filter
- Adjust the min / max range handles on the slider control to demonstration scaling of the data source range
- Inspect the slider with the UI Inspector, and use the sub-inspector for the receiver section to 'invert' the audio level data source
- Use the UI Inspector for the 'Section Preset' control in the Layer FX window to update the FX-chain preset, if one is used. Otherwise, create a new FX-chain preset now.
4. From the Audio Analysis inspector, add an additional audio filter band and reposition
- Right+click on the hide/show button in the Layer Composition controls for Layer 1 and select the new audio analysis band
5. Inspect the button with the UI Inspector
- Select the audio receiver from the list
- Adjust the threshold level so the button toggles at varying amount of sound input (low, mid, hid)
- Switch button receiver between toggle and match value modes and demonstrate differences

#### MIDI Receiving
1. Connect a MIDI controller to the computer
2. Right+click on the threshold slider control in the Duotone FX and select the 'MIDI Detect' option
- Send MIDI from a knob or slider on the controller to make the assignment
- Demonstrate reacting / performing on the parameter with the physical slider along with sound
- Note that the min/max and invert options demonstrated for audio analysis can also be used to change the behavior of MIDI assignments
3. From the Workspace Inspector > Plugins, add a Comm Display plugin
- Set to display incoming MIDI
4. Right+click on the hide/show button in the Layer Composition controls for Layer 1 and select the Detect MIDI option
- Press a button on the MIDI controller to send data and make the assignment
5. Inspect the button with the UI Inspector
- Select the MIDI receiver from the list
- If the device supports variable velocity on button press, demonstrate threshold setting
- Switch button receiver between toggle and match value modes and demonstrate differences
6. Demonstrate using the Hardware Learn option to make multiple assignments without using right+click or the UI Inspector
- Use the receivers inspector, or right+click on the button, to disable the connection
7. If using a MIDI controller that supports bi-directional communication, use the UI Inspector for sliders, buttons, etc, select the 'Enable Echo for all receivers'
- In the 'opts' tab for buttons, configure the values sent back for on / off states

#### OSC Receiving

If using TouchOSC...
1. Connect iOS device to wifi network
- If needed, use the "Create Network..." option from the wifi menu to create a temporary network
2. Launch TouchOSC on iOS device
3. Use the Bonjour setup to auto-configure TouchOSC sending for the IP and port of VDMX
- If needed, open the VDMX preferences under OSC to configure input ports
4. Load the Beatmachine template in TouchOSC
5. Demonstrate the same walkthroughs from MIDI listed above, using the available sliders and buttons in the Beatmachine template

If using Lemur...
1. Connect iOS device to wifi network
- If needed, use the "Create Network..." option from the wifi menu to create a temporary network
2. Launch Lemur on iOS device
3. Configure IP and port for VDMX
- If needed, open the VDMX preferences under OSC to configure input ports
4. Load the 'Studio Combo' template
5. Demonstrate the same walkthroughs from MIDI listed above, using the available sliders (faders) and buttons (drumpads / keyboard) in the Studio Combo template

If using OSCTestApp...
1. Launch OSCTestApp; this does not require any additional network / wifi configuration
2. Select detected VDMX or manually configure IP and port for sending
- If needed, open the VDMX preferences under OSC to configure input ports
3. Demonstrate the same walkthroughs from MIDI listed above, using the available sliders and buttons the OSCTestApp interface

Other OSC demo tips:
- Use the UI Inspector to create mappings for MIDI and OSC receivers to a single slider / button / etc at the same time.
- From the UI Inspector for sliders, buttons, etc, select the 'Enable Echo for all receivers'
- - In the 'opts' tab for buttons, configure the values sent back for on / off states

#### Media Bin configuration
1. Inspect the Media Bin plugin
2. From the 'Triggers' tab, clear the existing keyboard shortcuts from the template
3. Use the 'Detect' option to create new assignments for a MIDI or OSC controller
4. In the 'Control' tab, assign a MIDI or OSC slider to the 'trigger by float' option to demonstrate clip selection from a single input control
5. In the 'Options' tab, enable the Preload Media option to speed up triggering
6. If using a MIDI or OSC controller that supports bi-directional communication, demonstrate using 'echo' mode in the media bin from the 'Sending' tab

#### Control Surface plugin basics
1. From the Workspace Inspector > Plugins, create a new Control Surface plugin
2. Using the sub-inspector for the Control Surface, add a button, slider and color picker to the interface
3. Right+click on the threshold slider for Duotone and set it to use the slider from the control surface
4. Also demonstrate control+drag from the slider in Control Surface to the threshold slider (or another slider) for fast assignments
5. Control+drag from the color wheel in Control Surface to the color swatch in the brightColor (below the 'sample' button) to create a quick assignment
6. In the Duotone FX, click on the color swatch for brightColor to demonstrate it can be inspected like other UI items
7. Control+drag from the toggle button in Control Surface to the on/off button for the Duotone FX to create a quick assignment
- What are the differences between toggle and momentary buttons in the Control Surface?
- - Note that the on/off button follows the state of the CS button
- - Inspect the button in the Control Surface
- - Using the UI Inspector, change the button from a toggle to a momentary button
- - Recreate the connection by control+drag to the on/off button for Duotone
- - Note that the on/off button toggles between states when the CS button is pressed
8. Note that the Control Surface includes many other options that will be covered later, including the ability to customize the layout
9. Web browser access to Control Surface plugins
- Open the VDMX preferences and go to the OSC section > OSCQuery
- Click the link to open the HTML page; your default browser should open to a link like "http://10.0.1.14:2346/index.html?HTML"
- Use the UI items in the web browser and note that they change VDMX
- Adjust UI items in the VDMX control surface and observe that they change in the browser
- Optional: Have students open the link on their smart phones, tablets, or desktop computers and let them remote control the output. Another suggestion is to have a tablet or smart phone already loaded with this page to pass around.

#### Slider Presets
1. Click on a slider that is connected to an FX parameter to inspect it
- Switch to the 'Presets' tab of the UI Inspector
- Add a preset that set the slider to manual control
- - Use the sub-inspector to configure preset properties, such as whether or not the value gets restored.
- Configure the slider to receive from a data-source
- Add another preset for the receiving state
2. Switching presets
- Demonstrate clicking on buttons in slider UI to switch presets
- Use the UI Inspector > Presets tab to detect shortcuts (key / MIDI / OSC) to switch presets

### Exercises

#### Audio Analysis
- Add Audio Analysis plugin to existing project
- Create links between audio filters and parameters (source controls, FX, opacity)
- Adjust ranges for audio levels on sliders
- Invert audio data source receivers using the UI Inspector
- Adjust thresholds for buttons

#### Keyboard / MIDI / OSC Receiving
- Right+click on buttons and use 'Detect Key' to create keyboard assignments
- If available, connect MIDI or OSC controller
- - Create MIDI / OSC assignments using right+click and detect
- - Create MIDI / OSC assignments from the UI Inpsector
- - Use 'Hardware Learn' to create multiple assignments
- Update FX-chain presets using the UI Inspector for the Section Preset bar

#### Media Bin configuration
- Inspect the Media Bin plugin
- From the 'Triggers' tab, clear the existing keyboard shortcuts from the template
- Use the 'Detect' option to create new assignments for a MIDI or OSC controller, or using keyboard shortcuts
- In the 'Options' tab, enable the Preload Media option to speed up triggering
- If using a MIDI or OSC controller that supports bi-directional communication, use the 'echo' mode in the media bin from the 'Sending' tab

#### Control Surface plugin
- Create one or more Control Surface plugins
- Add sliders, buttons and color pickers
- Link controls to FX-chains and other parameters
- Use audio, MIDI, OSC and keyboard data-sources to drive UI elements in the Control Surface plugin
- Use the 'Section Presets' in the Control Surface plugin to save and load UI element collections and routings

#### Slider Presets
- Configure FX parameter sliders to have 2 or more presets
- Assign shortcuts (key / MIDI / OSC) for changing between slider presets
