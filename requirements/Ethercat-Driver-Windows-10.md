
 
should work that way... on Intel driver you need really a reboot (with switching off the pc) because of the CODESYS nic driver..  
please do this and try it again... it should from my point of view work.  
After reboot please check the plc logger.... (scan the ethercat net work with rightclick on the master in the device tree and then check the plc logger)  
BR  
Edwin
 
Hi,   
i created a new project and scanned with the master for slaves. He detected them without problems and i was able to add them to my device tree. as you can see in the picture i added all the checkmarks in the PDO configuration.
 
**Download ✓ [https://eninlili.blogspot.com/?file=2A0OZe](https://eninlili.blogspot.com/?file=2A0OZe)**


 
Hi,  
did you check your RTE realtime capabilities?  
If you are online with CODESYS in the Task configuration you see this jitter measurements.  
Is this in a good shape? (Usually you should see 30-40us jitter on the Ethercat/MotionTask after doing a reset by righclick on this line)
 
I just recognized that, - as you can see in the picture at the top- codesys says, that the Ethercat is running, but in the online configuration interface of the motor control there is displayed : "No Sync" and distributed Clocks is not running:
 
First of all I am sorry if this is not the right forum for this question but I was not sure where to ask.
I am currently running Dewesoft X 2024.1 on Windows 11 emulated via Parallels on an M1 Pro MacBook Pro. The software installed without any warning and runs smoothly (I can do data analysis and use all functions without any issue). The only big problem I have is that I am not able to connect any DAQ to it. It just does not seen any device connected. Keep in mind that all needed options (so adapter passthrough and network sharing) are enabled in the virtual machine settings.
I know that Dewesoft X does not natively support emulation but it seems weird that everything works fine but I can't connect to the DAQ. Do you have any idea why this might be? What could I try? Thanks in advance
 
The 2nd step when it comes to EtherCAT devices are not recognized manual is supposedly slightly different for paralleled systems. There, you should go to USB 10/100/1000 LAN settings, under "hardware" and change the "Automatic" configuration to "Manual". Then, set the speed to Base 1000baseT, Full Duplex, and Standard MTU. Press "OK" and then see if the Iolite is seen by Dewesoft.

It appears Ethercat DAQ Filter is not installed on the virtual machine. When trying to install I get the following. It may be due to the fact that windows ARM is running and translation to x64 is used.
 
It looks like this is an issue with the computer/virtual machine not being able to install the drivers, so there is not much we can do from Dewesoft's point of view. We also do not have much experience when it comes to using Parallels, so it is rather difficult to give you any concrete advice.
 
Since you are installing the drivers as a separate component, I would suggest you check out our solution: Manual EtherCAT DAQ driver installation, and try to re-install the drivers from our webpage. Please do note that you should uninstall the previously installed EtherCAT DAQ drivers before installing the new drivers.
 
We did have a client that has successfully resolved the error code: 0x0 issue, however, they were using a Windows computer, not a virtual machine, so I am not sure if any of their troubleshooting will help in your case. -> The client was running Windows 11 Pro with Microsoft 2013 C++ Redistributable installed.
 
The acontis ECAT Protocol Driver is needed to use the NDIS Link Layer and can be installed from Bin/Windows/x64/EcatNdisSetup-x86\_64Bit.msi or Bin/Windows/x86/EcatNdisSetup-x86\_32Bit.msi respectively depend on the Windows Operating System Type of 64 Bit or 32 Bit.
 
In case of problems while using the Link layer, it is advised to set the windows registry entry DontSetPromiscuousMode of the ECAT NDIS Protocol driver. This option is available since V3.1.3.02 of the driver.This can be done through the following steps:
 
I have created 2 Hyper V machine running windows 11 and Twincat .29, i have then created a NIC on both the virtual PCs. to run Ethercat, and installed beckohff RT driver on it.All that works.The NIC dont have any connection to the hardware NIC, all is virtualise.
 
hello,
At the moment I have a NUC, I work with EtherCAT and I have problem to run in full speed with the NUC, I was checking the in 
 =../content/1033/tcsystemmanager/reference/ethercat/html/ethercat\_supnetworkcontroller.htm&id=18955
where describe the Supported Network Controller by Beckhoff Ethernet Driver, I have a desktop PC with one the Ethernet Controllers (Vendor ID: 0x8086) listed in that web and I dont have problem to run in full speed, so I am planning to buy a new laptop and I can not find the correct one that have a compatible Ethernet controller integrated that is supported and listed in the beckhoff web side.
Any sugestion about how to find the correct laptop ?


 
On this forum, we can provide recommendations about the behavior your Intel NUC is experiencing at this moment. For questions about Intel Ethernet Controllers and their specifications, we can move this thread to the appropriate forum. Please let us know if you would like this thread to be moved.
 
The list of network adapters from that link are very old and deprecated at this point. It appears as though the vendor for the software needs to update their network adapter driver allowed list. My recommendation is to reach out to the software vendor directly and request for the adapter list to be updated.
 
I do not have specific request of brand of laptop, I am researching to buy the correct one that will work well with EtherCAT... About the old pc that I have I can not provide that information, because I dont have that computer anymore.


 
Looking at the link you provided, I can see that 82579V and 82579LM are on the list. These two Ethernet Controllers are still on the market. You may consider double checking with Beckhoff if it will work well with EtherCAT. Once done, you may now contact laptop manufacturers and check with them the list of laptops that has an Ethernet Controller mentioned above.
 
Please be informed that we will now close this request since we haven't received any response from our previous follow ups. If you need any additional information, please submit a new question as this thread will no longer being monitored
 
Intel does not verify all solutions, including but not limited to any file transfers that may appear in this community. Accordingly, Intel disclaims all express and implied warranties, including without limitation, the implied warranties of merchantability, fitness for a particular purpose, and non-infringement, as well as any warranty arising from course of performance, course of dealing, or usage in trade.
 
The next step is to find out which Library is best suited to be used to developed the LabView functions. If there is a better library for this task or have you have already done something like this free to reply.
 
If you would have used a LabVIEW Realtime controller you could have used the NI Industrial Communication for EtherCAT driver. It does have a learning curve for sure, but I have used it in the past successfully.
 
If you use other libraries you will have to make sure that it is 64-bit compiled in order to interface it through the LabVIEW Call Library Node. LabVIEW for Linux is since 2016 only available as 64 bit version.
 
The NI Industrial Communication for EtherCAT driver is only supported for windows. I will look for other possibilities. Maybe somebody have already tried to interface a Ethercat dll before and i can get some good suggestions.
 
I believe OPC UA is it. We run TwinCAT OPC UA on each PLC. You can also use one TwinCAT OPC UA installation to handle OPC UA for all TwinCAT PLCs at a location, though if that goes down it takes all lines down instead of one.
 
A promise based client implementation of the TwinCAT AMS and ADS protocols from Beckhoff. - GitHub - stamp/beckhoff-js: A promise based client implementation of the TwinCAT AMS and ADS protocols fr...
 
We currently use TwinCAT OPC UA to interface between the PLC and Ignition on our Beckhoff IPCs. A communications driver would be great though. Beckhoff is quickly gaining momentum in the automation sphere and we have found out (via some costly R&D) that Alan Bradley or Modicons IPC/PLCs cant perform even close to what Beckhoffs IPCs can.
 
Meh. Rockwell had (has?) a product called SoftLogix that applied the same "PLC in Windows" technology that Beckhoff pushes. It ran rings around Rockwell's flagship hardware. But you don't see it around because nobody in their right mind trusts critical 24/7/365 processes to Windows, however hardened it may be. IMNSHO.
 
I recommend you learn to partition your applications into the parts that need to go fast and the parts that need to be reliable. Make your process tolerate reboots of the former. (I count SCADA in the former.)
 
+1, I don't normally even have a continuous task anymore. It's all periodic or event driven and code placed strategically for best performance. I'd still like his take as I've heard this more than once... but, I don't see the issue.
 
I used a AB CP5380, maxed out with options. It ran slower than a Raspberry Pi 4 8G. It appears that the AB CP5380 is a modified BeagleBone that is able to run Windows but not Ignition as well as other systems.
 
In a personal performance test that I conducted on my own, the RPI was able to process around 67000+ tags to a tag historian in Ignition Edge, no problem. Where the RPI lacked was in dynamic creation of instances but quickly caught back up. The AB system had issues with dynamic creation of instances probably because of hardware limitations. It just couldnt ke