 ■ DOOFUS --- MS DOS PLATFORM GAME MODIFICATION PROJECT (Borland C++ & x86 Assembler)

Doofus is a high-quality platform game with stunning graphics & beautiful musics .. a masterpiece made for MS-DOS.<br>
Doofus uses **Adlib music files in TBS format, all the game's music/soundtrack is included in the tbsaplay.zip package**

<img width="1390" height="1316" alt="doofus4" src="https://github.com/user-attachments/assets/2ad47249-3f71-4b7a-8b93-4cc5249e7f9a" />


_________________________________________________________________________________________________________________________________________________________________________________

**(1)** - DOOFUS GAME "gamedata.g-d" EXTERNAL ARCHIVE FILE EXTRACTOR + REASSEMBLER(Combiner) = Unpacker/Packer --- Doofext.exe 

■  **Doofext.exe** (%100 Full working version)

I wanted to contribute to the modification of Doofus game by making some small additions, 

The game's main executable file is compressed/protected with PKLite. 
After unpacking it, the executable file becomes fully open to reverse engineering, and the real work begins from this point. 
As a first step, I started by writing a small tool that opens the game's external data archive file "gamedata.g-d," and this is complete. 
Now, unlike previous reverse engineering attempts, there's no need for a Java-based program. 
Using the MS-DOS command-line `doofext.exe`, 
all files in the "gamedata.g-d" image data archive can be easily (1) unpacked into the "\GD" folder, and then 
(2) reassembled(pack) to re-create the "gamedata.g-d" file. 

Doofext.exe (Doofus gamedata.g-d asset deployment subsystem) 

  ~ usage syntax options:
  
doofext -x     : eXtracts gamedata.g-d target entities into local \GD\ folder = UNPACK
  
doofext -c     : reCombines(reassembles) \GD\ folder contents dynamically back into archive = PACK
  
doofext -as    : displays original hardcoded file sizes matrix parameters (file name lister)  *** use this: doofext -as>log.txt

_________________________________________________________________________________________________________________________________________________________________________________

**(2)** - DOOFUS GAME GB-IMAGE-FILES(*_3f2.DAT) VIEWER --- GBview.exe 1.5h *UPDATED* 

■  **GBview.exe** (%100 Full working version)

0004_3f2.dat = Company Logo image (Prestige Softwareentwicklung GmbH logo)

0005_3f2.dat = Game Logo image (Doofus game logo)

0006_3f2.dat = Doofus boy dog monkey elephant image

0008_3f2.dat = HighScore image

0018_48b.dat = The market and the picture of the man that appear at the end of the level

0062_3f2.dat = Gameover image

0063_3f2.dat = End game "welldone" screen

0064_3f6.dat = Congratulations at the end of the game screen


I'm currently working on this project (doing what has never been done before, a small step but a giant leap onto the moon's surface.), 
a"GBView.exe" Image-Viewer that can display *.dat image files containing "GB headers". 
It's possible to view the game's graphics(some of *.dat files) using this tool after extracting them from the gamedata.g-d file. 

~ usage syntax options:

gbview.exe 0005_3f2.dat


_________________________________________________________________________________________________________________________________________________________________________________

**(3)** DOOFUS GAME GB-IMAGE-FILES(*_3f2.dat) to TGA PHOTOSHOP CONVERTER --- GB2tga.exe v1.0

INTERNAL ONLY - PRIVATE RELEASE v2.0 has bidirectional conversion capability 

■  **Gb2tga.exe** v1.0 working version tested with one direction GB-Image to TGA(TARGA)PHOTOSHOP. This tool can also convert TGA image file to GB-image BACK (!?)
   HOWEVER (!) Doofus image files are NOT plain image files; they contain assembler graphical code snippets in the header, 
   and therefore, translating them from TGA to GB-image to a fully working format is a really difficult and laborious task. 
   Reverse Operation TGA to GB(game-image) NOT working with version 1.0.. only one way
   
   **UPDATE: INTERNAL ONLY - PRIVATE v2.0 version TESTED and the program works perfectly in both directions,**
   **<br> 100% correctly working = GB(gameimage)to TGA & TGA to GB(gameimage)**
   With version 2.0, you can take the graphics from the game, modify them with Photoshop, and then put them back in game without any issues, game is working :-)
   I received special help :-) regarding the embedded image header with x86 assembly VGA code, which sped up the process(Otherwise, this could have taken 1-2 months.) 
   Version 2.0 was completed. Doofus image files are not just plain images; the image file header contains x86 assembly VGA code, and the game uses this code at runtime. <br>
   **v2.0 forward and backward conversion technology is 100% functional and has been tested**

   <img width="669" height="188" alt="0004_3F2" src="https://github.com/user-attachments/assets/9fc525b4-4425-48b5-bca9-4df299ee7e93" />
