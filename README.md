# 1987-1988 Pontiac Fiero OEM Drop-In Headlight Motor Controller
**PCB Designed by Ryan Blanchard 4.2024**\
**Based On A Project by WalkerTexan**\
**FOR NON-COMMERCIAL USE ONLY.**

![IMG_1802](https://github.com/gekko3622/Fiero-Drop-In-Headlight-Module/assets/166318874/6a2a40ab-9132-47d7-b57b-6cc2eff3ec69)


**Important:** Please pay attention to the Bill of Materials (BOM). Some components have been changed from my previous designs.\
**This PCB MUST be fabricated with 2 Oz Outer Copper Weight for power handling and safety.**

## Intro

This is a PCB implementation of WalkerTexan's "Fiero Headlight Controller" project.\
I started this project after getting frustrated with the cost and questionable reliability of used modules.\
While there are new reproductions of the original module available, I found the cost to be too high.

After publishing my original PCB implementation, I was challenged to make it fit inside the original GM module's housing. Here it is.

## Repository Contents

**1. Arduino Program**
- WalkerTexan's code for the Arduino Nano.\
This MUST be programmed onto the Pro Micro for the module to function.

**2. Gerber Files (For Production)**
- These are the files that must be provided to a fabricator to produce a PCB.\
  **VERY IMPORTANT:** This PCB MUST be produced with 2 Oz outer copper weight in order to meet power handling requirements.\
  The provided gerber files will produce an identical copy of the PCB installed in my own car, just minus my logo.

  The Zip file can be directly submitted to a fabricator and contains all of the other individual files in this folder.

**3. KiCad Project Files**
- These are my full design schematic and PCB layout files. Use them for learning PCB design or to create your own custom version of the module.

  This project requires KiCad v8 or higher.


## Requirements
This project requires that you already have a fried 87-88 headlight module. (You're considering this project for a reason, right?)\
A Firebird or Corvette module of similar design can also be used.

- You will need to desolder and re-use the original 4 and 5 pin headers from your original module.
- The original module case will also be reused, but requires a single modification.

## Important Building Tips

**1. Arduino Pro Micro**

Due to the low clearance of the GM module casing, the Pro Micro must be installed lower on its pins than standard.\
It is also installed in a DIP socket to further reduce the mounting height.

My recommendation is to install the DIP socket first, then push the Pro Micro's pins into it.\
While installed, push down the plastic spacer, moving side to side until it's as flush as possible with the socket.

![IMG_1767](https://github.com/gekko3622/Fiero-Drop-In-Headlight-Module/assets/166318874/9c42af81-7d07-4925-a20f-a141f330f416)

You can really see the difference in this side-by-side:

![IMG_1769](https://github.com/gekko3622/Fiero-Drop-In-Headlight-Module/assets/166318874/6352d428-33bd-4b9d-b7db-ef6ef3529aa6)

Once you've adjusted the pins for each side, place the Pro Micro onto the pins and solder it while socketed.

**2. Fuses**

I designed the module to directly solder in standard automotive mini fuses.\
For my own board, I used low profile mini fuses in order to avoid having to trim the fuse legs.

Regular mini fuses will work fine, just trim the legs after soldering.
  - 15 amps should be fine assuming your motors are in good shape.

![IMG_1806](https://github.com/gekko3622/Fiero-Drop-In-Headlight-Module/assets/166318874/958543e4-5b49-4b0c-9f4d-40e1c9081fc3)

**3. 4/5 Pin Original Header Pins**

The header pins must be installed slightly pulled out from the board to compensate for the added height of the relays.\
I tried my best to capture an image to demonstrate the needed spacing, but it's hard get a clear shot when assembled.

![IMG_1804](https://github.com/gekko3622/Fiero-Drop-In-Headlight-Module/assets/166318874/a144d649-118f-4b21-89da-a9fdd36cd9ea)

I found it easiest to install the pins one side at a time, getting them lined up right when installed into the housing.\
The holes for the headers are a pretty tight fit, so you should be able to position them fairly easily without them falling out.\
Once I was satisfied with the fitment, I lightly soldered a pin or two per side while still in the casing just to make sure the alignment was right.

**4. Modifying the Module Case**

The sole casing modification needed is to remove most of the plastic spacers from the back panel.\
The plastic is pretty soft, so I was able to grab and twist with vice grips to remove most of the material.

**You do not need to fully remove the spacers, just enough so the back panel can be re-installed without flexing.**\
**The round corner pieces do not need to be removed.**

Here's a comparison of an intact panel and my hastily trimmed panel. If you have the time, sanding them would give a more precise fit.

![image0(2)](https://github.com/gekko3622/Fiero-Drop-In-Headlight-Module/assets/166318874/f6a0df4b-b3ae-47fe-999a-014b6f4d32a0)




## Modifications to Original Source
1. Recreated the schematic diagram in KiCad.
2. Designed a PCB based on the schematic.
3. Added fuses and changed the power-on circuit to draw its power from the second 12V source.
4. Substituted the relays for a smaller part with higher current rating.
5. Adapted for compatibility with the original headlight module.

## Credits
The electrical schematic and Arduino code this project is based on were created by WalkerTexan.\
See his original project here: https://www.hackster.io/walkertexan/fiero-headlight-controller-8eaa4c

KiCad Schematic and PCB Layout/Design by Ryan Blanchard.

## License
This project is published under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International license.\
Use of this project for commercial purposes is prohibited.

For full details, see the license file.
