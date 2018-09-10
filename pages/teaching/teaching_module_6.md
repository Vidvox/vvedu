---
title: Module 6 Lesson Plans
keywords: 
last_updated: August 24, 2018
tags: [lesson_plans, live_visuals]
summary: "Module 6: Show and Event Production"
sidebar: home_sidebar
permalink: teaching_module_6.html
folder: teaching
---

# Show and Event Production Overview

It’s showtime! 

The final piece/performance is a culmination of the experience and knowledge gained over the semester. It must utilize at three techniques demonstrated during the course—incorporating motion and sound—with a written statement as to why those techniques were used and the dramatic intent. 

This is also the opportunity to include their interests in other disciplines, and to further develop visuals which reflect their own interests.

Over the course of this section, students will work towards completing a single project that will count as the final for this course. It can take one of three forms:
- Using a selected piece of audio or musical collaboration, create and perform a three minute audio/visual piece. 
- Using a selected piece of audio or musical collaboration, create and perform a three minute demo reel showcasing your work from the semester.
- Prepare for a 15 minute live performance piece using at least three of the techniques covered over the semester.

Students can work on their own, or in a small group for this project by request at the discretion of the professor.

As we get ready for the final project and performance we will also begin to have a more in depth look at the world of show production and how to prepare for your first big events.

## Lesson 1: Pre-Production and Show Design

[Handout: Pre-Production and Show Design](/handout_module_6.html)

Using our prepared mood boards and storyboards as a starting points we begin to gather and create the individual elements for the final project / performance. This can take the form of media files such as movies, still images, animated gifs and interactive generators, custom FX, as well as any physical portions that will be needed, such as projection surfaces.

During the pre-production phase it can often be useful to work with other artists and technicians; this can help with filling in knowledge gaps and for being able to accomplish more tasks before a deadline.

In some cases the materials prepared for a show may be arranged in advanced using a system of cues running from timecode, and in other cases the event may be intended to be performed entirely live. Most of the time for event you'll have a mix of the two, with some parts improvised and other pre-scripted.

As part of planning a show design for events, multi-channel output can add a physical, spatial element to your images, which is a great way to present split screen content, creating an immersive, spatial presentation of imagery. In the event of custom screens or architectural projection, a VJ can use mapping tools to crop and transform the imagery to fit seamlessly into the environment.

In addition to multiple outputs, a VJ might incorporate live-camera feeds into their performance. This adds an additional element of presence for both the performer and the audience, allowing a more intimate window into the processes onstage, making the performer a character in the visual narrative. 

