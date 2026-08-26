 ■ **DOOFUS --- MSDOS Platform Game - Reverse Engineering Project (Borland C++ & x86 Assembler)**

Doofus is a high-quality platform game with stunning graphics & beautiful musics .. a masterpiece made for MS-DOS.<br>
Doofus uses **Adlib music files in TBS format, all the game musics/soundtrack is included in the tbsaplay.zip package**

After a week to ten days of exhausting work, I've made quite good progress on the MS-DOS platform game Doofus :-) It's great to achieve things that haven't been done before..

The game's music was really great, and after long and intense effort, I converted the adlib player assembler code into a standalone player that runs directly from the MS-DOS command line.
After that, I focused on the unfinished graphics operations and made significant progress there as well. For the first time, Doofus's graphics have reached a level where they can be modified.
Spending hours and days in front of the debugger and examining x86 assembly code is necessary... it's crazy and truly exhausting for the eyes and brain.

The next step will be the in-game graphics and sprites, but that's a really tiring job, requiring hours and days of studying and decoding x86 assembly machine language code, developing Borland C++ code, 
and seriously focusing on this..


____ █  **GREETINGS to friends and people I know __________________________________________________________** 
<br>
<br>
**The Keyboard Caper (TKC) & ALL PhRoZeNCReW 1997 TEAM - (MeMBeRs & #PC97 IRC friends)** <br>
<br>
***EXODUS/c64 , McfISCHER , AKiRA~&~FERiT , BUDU/MURAT , MORGOTH/BLACKWIND , CASPER/CAGTAY ,<br> 
RASEL , GNOSTiC , FALCON/GOKHAN , PLASTiCMAN/ESCAPE , REMiX/CLIQUE , KriS/CLIQUE ,<br>
BLoOdY/CLIQUE , ESQuiRE(Amiga/LEGACY) , CHAO/CAGTAY , DENiZTAS(Stone BBS) , <br>
FIShER KiNG(Rocka Rolla BBS) , MURaTGüL & YaRRiX/ALPER , Baris(B.T.G.) aND otHER fRieNDs in Turkiye! <br>
Selamlar ;-) CEM-abi/ARMA(PC) , ALP-abi/LACINSOFT(Amiga/Suadiye'90s)<br>
<br>
MARQUiS/MARKUS & United Cracking Force (UCF) TEAM: rANDOM , rIDDLER , Dj-PAUL , dA! , nET-KiNG*** <br>
<br>
**____________________________________________________________________________________________________________**
<br>
<br>

<img width="1424" height="1344" alt="doofus4" src="https://github.com/user-attachments/assets/d3c23479-d463-4802-b811-313076b5d517" />




_________________________________________________________________________________________________________________________________________________________________________________
Currently ongoing projects >>> ■ Doofext.exe ■ TBSAplay.exe ■ GBview.exe ■ GB2tga.exe ■ 237unpak.exe <br>
<br>
█ UPCOMING RELEASE : <br>
  ___ **Sprextga.exe - Doofus Sprite Extractor & TGA (Photoshop TARGA) Converter**<br> 
    **(!) NOT READY YET , NOT WORKING YET**<br>
  Sprextga >>> Sprite to TGA & TGA to Sprite Converter:<br>
  This will make it possible to edit sprites with Photoshop and then write them back into the game. <br>
  **Another time-consuming, difficult, and tiring project**

<img width="552" height="311" alt="sprextga" src="https://github.com/user-attachments/assets/663c254f-1521-44aa-9700-1047118a4d3a" />



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



**(2)** - **STANDALONE ADLIB MUSIC PLAYER "The Bone Shaker Architect" Engine --- TBSAplay.exe v0.4**

**■ This player is The 0riginal Adlib-Player Engine for the Doofus game. After much effort, it was extracted from the game and made to run standalone in the MS-DOS command line.**

<img width="899" height="548" alt="adlib" src="https://github.com/user-attachments/assets/83161383-c465-45cc-b2d3-a08a6a1b4afe" />




" Believe the unbelievable " The game Doofus uses Adlib music files in tbs format (*.tbs files) **ALL soundtrack files included** :-)
**Player will be available as a standalone for the first time** :-) **<ins>The 0riginal Adlib-Player Engine</ins>** in the Doofus game operates as a complex mechanism(TSR). 
Extracting this player from within the game and making it work independently was a really laborious and tiring task.

In the initial attempts, the sounds and music were distorted and not working properly. 
There were problems in the early stages of the standalone adlib player project. I tried repeatedly, 
and timing issues arose when I extracted the adlib player from the game; these have now been resolved.
**<ins>A great deal of effort and labor was expended exclusively for this job!</ins>**

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


**(3) - DOOFUS GB-IMAGE-FILES(*_3f2.DAT) VIEWER --- GBview.exe 1.5i UPDATED** 


<img width="1467" height="397" alt="images" src="https://github.com/user-attachments/assets/3796ef6a-d2c6-4ad2-b71b-b7843f5fc1bf" />



■  **GBview.exe** (%100 Full working version)

0004_3f2.dat = Company Logo image (Prestige Softwareentwicklung GmbH logo)

0005_3f2.dat = Game Logo image (Game logo) >>> This file contains 2-images; code needs to be updated.

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

