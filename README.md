[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
<br>

 <img src="Pictures/IMG_9009.jpeg" width="500px"><BR><BR>
 <img src="Pictures/IMG_9010.jpeg" width="500px"><BR><BR>


# Grappler Minus

The Grappler Plus was originally a printer interface card, but in recent years no one wanted to use it. However, after Wing Yeung came up with the idea of a repurposed ROM, Grappler Plus' popularity resurfaced.<BR>
Grappler Minus is a clone of Grappler Plus without printer interface functionality. This card does not function on its own. Used in conjunction with Apple's genuine DiskII controller card. It is a card that acts like an interpreter, changing the DiskII controller card to support Smartport like the Liron card.<BR><BR>

The reason for developing this... I didn't know the structure of Grappler Plus in the early stages, so I turned my attention to Brad Bell 's clone project on the GitHub. I also asked Brad if he would allow me to redesign the Grappler Plus PCB by removing the interface for this purpose. He was kind and allowed it, and I forked from his repository.<br><br>

 <img src="Pictures/IMG_8986.jpeg" width="500px"><BR><BR>

Our SPIISD worked fine with Grappler Plus on SoftSP DIY V2 and V3, but Apple IIplus would never boot with any ROM Rev. Also, since Grappler Plus has a useless circuit because it is a printer interface, so they are electrically interfering and delaying Lyle's timing. And by removing these extra circuits, the timing of the 10 smart port redirects may be improved.<br><br>

In our testing, [SPIISD](https://github.com/kerokero5150/SP2SD_DIY_KIT) and Grappler Minus worked on the Apple IIPlus, which had never worked before! Of course it works like a feather on Apple IIe as well.

### Advantages of Grappler Minus

- Not as difficult to obtain as Grappler Plus, anyone can create it for themselves for free!
- In the last version, all parts have been changed to DIP parts, so soldering is not difficult even for enthusiasts.
- You can try out Smartport without a Liron card. Your investment is minimal.

## SoftSP DIY 

This card is designed to use "SoftSP DIY" ROM.
SoftSP DIY is a product of Wing Yeung, MFA2 WorkShop(Aka.KbooHK) and used with permission.
http://www.mfa2lab.com

<BR><BR>

Latest ROM version is [V6-a](SoftSP-ROMs/softsp-DIY-v6-a.bin), improved timing and different disk slot code can be generated from the utility program.<BR><BR>



Chris Torrence 's store CT6502 sells SoftSP. I recommend this if you want a complete SoftSP:
https://ct6502.org/product/softsp/


## Gerber files

Feb 24 2024, Updated PCB files. Includes router error fixes, please check this [V.1.4b](Gerber_GH_DIY_1.4b) <BR><BR>
You can use it by compressing this [Gerber](GERBER_GH_DIY) folder and uploading it to JLCPCB as it is.



## Assemble and BOM

### BOM
Location, Parts Number<BR>
U1 74LS00<BR>
U2 74LS279<BR>
U3 74LS02<BR>
U4 74LS08<BR>
U5 74LS30<BR>
U6 EPROM 2732 or 2764 (*SoftSP DIY ROM flashes to this EPROM.)<BR>
C1, C2, C3, C4 100nF multilayer ceramic capacitor<BR>
C5 470pF multilayer ceramic capacitor<BR>
C6, C7 100pF multilayer ceramic capacitor<BR><BR>
Option: 14pin IC socket x4, 16pin IC socket x1, 24pin or 28pin IC socket(wide)<BR><BR>
If you want to use ICs such as 74HCXX that are not CMOS, they will probably work fine, but they are fast but leaky and should be handled with care. Please try at your own risk.

### ROMS

Wing Yeung has created a new V6-a ROM for SoftSP DIY. After we created the Grappler Minus card, he let us try it out right away. The [ROMs](https://github.com/kerokero5150/GrapplerMinus/tree/main/SoftSP-ROMs) that we have confirmed to work are SoftSP DIY ROM V2, V3 and V6-a. 


## Supported computers

Apple IIPlus, Apple IIe
*Apple ///: Possibly bootable if supported onboard ROM.

## Suported Devices

- SPIISD<BR><BR>
- wDrive<BR><BR>
*We do not support BMOW's FloppyEMU. Please read the Known issues below for the reason.

## Known issues

This is designed to work with our product SPIISD, Please note the following points:<BR>
- In the Rev V.1.3, It is known that the Grappler Minus card does not work with MFA2 WorkShop's WDrive due to timing issues. This is because there was a router error in one place, but it can be easily fixed. In addition, it works normally with SPIISD. This has been fixed in [V.1.4](Gerber_GH_DIY_1.4b)<BR>
This issue was solved by Wing Yeung, plx see my [blog](https://ameblo.jp/keroxiee1016/entry-12838344596.html)<BR><BR>
- When using BMOW's Floppy EMU, there is an inflow of 12Pin +5V, which will fry the FloppyEMU's CPLD chip XC9572XL-10VQG44. To prevent this, it is necessary to cut pin 12, but this is not recommended as there are still many accidents. Please do everything at your own risk. <BR>


## Available for purchase now
<img src="Pictures/sc-keros-store.png" width="300px"><BR><BR>
You can buy it in [our store](https://en.infinityproducts.co.jp/shop-1). Bare PCB and complete finished product.<BR><BR>
Kero's Mac Mods store is currently selling revision V1.5b. The difference between V1.5 and V1.4 is whether 74LS02 is present or not, but this will not be uploaded to GitHub for a while. Because the cloner is listing it on eBay.


## License
Grappler Minus is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). Your personal use is permitted, but not for sale.<BR><BR>
The copyright and handling of "SoftSP DIY" is subject to the [MFA2 WorkShop](http://www.mfa2lab.com) license. used with permission.

## Special Thanks

I would like to express many thanks to the following our friends. They helped with this project:

Wing Yeung, MFA2 WorkShop(Aka.KbooHK)<BR>
Chris Torrence, Assembly Lines<BR>
Bradly Bell (Aka. BTB)<BR>
Petar Puskarich <BR>











