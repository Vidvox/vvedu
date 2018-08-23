---
title: Module 1 Lesson Plans
keywords: 
last_updated: August 22, 2018
tags: [lesson_plans, live_visuals]
summary: "Module 1: Live Visuals"
sidebar: home_sidebar
permalink: teaching_module_1.html
folder: teaching
---

# About This Document

This page contains a list of lesson plans for Module 1: “Live Visuals”

For each lesson you will find the following resources:
* Lesson description: A short introduction describing the concepts, exercises and goals associated with the lesson.
* Handout: A link to a handout that can be provided to students that includes notes and useful reference links from the lesson.
* Lecture notes: Starting points for material that can be used to explain lesson topics in the form of a lecture or presentation.
* Demonstrations: A list of suggested in class lessons that you, the teacher, should walk-through as demonstrations for the students to observe or follow along.
* Exercises: A list of suggested tasks that students can work on in class individually or in small groups.
* Discussion: Ideas for guided group conversations based on topics related to the lesson.

It is recommended that you go through this material yourself in advance of each lesson as a refresher.

## “Live” Visuals Overview

## Lesson 1: Input to Output

### Lesson Overview

[Handout: Input To Output](/handout_module_1.html#lesson-1-video-input-to-output)

* What is a video signal?
* What are the different types of media files for live visuals?
* What is a video codec?

* Inputs / Sources in VDMX
* * Pre-rendered files
* * * Movies, animated gifs, PDFs
* * * Still images
* * Interactive generators
* * * ISF
* * * Quartz Composer
* * * CoreImage
* * * Vuo
* * * Custom apps (connected by Syphon)
* * Live feeds
* * * Cameras
* * * Capture devices (blackmagic)
* * * NDI® (network streaming)
* * * Syphon (share video between apps)
* * * Screen / window capture
* * * Internal feedback loops
* FX
* * Adding filters between input and output
* * Cropping
* Outputs
* * Fullscreen output
* * * Using projectors / displays
* * * System Preferences: Displays
* * * Color calibration
* * Recording movies
* * * Capture to h.264 for uploads to YouTube, Vimeo
* * * Capture to PhotoJPEG / HAP for live remixing

### Lecture Notes:

1. What is a video signal?
2. What are the different types of media files for live visuals?
3. What is a video codec?

### Demonstrations:

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

#### Introduction to FX
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
- Locate the movie file on disk (if using auto load to the media bin, right-click on the file and use the 'Reveal in Finder' option)
- Upload file to youtube, vimeo, or social media site (if using Chrome you may need to change the file extension to .mp4 for some sites)

### Exercises:

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

#### 

### Discussions: