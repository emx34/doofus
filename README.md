 ■ **DOOFUS --- MS DOS PLATFORM GAME MODIFICATION PROJECT (Borland C++ & x86 Assembler)**

Doofus is a high-quality platform game with stunning graphics & beautiful musics .. a masterpiece made for MS-DOS.<br>
Doofus uses **Adlib music files in TBS format, all the game musics/soundtrack is included in the tbsaplay.zip package**

After a week to ten days of exhausting work, I've made quite good progress on the MS-DOS platform game Doofus :-) It's great to achieve things that haven't been done before..

The game's music was really great, and after long and intense effort, I converted the adlib player assembler code into a standalone player that runs directly from the MS-DOS command line.
After that, I focused on the unfinished graphics operations and made significant progress there as well. For the first time, Doofus's graphics have reached a level where they can be modified.
Spending hours and days in front of the debugger and examining x86 assembly code is necessary... it's crazy and truly exhausting for the eyes and brain.

The next step will be the in-game graphics and sprites, but that's a really tiring job, requiring hours and days of studying and decoding x86 assembly machine language code, developing Borland C++ code, 
and seriously focusing on this..



<img width="1390" height="1316" alt="doofus4" src="https://github.com/user-attachments/assets/8b2eb4f8-05d1-4c52-8ab3-96fa483f0c7f" />



_________________________________________________________________________________________________________________________________________________________________________________


**(1) - DOOFUS gamedata.g-d EXTERNAL ARCHIVE FILE EXTRACTOR+REASSEMBLER(Combiner) --- Doofext3.exe v2.0** 

■  **Doofext.exe** (%100 Full working version)


<img width="785" height="372" alt="doofext" src="https://github.com/user-attachments/assets/88a94817-b89b-4074-9913-b2aeecc7edca" />


The game's main executable file is compressed/protected with PKLite. 
After unpacking it, the executable file becomes fully open to reverse engineering, and the real work begins from this point. 
**As a first step, I started by writing a small tool that opens the game's external data archive file "gamedata.g-d," and this is complete. 
Now, unlike previous reverse engineering attempts, there's no need for a Java-based program. 
Its using the MS-DOS command-line `doofext.exe`,** 
all files in the "gamedata.g-d" archive can be easily **(1) unpacked** into the "\GD" folder, and then 
**(2) reassembled(pack) to re-create** the "gamedata.g-d" file. **(Unpacker & Packer)**

Doofext.exe (Doofus gamedata.g-d asset deployment subsystem) 

  ~ usage syntax options:
  
doofext -x     : eXtracts gamedata.g-d target entities into local \GD\ folder **(UNPACK)**
  
doofext -c     : reCombines(reassembles) \GD\ folder contents dynamically back into archive **(PACK)**
  
doofext -as    : displays original hardcoded file sizes matrix parameters (file name lister)  *** use this: doofext -as>log.txt


_________________________________________________________________________________________________________________________________________________________________________________



**(4)** - **STANDALONE ADLIB MUSIC PLAYER "The Bone Shaker Architect" Engine --- TBSAplay.exe v0.4**


<img width="834" height="472" alt="adlib" src="https://github.com/user-attachments/assets/8b10a6a6-28e4-4239-a2e6-727166615c06" />



" Believe the unbelievable " The game Doofus uses Adlib music files in tbs format (*.tbs files) **ALL soundtrack files included** :-)
**Player will be available as a standalone for the first time** :-) The original adlib-player engine in the Doofus game operates as a complex mechanism(TSR) 
Extracting this player from within the game and making it work independently was a really laborious and tiring task.

█ **TBSAplay.exe** v0.4 Tested with **DOSBOX(OK)** , **DOSBox Staging(OK)** , **DOSBOX-X(!)**:There's a timing synchronization problem in DOSBOX-X
maybe something is missing in the emulation settings/config in DOSBOX-X? There are stutters(some kind echo problem) in the OPL player sound, 
but there's NO problem with the original DOSBOX and DOSBOX-Staging, they are working properly.

Original classic DOSBOX 

->> change/modify-settings ->> dosbox-0.74.conf ->>

[sblaster]
oplmode=opl3
oplemu=compat
oplrate=44100

■  Tbsaplay.exe v0.4  %100 WORKING

~ usage: 

tbsaplay.exe 0055_59e.tbs 


_________________________________________________________________________________________________________________________________________________________________________________


**(2) - DOOFUS GB-IMAGE-FILES(*_3f2.DAT) VIEWER --- GBview.exe 1.5i UPDATED** 


<img width="1467" height="397" alt="images" src="https://github.com/user-attachments/assets/3796ef6a-d2c6-4ad2-b71b-b7843f5fc1bf" />



■  **GBview.exe** (%100 Full working version)

0004_3f2.dat = Company Logo image (Prestige Softwareentwicklung GmbH logo)

0005_3f2.dat = Game Logo image (Doofus game logo)

0006_3f2.dat = Doofus boy dog monkey elephant image

0008_3f2.dat = HighScore image

0015_43e.dat = Bonus screen

0018_48b.dat = The market and the picture of the man that appear at the end of the level

0062_3f2.dat = Gameover image

0063_3f2.dat = End game "welldone" screen

0064_3f6.dat = Congratulations at the end of the game screen


