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

Touchpad buttons and tap gesture (This ones weird af, the trackpad itself works great with voodoo PS2 drivers but the buttons and tapping click does not). The trackpad is indeed a Synaptic one based on the drivers found on the HP website and windows device manager claims its a PS2 one. 
Alternatively trying Voodoo RMI drivers also did not fix the issue, in fact the touchpad stopped respoding alltogether.

## All in all,  
This build is sufficient for devs like me who want to use this budget laptop for building iOS apps. But I would not recommend this as a daily driver by any means. 


![photo](https://github.com/eeshankeni/HP-15-R206TU-Hackintosh-OpenCore-EFI-MacOS-Monterey/blob/main/image.jpg?raw=true)





