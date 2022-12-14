---
layout: post
title: Super Noah's Ark 3D (USA) (Source Code)
date: 2018-11-22 12:00:00
updated: 2018-11-22 12:00:00
slug: super-noahs-ark-3d-source-code
category: Documents
author: matthew_callis
thumbnail: super-noahs-ark-3d-source-code/super-noahs-ark-3d.0.png
download:
 title: Super Noah's Ark 3D (USA) (Source Code)
 filename: other/NOAH3D.zip
---

This is the source code to the _unlicensed_ [Super Noah's Ark 3D](https://superfamicom.org/info/super-noahs-ark-3d) SNES game by Wisdom Tree, known for their unlicensed NES games. The game is notably "the only commercially released SNES game in the U.S. that was not officially sanctioned by Nintendo", as well as using the same game engine for the Super Nintendo version of [Wolfenstein 3D](https://superfamicom.org/info/wolfenstein-3d-the-claw-of-eisenfaust) under license from id Software.

_Origin_

I bought this off of eBay in November of 2018 and got 4 diskettes and an official seal of authenticity (deep irony) for the disks on official Wisdom Tree letterhead. The disks were zipped using PKZIP, an old version that split it across 4 3.5 inch disks. This was a huge pain to unzip, given no modern tools support this specific format and required old software on old hardware to successfully extract. The disks were zipped sometime on of after November 13th 1994, 10:31AM, which is the latest date on any files in the disks. The original files from the diskettes are included as well as an extractable archive of the contents. All files are available on [GitHub](https://github.com/MatthewCallis/NOAH3D) as well.

_Interesting Contents_

There were a few notable items in the archives I will share below. First (not below) is the full set of tools provided by id Software to extract and repackage the contents of [Wolfenstein 3D](https://superfamicom.org/info/wolfenstein-3d-the-claw-of-eisenfaust), as well as the C source code for it.

There are several emails from [John Carmack](https://twitter.com/ID_AA_Carmack) himself as well as code he wrote for the sole purpose of cloning Wolfenstein. The sound driver was written by [John Carmack](https://twitter.com/ID_AA_Carmack) and [Rebecca Heineman](https://twitter.com/burgerbecky) credited as `Bill Heineman`. If you dig in and find more interesting items, please update on the [Super Famicom Development Wiki](https://wiki.superfamicom.org/) and TCRF [Super 3D Noah's Ark (SNES)](https://tcrf.net/Super_3D_Noah%27s_Ark_(SNES)) article.

Updates:

[Rebecca Heineman](https://twitter.com/burgerbecky/status/1065842338109448192): The sound code was originally written for [RPM Racing](https://superfamicom.org/info/rpm-racing), using the Apple IIgs Merlin assembler with macros to build for the custom [Sony SPC700 CPU](https://wiki.superfamicom.org/spc700-reference). It was improved over time for [Wolf3D](https://superfamicom.org/info/wolfenstein-3d-the-claw-of-eisenfaust).

[Rebecca Heineman](https://twitter.com/burgerbecky/status/1065846965487919104): Kewl. I found the source to my old audio tools for the SNES. At the time they were written, I had no docs to the SNES because of licensing issues with Sony. This code was created by reverse engineering the audio hardware and figuring out how it worked.

[Rebecca Heineman](https://twitter.com/burgerbecky/status/1065847211940954113): I even learned Japanese, so I could read the patents, Sony [docs on the SPC 700 CPU](https://wiki.superfamicom.org/spc700-reference) I found "elsewhere" and other bits I could gather to complete the sound driver. [Sugoi](https://www.google.com/search?q=translate+sugoi+to+english)!

[Rebecca Heineman](https://twitter.com/burgerbecky/status/1065852240626237440): I think for the xmas break, I'll get the game to compile with my current [65816](https://wiki.superfamicom.org/65816-reference) build tools.

[John Carmack](https://twitter.com/ID_AA_Carmack/status/1066155123007766529): I gave [you](https://twitter.com/burgerbecky) huge respect for learning enough Japanese back then to get through the tech docs!

```
From johnc@idcube.idsoftware.com Fri Aug 19 13:46:52 1994
Date: Thu, 18 Aug 94 20:21:29 -0600
From: John Carmack <johnc@idcube.idsoftware.com>
To: Vance Kozik <vance@crl.com>
Subject: Re: SNES snds

Ok, here is the code for the utility that generated SNES sounds (a  
tiny NeXT program).  I wrote this, but only because the original  
development plan fell apart.  I make no claim that the sound code in  
wolf is worth a damn.

John Carmack
```

```
From johnc@idcube.idsoftware.com Thu Aug 25 14:48:29 1994
Date: Wed, 24 Aug 94 19:38:27 -0600
From: John Carmack <johnc@idcube.idsoftware.com>
To: jimt@crl.com
Subject: sndlink

I think the sounds were all 22khz 16 bit samples, but it has been a  
LOOOONG time since I looked at that stuff.

I think you have the cmdlib.[ch] files from other stuff.  Here is  
sndlink.c:
```

```
printf ("sndlink 0.1 by John Carmack\n");

printf ("Sndlink (v0.1) by John Carmack\n\n");

//%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
//						   WOLFENSTEIN 3D
//						   by John Carmack
//%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

=============================================================================

							  SNESGRAB

						  by John Carmack

=============================================================================

=============================================================================

							  WALLGRAB

						  by John Carmack

=============================================================================
```

```
;--------------------------------------------------------------------
; Id's SNES sound driver - decoded from 'driver.s' provided by Id in
; an 'encoded' state (simply and each character with $7F to get in
; ASCII range - for some reason this was the ONLY file provided by
; Id that was encoded...).  It includes 'SPC700.MACS' which was not
; provided by Id but it appears to be only a macro file so the SNES
; sound chip code could be compiled by their regular 65816 assembler!
;--------------------------------------------------------------------


		LST	OFF
		TR	ON
		USE	SPC700.MACS	;Write this in SPC700
		REL

**************************************************
*
*
*  SuperFamicom Music Low Level Sound Driver     *
*
      By Bill Heineman and John Carmack          *
*
*
**************************************************

// JAPVERSION has mission pics instead if briefing

//#define	JAPVERSION


// If PALCHECK is defined, aborts on NTSC version, else abort on PAL

//#define	PALCHECK
```

Assets and other files all seem in place, as well as some tools I was not able to find anything for online, which I believe could be the iD assembler mentioned in the file above as `regular 65816 assembler`:

```
MSD RomEm(R)-PLUS Interactive Control Program --
Copyright (C) 1988-1993,
Microsystems Development, San Jose, California, USA,
ALL RIGHTS RESERVED --
Copyright (C) 1988-1993,
John Golini, Los Gatos, California, USA,
ALL RIGHTS RESERVED
```

```
***************************************
 **   Zardoz 65C816 Macro Assembler   **
 **                                   **
 **     Version%s- %s    **
 ***************************************

    2.0h  Aug 11 1994 
2.0h  Aug 11 1994 04:58:09        Copyright (C) 1992,1993 by Zardoz Software, Inc.
```

_Screenshots_

![Screenshot](https://snes.in/screenshots/super-noahs-ark-3d/super-noahs-ark-3d.0.png)
![Screenshot](https://snes.in/screenshots/super-noahs-ark-3d/super-noahs-ark-3d.1.png)
![Screenshot](https://snes.in/screenshots/super-noahs-ark-3d/super-noahs-ark-3d.2.png)
![Screenshot](https://snes.in/screenshots/super-noahs-ark-3d/super-noahs-ark-3d.3.png)