Multiple cameras can present different views of the performer at the same time, also called multiple perspective, [simultaneity](https://en.wikipedia.org/wiki/Simultaneity) or multiplicity. This allows an otherwise impossible, holistic viewing experience for every member of the audience, regardless of where they stand.

### Lesson Overview

* Multiple Inputs / Outputs in VDMX
* Timecode plugin
* * MTC, LTC and OSC sync
* * Time markers
* Using materials from other people
* * Creative Commons: Share, Collaborate, Remix, Reuse
* * What is fair use?
* * Works for hire

### Special Equipment

Required:
- Software or hardware for sending MTC
- LTC audio test file
- Software to receive MTC
- Software to receive LTC

Recommended:
- NDI® test video feeds
- Syphon test apps
- Multiple web-cameras
- BlackMagic, Magewell or similar capture devices
- - Devices that can provide HDMI/SDI feeds for capture
- [OSC Test app](http://vidvox.com/rays_oddsnends/vvopensource_downloads/OSCTestApp_0.2.4.zip)

### Lecture Notes

- Using materials from other people
- - Creative Commons
- - Fair Use
- - Works for Hire
- Introduction to timecode
- - MTC and LTC

### Discussions

### Demonstrations

#### Multiple Inputs / Outputs in VDMX
1. Creating a multi-live input setup, VDMX as a live feed switcher
- Open the Media Browser from the Window menu (cmd+3)
- - Add Live Inputs, NDI, Syphon feeds to Media Bin page
- - Close Media Browser
- Trigger each feed to activate / demonstrate connection
- From the Workspace Inspector > Plugins
- - For each live video feed, add a 'Preview Window' plugin and set the source
- - Optional: Use the 'Mouse Down' data-source from each Preview Window plugin to trigger the appropriate clip in the bin
- - - Inspect the Media Bin
- - - Use the Triggers tab to create and assign data-source receivers
- - - Enable the 'Eject on empty file' option so that clicking not on a clip ejects / cuts to black
2. Multi-live input pre-vis
- Add a Movie Recorder plugin to the project
- - Capture short video loops or still images from each live feed
- - These images and video loops can now be used as “stand ins” when real live feed are not available
3. Create a dual screen output setup; or skip initial setup steps and load “Dual Screen Example“ template (jump to System Prefs:Displays)
- From the Workspace Inspector > Layers
- - Adjust the width of the canvas to 2x its current size
- - Use the Layer Composition controls to position Layer 1:
- - - Use “onscreen” position mode
- - - Set x position to far left (0.0)
- - Duplicate Layer 1 and rename to Layer 2
- - Use the Layer Composition controls to position Layer 2:
- - - Set x position to far left (1.0)
- Optional: Create and configure a second media bin for triggering to Layer 2
- Open System Preferences:Displays and configure external displays as needed
- Open the Fullscreen Options panel (cmd+f)
- - Select the ‘Fullscreen’ tab to switch to fullscreen mode
- - Select monitors to stretch the canvas across

#### Timecode plugin

This demonstration and additional techniques can be found in the [Timecode plugin tutorial](https://vdmx.vidvox.net/tutorials/introduction-to-timecode)

Timecode Overview:
- A single Timecode plugin can only receive from one source at a time- it can receive from MTC (MIDI Timecode), LTC (Linear timecode), or from any data source in VDMX (including any MIDI/OSC/DMX data VDMX receives). Timecode plugins can also generate their own timecode locally, using a variety of framerates.
- The values received by a Timecode plugin are published in VDMX as a data source as a floating-point number describing the time in seconds.
- These values can be used to drive Cue Lists, LFOs, control movie playback directly, etc.
- A single timecode plugin can have multiple reference times, which are configured in its inspector- the time passed since the last reference time is published as a data source in VDMX, along with the index and name of the reference time.
- A single timecode plugin can publish its value to multiple destinations, in multiple formats. Values can be sent to other devices using MTC, LTC, and OSC.
- Step Sequencer and LFO plugins can time-sync with Timecode plugins just like Clock plugins.

1. Using Timecode
- From the Workspace Inspector > Plugins
- - Add a Timecode plugin
- - Use the “Reference Times” tab:
- - - Add time index 00:00:00.01
- - - Add time index 00:00:30.01
- - - Add time index 00:01:00.01
- - - Add time index 00:02:00.01
- - Demonstrate main interface:
- - - Jump to last ref time button
- - - Pause / resume button
- - - Ref times pop-up button
- - - - Use UI Inspector to assign shortcuts to jump to specific ref times
- Add sample media to project
- Inspect Media Bin
- - In the Control tab set the Trigger by Index receiver to use Timecode > ”Last ref index” data-source
- - Demonstrate switching between ref times with pop-up button
- From the Workspace Inspector > Layers
- - Add Layer 2 and set source to 'SMPTE Clock.fs'
- - Use the UI Inspector to adjust the parameters of the SMPTE time slider in the Layer Source controls:
- - - Add a data-receiver and set to use Timecode > “Time since last ref” data-source
- - - Use the sub-inspector to specify that the values are not normalized
2. Receiving MTC
- Launch MTC sending software
- - Configure to send MTC “To VDMX”
- Return to VDMX
- Inspect the Timecode plugin
- - Set the Timecode Source: to MTC
- - Select the “To VDMX” option
- - Optional: Enable 'Jam Sync' and stop sending MTC; observe that timecode continues after signal is dropped
3. Receiving LTC
- Launch LTC sending software or connect external sound feed to audio input device
- - If using sample LTC audio file, you can use QuickTime Player, iTunes or any standard soundfile playback software.
- - If using LTC software or an LTC audio file on the same computer, set sound output device to Soundflower
- Return to VDMX
- Inspect the Timecode plugin
- - Set the Timecode Source: to LTC
- - Select the appropriate sound input device (eg Soundflower)
- - Optional: Enable 'Jam Sync' and stop sending LTC; observe that timecode continues after signal is dropped
4. Sending Timecode from VDMX as LTC, MTC, and OSC
- Inspect the Timecode plugin
- Switch to the “Sending” tab
- - Use the + button to add 3x senders
- - - Configure senders to send MTC, LTC and OSC
- - - Use MTC, LTC and OSC test software to demonstrate received streams
- - - Tip: You can use a second Timecode plugin

### Exercises

#### Creating a multi-live input setup, VDMX as a live feed switcher
1. Create a project using several live inputs, NDI streams and Syphon sources as described above.
- For each stream, create a preview window
- Use Media Bin data-sources to switch between feeds
- Challenge: Start from the Two Channel Mixer template and create a live feed mixer 
2. Pre-vis inputs
- Use a Movie Recorder to capture short loops and images for each input
- Use photos / videos from non-connected cameras to try out other possible camera angles

#### Timecode Reference Points
1. Start from the Simple Player template or an existing project
- Add media files to Media Bin
- Add a Timecode plugin
- - Use the Timecode plugin inspector > Reference Times tab 
- - - Add several time markers
- Use the “Last ref index” data-source to automatically switch media files
- Use the other data-sources from the Timecode plugin to control playback and FX parameters
- When using LFO and Step Sequencer plugins to animate properties, try setting the quantization source to use a Timecode plugin instead of a Clock plugin
2. Optional challenge: Work with another student to sync Timecode plugins on two computers
- Pick one machine to generate and send Timecode and one machine to receive Timecode
- Which protocol (LTC, MTC) will you use? How will the data get from one machine to another?

## Lesson 2: Technical Riders and Contracts

[Handout: Technical Riders and Contracts](/handout_module_6.html)

When preparing to perform a show two of the most important documents an artist might prepare are the technical riders and contracts, which can be used to help define the working relationships with other people involved in the project.

As the name suggests, the technical rider includes the everything related to the more technical aspects of your setup, often including detailed descriptions of spacial, electrical and other requirements for a venue, wiring diagrams demonstrating how each piece of equipment should be connected, and contact information of anyone who might need to be reached for any follow up questions.

Contracts can come into play to help specify the scope of a working relationship, whether it is a collaboration or work-for-hire. As an artist you may find yourself on many different sides of contracts. In one situation, you may have a client who is paying you to do certain tasks, such as perform live at an event. In another, you may hire someone else to help with the preparation of materials. For collaborations it can often be useful to have a contract in place to clarify the responsibilities of each individual before a project begins, and specify who has future rights to continue development after the initial work has been completed.

Another detail we will look at in this lesson are the various jobs that are crucial to the lifetime of a show production beyond the artists and performers themselves. In particular, visual artists and VJs may find themselves working closely with, or assuming the role of, the lighting designer (the LD) for a show. The LD also deals with light, color, themes, feelings and time, with many of the same intentions as the video side of a performance, and there are an enumerable number of ways to use the two techniques together to reach the level of epic event production.

### Lesson Overview

* What jobs are involved in a large show production?
* What is a technical rider?
* Review of cables, adapters and other equipment.
* Client contracts.
* Working with lighting designers

* DMX and VDMX
* * Using VDMX as a DMX controlled media server
* * Sending DMX from VDMX

### Special Equipment

Required:
- DMX Equipment
- - DMX -> ArtNet device
- - ArtNet -> DMX device
- - DMX controllable light(s)
- - DMX cables

Recommended:
- 
- 

### Lecture Notes

- What jobs are involved in a large show production?
- - Artists / Performers (openers, headliners)
- - Tour & Show Managers
- - Technicians
- - Lighting designers (LDs)
- - Camera operators
- - Stage hands
- - "Runners"
- Technical rider examples and templates
- - Review of cables, adapters and other equipment
- - Considerations for different types of performance venues
- - - Clubs
- - - Arenas
- - - Festival shows
- - - Theaters
- - - Art galleries
- Contracts
- - When do you need a contract?
- - What goes in a contract?
- History of DMX / ArtNet

### Discussions

* Working with lighting designers
* * Design considerations; when can light / video elements work together, when do they work better alone?

### Demonstrations

#### Using VDMX as a DMX controlled media server

*This demonstration is similar to [the two channel DMX controlled video mixer](http://vdmx.vidvox.net/tutorials/the-two-channel-dmx-controlled-video-mixer) example.*

1. Configure VDMX Preferences:DMX and System Preferences:Network; and any other related tools for your ArtNet equipment
- If needed, open the System Preferences:Network and configure settings for the network port
- If needed, launch any software for configuring your ArtNet devices (eg the NMU tool for ENTTEC devices)
- - Use the device to set the subnet / universe
- - Set the device to input DMX (send ArtNet)
- Open VDMX Preferences:DMX
- - Select the desired ArtNet Network using the menu selection
- - - If possible, use an Ethernet based solution
- - Set the number of input ports to 1 (or higher if demonstrating multiple universes)
- - Set the subnet / universe to match the device you will be receiving from
- - - Optional: In some cases you can use the automatic setup option for inputs to configure the subnet / universe pairs for input ports
- - Close the VDMX Preferences
2. Start from the ‘Simple Mixer’ template, or an existing project file
- Optional: Add a ‘Sticky’ plugin to the project that we can use to take notes about DMX mappings
- Add sample media files (movies, etc)
- DMX can be assigned like MIDI and OSC:
- - Right click on the “Crossfader” slider and use the “Detect DMX” option
- - - Send DMX values from lighting board / test controller to create assignment
- - Use the UI Inspector to manually add receivers
- - - Address paths take the form of “/DMX/**{port number}**/**{channel number}**”
- Create consecutive DMX channel assignments for properties such as:
- - - *note that this final setup step can be skipped, instead use load the ‘DMX Video Mixer’ template for a completed setup*
- - Global:
- - - Master fade level
- - - Page selection (use UI Inspector > Nav, “Choose by Index” receiver)
- - - Crossfade
- - Individual layers:
- - - Clip Select (use Media Bin inspector > Control, “Trigger by Index” receiver)
- - - Movie Time
- - - Movie Rate (optional: limit min / max range)
- - - Movie Volume
- - - Movie inpoint (use UI Inspector, create receiver, set to “min“ instead of “val“ mode
- - - Movie outpoint (use UI Inspector, create receiver, set to “max“ instead of “val“ mode
- - - Add “Control Controls“ FX and assign contrast / saturation settings

#### Sending DMX from VDMX

*This demonstration is similar to [sending DMX from a color picker](https://vdmx.vidvox.net/tutorials/sending-dmx-values-from-a-vdmx-color-picker)*

1. Configure VDMX Preferences:DMX and System Preferences:Network; and any other related tools for your ArtNet equipment
- If needed, launch any software for configuring your ArtNet devices (eg the NMU tool for ENTTEC devices)
- - Use the device to set the subnet / universe
- - Set the device to output DMX (receive ArtNet)
- Open VDMX Preferences:DMX
- - Configure DMX sending ports
2. Sending from UI items
- Create a Control Surface plugin
- - Add a Color Wheel
- - Use UI Inspector to configure sending DMX for your demonstration fixture
- - Add any additional UI items and configure sending DMX for your demonstration fixture

### Exercises

#### Technical Riders
1. Create a flowchart that explains the audio / video / data routing for:
- Simple Player template
- Simple Mixer template
- 4 Channel Mixer template
- Your own project files
- Your home entertainment system

#### Send DMX colors
1. Use a Control Surface to send DMX values to a fixture
2. Use data-sources to control DMX sending
- Assign MIDI or OSC to sliders and buttons 
- Use a Step Sequencer plugin with a color track to sequence colors for output
- Use an LFO plugin to adjust color controls
3. Use Control Surface section presets and local UI item presets to switch between automations

#### Advanced: Media Server control of VDMX
1. Use your preferred DMX media server software along with the “DMX Video Mixer” template

## Lesson 3: Getting gig ready, Rehearsals and Performances

[Handout: Getting gig ready, Rehearsals and Performances](/handout_module_6.html)

### Lesson Overview

* Rehearsals and revisions
* Preparing a rig for travel
* Performances

* Creating backups
* * Backing up to hard drives / USB thumbdrives
* * Using GitHub for code storage
* * Online backup: Google Drive / Backblaze
* Making a packing guide
* * Travel cases
* * Gear checklists
* Being on site

* Video editing tools
* * Introduction to iMovie / ScreenFlow and basic non-linear editing
* * Creating a demo reel
* Preparing cues
* * Using the Cue List plugin in VDMX
* * Cue List import / export

### Special Equipment

Required:
- Hard drives / USB thumbdrives

Recommended:
- GitHub account
- Google Drive / CloudFlare / etc

Optional:
- Carbon Copy Cloner

### Lecture Notes

### Discussions

* Packing checklist template

### Demonstrations

#### Creating back ups
1. Backing up to hard drives / USB thumbdrives
2. GitHub
3. Online backups

#### Preparing cues
1. Adding Cues
- Start from the Simple Mixer template
- Add a Cue List plugin
- Use the default data-source to control the mixer position
- Add media files to project
- Drag media files into list of cues to create file triggers
- - Demonstrate adjusting target layer
- From the Cue List inspector
- - Add a Color data-source
- - Use the sub-inspector to directly send the color as OSC / DMX
2. Time display and sync
- Add a Timecode plugin to the project
- From the Cue List inspector in the Time section
- - Demonstrate each of the display formats:
- - - Index
- - - Beats
- - - Measures
- - - Seconds
- - - SMPTE
- Cue List can be synchronized to a Clock or Timecode plugin
- - Time signature format automatically changes to match
- - Lock to sync option disables time jumping
- - Timecode sync can be nudged forward or backwards
3. Cue import / export
- From the Options section of the Cue List, click the Export CSV button
- - Save the list of cues as a CSV – comma separate values
- Open CSV file in text editor or spreadsheet software
- CSV is easily written or modified by hand
- Change times and values in CSV file and save the file
- From the Options section of the Cue List, click the Import CSV button
- - Import the modified CSV file
- Optional: Demonstrate using Google Sheets with CSV files

### Exercises

#### Creating back ups
1. Local storage
- Get an external hard drive or USB thumbdrive with enough capacity for your video library
- Create a back up of your media files and any 3rd party plugins
- - Make sure to copy any installed resources in VDMX assets
- - Custom installed ISF (/Library/Graphics/ISF and ~/Library/Graphics/ISF)
2. Online storage
- Codeback using Git
- - Create a GitHub (or similar) account
- - Create a repository for your ISF, QC and other code compositions
- Optional: File backup with Google Drive / CloudFlare / etc
- - Create an account with an online back up service
- - Back up your media and other important files

#### Preparing cues
1. Add Cue List control to an existing project
2. Export cues as a CSV
3. Modify time values to match interesting points in a song and re-import CSV file