**(4) DOOFUS GB-IMAGE-FILES(*_3f2.dat) to TGA Photoshop CONVERTER --- GB2tga.exe v1.0**


■  **GB2tga.exe** v1.0 working version tested with one direction GB-Image to TGA(TARGA)PHOTOSHOP. This tool can also convert TGA image file to GB-image BACK (!?)
   **HOWEVER (!) The reversal process doesn't work properly in this test version (1.0) yet.** Doofus image files are NOT plain image files; they contain assembler graphical code snippets in the header, 
   and therefore, translating them from TGA to GB-image to a fully working format is a really difficult and laborious task. 
   Reverse Operation TGA to GB(game-image) NOT working with version 1.0.. only one way.
   Version 1.0 only converts graphics, and the graphics header must have embedded VGA x86 assembler code. 
   This process/feature is not yet present in this code; when Doofus Game calls and loads the graphics, 
   the game freezes on a black screen and crashes because there is no code to process and display those graphics within the game. 
   This is a normal situation; the process is incomplete, and the game breaks!..
   
~ usage: 

GB2tga.exe 0004_3f2.dat 


and >>> GB2tga tool will convert your Doofus-GB-image into a TGA(TARGA) Photoshop file = "0004_3f2.tga" 

with version 1.0 (free download version) only one-way forward operation is possible: GB to TGA(Photoshop)


<img width="1151" height="526" alt="gb2tga" src="https://github.com/user-attachments/assets/001bec19-8d2f-424e-8f8b-bb83b2850104" />


   **UPDATE: INTERNAL ONLY - PRIVATE v2.0 version (NOT released) TESTED and the program works perfectly in both directions, 100% correctly working = GB(gameimage)to TGA & TGA to GB(gameimage)**
   **With version 2.0**, you can take the graphics from the game, modify them with Photoshop, and then put them back in game without any issues, game is working :-)
   In version 2.0, the x86 asm vga code is added to the beginning of the newly converted graphics, and the graphics data is repackaged and converted back to the original GB-image standard. 
   :-) Version 2.0 was completed. Doofus image files are not just plain images; the image file header contains x86 assembly VGA code, and the game uses this code at runtime.
   **v2.0 forward and backward conversion technology is 100% functional and has been tested**

_________________________________________________________________________________________________________________________________________________________________________________


**(5) - 237UNPAK 1.2 v6a - Doofus 237/327.dat files Universal Unpacker/Packer (INTERNAL ONLY/PRIVATE) NOT released**

<img width="962" height="465" alt="237unpak" src="https://github.com/user-attachments/assets/0e1ecda6-125d-4ced-ad65-a77d09d8adcb" />



■ **237unpak.exe** : Specially designed LZSS Decompression + Compression engine, capable of processing >>> *_237.dat  &  *._327.dat files.

This tool **Decompresses/Unpacks** the 0010_237.dat(This file is packaged and located inside the gamedata.g-d archive.)and all *.237/327 files.. 
you can modify it, then **Compresses/Packs** it back to its 0riginal state, allowing the game to open and run the file **<ins>without corruption.</ins>**
***This ensures the game opens and runs without corrupting the file; otherwise, the game gets stuck on a black screen, crashes, and becomes corrupted.***
The 0010_237.dat file contains the programmer names and text messages that appear on the demo loop before the start menu.
Files *_237 and *_327 contain memory operations and x86 program codes, plus some other things used in the game.

<img width="661" height="575" alt="lzss" src="https://github.com/user-attachments/assets/4cc02c12-5675-4144-b038-9c272a59e5da" />


***There's a very important point and detail I want to highlight here... The LZSS code used in the Doofus game was designed and released solely for the Decompressor/Unpack process. 
**<ins>There's no LZSS compressor code in the game itself :-)</ins>** ?! The Compressor/Packer code is only in the hands of the programmers at the software company that produced the game. 
Normally, only the decompressor/unpacker code runs within the game, and no other code exists :-) After much effort and with the help.. , 
I examined the decompressor code within the game and reverse-engineered it to write a Compressor/Packer code from scratch (237UNPAK.exe). 
This tool compresses/packs the game files in parallel with, or even with better compression ratios than, 
the original Compressor/Packer in the hands of the game's software company's programmers, and in a compatible way.
Result = Game files compressed with 237UNPAK.exe are decompressed/unpacked by doofus.exe **<ins>without corruption or errors,</ins>** in their original form.***




_________________________________________________________________________________________________________________________________________________________________________________

■ **DOOFUS GAME ~ ANTI-PIRACY PROTECTION SCREEN :** 

<img width="673" height="696" alt="Protection" src="https://github.com/user-attachments/assets/8d6d5f0c-fbf4-4177-8372-e0570c4a7e51" />


**<ins>Memory addresses have been erased (!)</ins>**

I'm N0T giving details to <ins>lamers</ins> about Cr4ck!ng.. **Professionals dont need such an explanation anyway ;-)**



_________________________________________________________________________________________________________________________________________________________________________________

___ The projects are not finished and it seems like it will take a long time

___ The source codes for the projects is currently **PRIVATE**

___ The entire project is my own; working alone, I've only been able to progress this far so far.

___ █  Istanbul / Türkiye (2026) 
<br>
