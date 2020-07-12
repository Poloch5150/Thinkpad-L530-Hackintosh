# Thinkpad-L530-Hackintosh

The purpose of this guide is to help people installing MacOS on a Thinkpad L530.
This current EFI works like a charm with MacOS Mojave 10.14.6
I haven't tried catalina yet. It was working fine with both Sierra and High Sierra back in the day but i cant confirm if it is still working on previous versions of MacOS. If you want to try other versions, update me if it works ! 


I figured out most things by toying with clover bootloader and reading guides. With the latest revisions of the clover bootloader, the process got easier : it no longer needs a custom dsdt for custom brightness range + an injector kext (thanks to whatevergreen), battery etc. 
I've been alone with this laptop running MacOS for years, desperatly looking for help. But people only seemed to care for the t430 and the x230 at the time.
Now that it works fine, I guess it is time to share my work !


Most of what i did to fine tune the laptop was about 2 years ago and I just updated my kexts and bootloader since then. 
I'm not sure I could do everything again from scratch but I do a lots of backups of my files so I don't have to figure this out again. :)
Some basic knowledge about hackintosh is needed to do this. Find out for yourselves, I'm not clever enough to do a beginner guide.


Note also that there are several revisions of this model. Mine is 2475A38 (first model, june 2012), bios rev 2.70.
Some guys with newer L530 flavours got it to work, but I can't garantee my files will work with your L530.


# MY SPECS :
HM76 Chipset
I7 3632qm
2x8gb DDR3 Corsair Vengeance 1600mhz
Samsung EVO 840 ssd
1366x768 shitty screen
9-cells battery 
Docking station 4337 (only the audio jack won't work on it, but I'm using a Focusrite Scarlett 2i2 when docked)


Note that most Intel core cpu will work, but if you have the celeron model, you'l have to toss this (bad) cpu since it isn't supported by MacOS.
but I suggest getting an i7, the 3520m for example if you are low on money (dual core, 2,9ghz)

I even tried a 3630qm (45w tdp cpu for a 35w tdp laptop). It was overheating, but I'm sure that it could be fine with some thermal grizzly paste.
The 3632qm is the best CPU you can get with the right tdp for this laptop.


# BIOS SETTINGS (These are mine, maybe some of them are pointless - always on usb, power on AC etc were bothering sleep at the time)
Always On USB : disable
Express Card Speed : Automatic 
Power on with AC attach : Disabled
Intel Rapid Start technology : Disabled
Sata controller mode : AHCI
Security Chip : Disabled
Execution prevention : Enabled
Intel Virtualization technology : Enabled (I you are running VM on top of MacOS)
Secure Boot : disabled

Boot Mode : UEFI only, CSM disabled


# Creating a MacOS installer 
Use the method you want to get macOS. To me, the easiest way is to get an Olarila Image, burn it to an usb drive using etcher and then replacing the content of the EFI partition 