<br><br>
~ usage: 
<br>
<br>
gb2tga.exe 0004_3f2.dat 
<br><br>
and >>> GB2TGA tool will convert your Doofus-GB-image into a TGA(TARGA) Photoshop file = "0004_3f2.tga" 
<br>
**with version 1.0 (free download version) only one-way forward operation is possible = GB to TGA(Photoshop)**
_________________________________________________________________________________________________________________________________________________________________________________


**(4)** - **STANDALONE ADLIB MUSIC PLAYER "The Bone Shaker Architect" Engine --- TBSAplay.exe v0.4**

<img width="748" height="261" alt="adlib" src="https://github.com/user-attachments/assets/bf0a00db-2874-4be4-8daa-788f66cd19a3" />


" Believe the unbelievable " The game Doofus uses Adlib music files in tbs format (*.tbs files) **ALL soundtrack files included** :-)
**Player will be available as a standalone for the first time** :-) The original adlib-player engine in the Doofus game operates as a complex mechanism(TSR) 
Extracting this player from within the game and making it work independently was a really laborious and tiring task.

█ **TBSAplay.exe** v0.4 Tested with **DOSBOX(OK)** , **DOSBox Staging(OK)** , **DOSBOX-X(!)**:There's a timing synchronization problem in DOSBOX-X
maybe something is missing in the emulation settings/config in DOSBOX-X? There are stutters(some kind echo problem) in the OPL player sound, 
but there's NO problem with the original DOSBOX and DOSBOX-Staging, they are working properly.

Original classic DOSBOX ->> change/modify-settings ->> dosbox-0.74.conf ->>
[sblaster]
oplmode=opl3
oplemu=compat
oplrate=44100

■  Tbsaplay.exe v0.4  %100 WORKING

~ usage: 

tbsaplay.exe 0055_59e.tbs 

_________________________________________________________________________________________________________________________________________________________________________________

**(5)** - **237UNPAK 1.1a** - Doofus *_237/*_327 files Universal Unpacker/Packer [ INTERNAL ONLY / PRIVATE ]

<img width="962" height="465" alt="237unpak" src="https://github.com/user-attachments/assets/4bc00a94-80c8-4be0-9221-c4afd5b0dffa" />



■ **237unpak.exe** : Specially designed LZSS Decompression + Compression engine, capable of processing >>> *_237.dat  &  *._327.dat files.

This tool **decompresses/unpacks** the 0010_237.dat(This file is packaged and located inside the gamedata.g-d archive.)and all *.237/327 files.. 
you can modify it, then **compresses/repacks** it back to its 0riginal state, allowing the game to open and run the file **<ins>without corruption.</ins>**
The 0010_237.dat file contains the programmer names and text messages that appear on the demo loop before the start menu.
Files *_237 and *_327 contain memory operations and VGA x86 program codes, plus some information used in the game.


_________________________________________________________________________________________________________________________________________________________________________________

■ **DOOFUS GAME ~ ANTI-PIRACY PROTECTION SCREEN :** 

<img width="673" height="696" alt="Protection" src="https://github.com/user-attachments/assets/8d6d5f0c-fbf4-4177-8372-e0570c4a7e51" />


**<ins>Memory addresses have been erased (!)</ins>**

I'm N0T giving details to <ins>lamers</ins> about Cracking , **professionals dont need such an explanation anyway ;-)**



_________________________________________________________________________________________________________________________________________________________________________________

___ The projects are not finished and it seems like it will take a long time ___

___ The source codes for the projects is currently **PRIVATE** ___

___ █  Istanbul / Türkiye (2026)
