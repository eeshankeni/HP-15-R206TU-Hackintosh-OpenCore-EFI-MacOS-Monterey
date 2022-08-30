# HP 15 R206TU Hackintosh OpenCore EFI for MacOS Monterey

## Specs:

Intel Core i3 5010U (Broadwell)  
Intel HD 5500  
Realtek rtl8111h  
Synaptic PS2 Touchpad  
4GB Ram

## What works?

Power Management  
Battery Indicator  
Brightness  
Ethernet  
All USB ports  
Secure Boot and SIP  
SSDT-HPET.aml compiled with SSDTtime on Windows


## What does not work?
Onboard Wifi and BT (Typical for any hackintosh). I use Tp link TL-WN722N with [these drivers](https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter)

Audio (I have already added Realtek driver kexts so possibly [playing around with ALC-ID](https://dortania.github.io/OpenCore-Post-Install/universal/audio.html) can fix this problem)

Touchpad buttons. (This ones weird af, the trackpad itself works great with voodoo PS2 drivers but the buttons do not). The trackpad is indeed a Synaptic one based on the drivers found on the HP website and windows device manager claims its a PS2 one. 
Alternatively trying Voodoo RMI drivers also did not fix the issue, in fact the touchpad stopped respoding alltogether.

## Special Instructions
I have noticed that after the installer first reboots, opencore efi keeps looping before the picker even shows up. A workaround for this is to create a second opencore efi recovery usb. And use that to enter the macOS installer which has been made by the first usb installer on your hard disk. This installer was copied to your hard disk before it rebooted for the first time. So you should be able to see it when the picker eventually opens up. Post this point, there should be an apple logo with 'xx time remaining' text and a progress bar.

This is only necessary once, subsequent boots do not need this second usb and everything works great with the first usb alone. Some weird shit man seriously!  

After that you can use mountEFI to copy the usb EFI to your hard disk EFI parition. Use [this guide](https://dortania.github.io/OpenCore-Post-Install/universal/oc2hdd.html). 


## All in all,  
This build is sufficient for devs like me who want to use this budget laptop for building iOS apps. But I would not recommend this as a daily driver by any means. 


![photo](https://github.com/eeshankeni/HP-15-R206TU-Hackintosh-OpenCore-EFI-MacOS-Monterey/blob/main/image.jpg?raw=true)