Doing what has never been done before, a small step but a giant leap onto the moon's surface.. 
a GBView.exe, Image-Viewer that can display *.dat image files containing "GB headers". 
It's possible to view the game's graphics(some of *.dat files) using this tool after extracting them from the gamedata.g-d archive file. 

~ usage syntax options:

gbview.exe 0005_3f2.dat


<img width="749" height="411" alt="gbview" src="https://github.com/user-attachments/assets/1ea6a024-c1f3-41c8-a11e-080b686c9b7e" />


_________________________________________________________________________________________________________________________________________________________________________________

**(3) DOOFUS GB-IMAGE-FILES(*_3f2.dat) to TGA Photoshop CONVERTER --- GB2tga.exe v1.0**


■  **GB2tga.exe** v1.0 working version tested with one direction GB-Image to TGA(TARGA)PHOTOSHOP. This tool can also convert TGA image file to GB-image BACK (!?)
   HOWEVER (!) Doofus image files are NOT plain image files; they contain assembler graphical code snippets in the header, 
   and therefore, translating them from TGA to GB-image to a fully working format is a really difficult and laborious task. 
   Reverse Operation TGA to GB(game-image) NOT working with version 1.0.. only one way
   
   **UPDATE: INTERNAL ONLY - PRIVATE v2.0 version (NOT released) TESTED and the program works perfectly in both directions,**
   **<br> 100% correctly working = GB(gameimage)to TGA & TGA to GB(gameimage)**
   With version 2.0, you can take the graphics from the game, modify them with Photoshop, and then put them back in game without any issues, game is working :-)
   I received special help :-) regarding the embedded image header with x86 assembly VGA code, which sped up the process(Otherwise, this could have taken a month or more) 
   Version 2.0 was completed. Doofus image files are not just plain images; the image file header contains x86 assembly VGA code, and the game uses this code at runtime.
   **v2.0 forward and backward conversion technology is 100% functional and has been tested**

   <img width="669" height="188" alt="0004_3F2" src="https://github.com/user-attachments/assets/9fc525b4-4425-48b5-bca9-4df299ee7e93" />

~ usage: 

GB2tga.exe 0004_3f2.dat 


and >>> GB2tga tool will convert your Doofus-GB-image into a TGA(TARGA) Photoshop file = "0004_3f2.tga" 

with version 1.0 (free download version) only one-way forward operation is possible: GB to TGA(Photoshop)
_________________________________________________________________________________________________________________________________________________________________________________


**(5) - 237UNPAK 1.2 - Doofus _237 / _327.dat files Universal Unpacker/Packer (INTERNAL ONLY/PRIVATE) NOT released**

<img width="962" height="465" alt="237unpak" src="https://github.com/user-attachments/assets/4bc00a94-80c8-4be0-9221-c4afd5b0dffa" />



■ **237unpak.exe** : Specially designed LZSS Decompression + Compression engine, capable of processing >>> *_237.dat  &  *._327.dat files.

This tool **Decompresses/Unpacks** the 0010_237.dat(This file is packaged and located inside the gamedata.g-d archive.)and all *.237/327 files.. 
you can modify it, then **Compresses/Packs** it back to its 0riginal state, allowing the game to open and run the file **<ins>without corruption.</ins>**
***This ensures the game opens and runs without corrupting the file; otherwise, the game gets stuck on a black screen, crashes, and becomes corrupted.***
The 0010_237.dat file contains the programmer names and text messages that appear on the demo loop before the start menu.
Files *_237 and *_327 contain memory operations and VGA x86 program codes, plus some other things used in the game.

<img width="661" height="575" alt="lzss" src="https://github.com/user-attachments/assets/4cc02c12-5675-4144-b038-9c272a59e5da" />


***There's a very important point and detail I want to highlight here... The LZSS code used in the Doofus game was designed and released solely for the Decompressor/Unpack process. 
There's no LZSS compressor code in the game itself :-) ?! The Compressor/Packer code is only in the hands of the programmers at the software company that produced the game. 
Normally, only the decompressor/unpacker code runs within the game, and no other code exists :-) After much effort and with the help.. , 
I examined the decompressor code within the game and reverse-engineered it to write a Compressor/Packer code from scratch (237UNPAK.exe). 
This tool compresses/packs the game files in parallel with, or even with better compression ratios than, 
the original Compressor/Packer in the hands of the game's software company's programmers, and in a compatible way.
Result = Game files compressed with 237UNPAK.exe are decompressed/unpacked by doofus.exe **<ins>without corruption or errors,</ins>** in their original form.***

_________________________________________________________________________________________________________________________________________________________________________________

■ **DOOFUS GAME ~ ANTI-PIRACY PROTECTION SCREEN :** 

<img width="673" height="696" alt="Protection" src="https://github.com/user-attachments/assets/8d6d5f0c-fbf4-4177-8372-e0570c4a7e51" />


**<ins>Memory addresses have been erased (!)</ins>**

I'm N0T giving details to <ins>lamers</ins> about Cracking , **professionals dont need such an explanation anyway ;-)**



_________________________________________________________________________________________________________________________________________________________________________________

___ The projects are not finished and it seems like it will take a long time ___

___ The source codes for the projects is currently **PRIVATE** ___

___ █  Istanbul / Türkiye (2026)
