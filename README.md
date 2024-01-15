[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
<br>

 <img src="Pictures/IMG_9009.jpeg" width="500px"><BR><BR>
 <img src="Pictures/IMG_9010.jpeg" width="500px"><BR><BR>


# Grappler Minus

I didn't know the structure of Grappler Plus in the early stages, so I turned my attention to Brad Bell 's clone project on the GitHub. I also asked Brad if he would allow me to redesign the Grappler Plus PCB by removing the interface for this purpose. He was kind and allowed it,and fork from his repository.<br><br>

 <img src="Pictures/IMG_8986.jpeg" width="500px"><BR><BR>

Our SPIISD worked fine with Grapplerplus on SoftSP, but IIplus would never boot. Also, since Grapplerplus has a useless circuit because it is a printer interface, so they are electrically interfering and delaying Lyle's timing. And by removing these extra circuits, the timing of the 10 smart port redirects may be improved.<br><br>

In our testing, [SPIISD](https://github.com/kerokero5150/SP2SD_DIY_KIT) and GrapplerMinus worked on the Apple IIPlus, which had never worked before! Of course it works like a feather on IIe as well.

## SoftSP DIY 

This card is designed to use "SoftSP DIY" ROM.
SoftSP DIY is a product of Wing Yeung, MFA2 WorkShop(Aka.KbooHK) and used with permission.
http://www.mfa2lab.com

Chris Torrence 's store CT6502 sells SoftSP. I recommend this if you want a complete SoftSP:
https://ct6502.org/product/softsp/


## Gerber files

You can use it by compressing this [Gerber](GERBER_GH_DIY) folder and uploading it to JLCPCB as it is.

## Assemble and BOM

### BOM
Location, Parts Number<BR>
U1 74LS00<BR>
U2 74LS279<BR>
U3 74LS02<BR>
U4 74LS08<BR>
U5 74LS30<BR>
U6 EPROM 2732 or 2764<BR>
C1, C2, C3, C4 100nF multilayer ceramic capacitor<BR>
C5 470pF multilayer ceramic capacitor<BR>
C6, C7 100pF multilayer ceramic capacitor<BR><BR>
Option: 14pin IC socket x4, 16pin IC socket x1, 24pin or 28pin IC socket(wide)<BR><BR>
If you want to use ICs such as 74HCXX that are not CMOS, they will probably work fine, but they are fast but leaky and should be handled with care. Please try at your own risk.

### ROMS

Wing Yeung has created a new V6-a ROM for SoftSP DIY. After we created the Grappler Minus card, he let us try it out right away. The [ROMs](https://github.com/kerokero5150/GrapplerMinus/tree/main/SoftSP-ROMs) that we have confirmed to work are SoftSP　DIY　ROM Rev. V2, V3 and V6-a.


## Supported conputers

Apple IIPlus, Apple IIe
*Apple ///: Possibly bootable if supported onboard ROM.

## Available for purchase now
<img src="Pictures/sc-keros-store.png" width="300px"><BR><BR>
You can buy it in [our store](https://en.infinityproducts.co.jp/shop-1). Bare PCB and complete finished product.


## License
Grappler Minus is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). Your personal use is permitted, but not for sale.<BR><BR>
The copyright and handling of "SoftSP DIY" is subject to the [MFA2 WorkShop](http://www.mfa2lab.com) license. used with permission.









