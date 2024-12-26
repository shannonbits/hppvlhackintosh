# Hackintosh HP Pavilion Notebook InsydeH20
My HP Pavilion Notebook Hackintosh and, how i did it.

Disclaimers:
(Im Turkish and Most of the guides that are used in this repo is in Turkish. The repo may have some wrong words used, try using a translator if you don't understand anything.)

I will use macOS X Monterey on this guide, the things i use might not work on other versions.

Im gonna try to make this guide the easiest guide there is on the internet.

Please write something to me or this repo if you didn't get something, I will appricate it!

Im not a Professional, I learned by trying to fix my own mistakes. I can't do anything if your Computer can't run MacOS.
------------------------------------------------------------------------------------------------------------------------------------------
FAQ'S

-What is a Hackintosh?
* A Hackintosh is a PC That has an Intel CPU (Mostly), that you installed macOS into. This Guide will show you how to make a Hackintosh using my Old Hp Pavilion Notebook as an example.

-Which Intel CPU's are supported?
* See if your CPU is supported in this article: https://hackintoshenglish.fandom.com/wiki/CPU_Compatibility .

-What will i (shannon) use in this guide?
*Im gonna use my old HP Pavilion Notebook InsydeH20, It has an Intel i7-4500U CPU, which is considered Haswell CPU. I will link all of the guides to get your computer up and running, and the things i used like my config.plist (config file).

-The things that are working on my own Hackintosh:

![Ekran Resmi 2024-12-26 16 54 47](https://github.com/user-attachments/assets/afc8756d-cd00-401d-8315-84d8540fcddc)

Working things:
* Graphics Card
* USB Ports
* Sound - Microphone
* Trackpad and Keyboard
* iCloud and Apple ID
* Wifi (mine is a usb adaptor)
* Siri

Not working things:
* HDMI (didn't patch yet, will update the guide if i patch it)
* Bluetooth (didn't try yet, might work)
* Other things i didn't check yet (None, i think)
  
------------------------------------------------------------------------------------------------------------------------------------------

Guide Part(s):

Flashing Our MacOS Image onto the USB (Part One)
------------------------------------------------------------------------------------------------------------------------------------------

Let's Get Started!

I Used a lot of websites but mostly a website named OSXINFO (https://osxinfo.net/), which is the best Hackintosh Website that i could find on turkish internet. There are a lot of guides on OSXINFO, check them if you know turkish!

Of Course, I didn't know what to do when i first started Hackintoshing, I used yusufklncc's Guide (https://osxinfo.net/konu/rehber-opencore-ile-adim-adim-macos-kurulumu.23648/#) on OSXINFO. 

First, you need to download the macOS X image, as i said im gonna use monterey. But, you can use any version you like.
Open this link: https://osxinfo.net/konu/macos-monterey-intel-ve-amd-kurulum-imaji.24330/ , then click this

![Ekran Resmi 2024-12-26 19 15 55](https://github.com/user-attachments/assets/a18ab901-fdc3-48a5-a0a4-20a5b06e3c90)

Once you download the image, you need to use an software called Balena Etcher (https://www.balena.io/etcher&ved=2ahUKEwjej9y068WKAxXu8DQHHSZuAPIQFnoECAoQAQ&usg=AOvVaw0UNPm_qcksmQ1aL8D-5gLD)

After you download Etcher, open the software select the .raw file we downloaded (our image of macOS Monterey). Selcet your USB (it should be atleast 32 or 16 GB) and click the big green flash button! what this will do is flash the .raw file we downloaded onto the usb.

After Flashing is finished, go into your bios settings and change some things up, for me i only needed to close secure boot off. But, i will tell you the things that you need to change if you have those settings:


    Intel BIOS Settings:
        Before starting load default settings in the BIOS
        Disable
            Fast Boot
            Secure Boot
            VT-d
            Serial/COM Port
            Parallel Port
            CSM
            Thunderbolt
            Intel SGX
            Intel Platform Trust
        Enable
            VT-x
            Above 4G decoding
            Hyper-Threading
            Execute Disable Bit
            EHCI/XHCI Hand-off
            OS type: Windows 8.1/10 UEFI Mode
            DVMT Pre-Allocated(iGPU Memory): 64MB
            SATA Mode: AHCI

            In this guide, im not gonna show how to make a Hackintosh with AMD CPU's but you can find how to do it on the internet.

After you finished changing these settings in the bios, reboot into Windows if you want to save some files or things on the hardrive because we are gonna reset the hardrive in the macOS Setup.

Once you are done, reboot into BIOS And select the normal boot device as the usb and reboot.

macOS Installation (Part Two)
------------------------------------------------------------------------------------------------------------------------------------------

Once you rebooted. it needs to show you the Opencore Select Screen, select Install MacOS Monterey (or the version you downloaded).
It should take you to the macOS Recovery screen.

Select Disk Utility

![image](https://github.com/user-attachments/assets/e1d332ce-3c24-4cd4-bdaa-e25b4c52989e)

then select show all volumes.

![image](https://github.com/user-attachments/assets/73dbc6ce-ee26-44c3-817f-c9ba7321f043)

Select your hardrive, and erase it as APFS And GUID Partition Map. THIS WILL ERASE THE HARDRIVE AND YOUR DATA.

![image](https://github.com/user-attachments/assets/ee9c9847-bf79-408a-9df3-66a7d64d1497)

after erasing your hardrive, select Install macOS Monterey. Select basic things as agreeing the tos, and select your hardrive (or the disk you want to install macOS on)








