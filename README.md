
<img width="1424" height="1344" alt="doofus4" src="https://github.com/user-attachments/assets/d3c23479-d463-4802-b811-313076b5d517" />

 ■ **DOOFUS --- MSDOS Platform Game - Reverse Engineering Project (Borland C++ & x86 Assembler)**
<br><br>
Doofus is a high-quality platform game with stunning graphics & beautiful musics .. a masterpiece made for MS-DOS.<br>
Doofus uses **Adlib music files in TBS format, all the game musics/soundtrack is included in the tbsaplay.zip package**

After a week to ten days of exhausting work, I've made quite good progress on the MS-DOS platform game Doofus :-) It's great to achieve things that haven't been done before..

The game's music was really great, and after long and intense effort, I converted the adlib player assembler code into a standalone player that runs directly from the MS-DOS command line.
After that, I focused on the unfinished graphics operations and made significant progress there as well. For the first time, Doofus's graphics have reached a level where they can be modified.
Spending hours and days in front of the debugger and examining x86 assembly code is necessary... it's crazy and truly exhausting for the eyes and brain.

The next step will be the in-game graphics and sprites, but that's a really tiring job, requiring hours and days of studying and decoding x86 assembly machine language code, developing Borland C++ code, 
and seriously focusing on this..
<br>
<br>
**EMX (eMX!)** 
<br>

____ █  **GREETINGS to friends and people I knew in the past __________________________________________________________** 
<br>
<br>
**The Keyboard Caper (TKC) & ALL PhRoZeNCReW 1997 TEAM - (MeMBeRs & #PC97 IRC friends)** <br>
<br>
***EXODUS/c64 , McfISCHER , AKiRA~&~FERiT , BUDU/MURAT , 2K/MORGOTH/BLACKWIND , CASPER/CAGTAY ,<br> 
RASEL , GNOSTiC , FALCON/GOKHAN , PLASTiCMAN/ESCAPE , REMiX/CLIQUE , KriS/CLIQUE ,<br>
BLoOdY/CLIQUE , ESQuiRE(Amiga/LEGACY) , CHAO/CAGTAY , DENiZTAS(Stone BBS) , <br>
FIShER KiNG(Rocka Rolla BBS) , MURaTGüL & YaRRiX/ALPER , Baris(B.T.G.) aND otHER fRieNDs in Turkiye! <br>
Selamlar ;-) CEM ağabey/ARMA(PC) , ALP ağabey/LACINSOFT(Amiga/Suadiye'90s)<br>
<br>
MARQUiS/MARKUS & United Cracking Force (UCF) TEAM: rANDOM , rIDDLER , Dj-PAUL , dA! , nET-KiNG*** <br>
<br>
**■ There's n0 music playing in the background right now :-) but imagine there is -> The_Alibi.SiD & X-FACTOR.SiD**<br>
X-FACTOR SiD DRAX (c64) = https://www.youtube.com/watch?v=inzU_KiYL7Q<br>
The Alibi SiD LAXITY (c64) = https://www.youtube.com/watch?v=HnfuiYOF9jQ<br>
<br>
For some motivation, here's some musics: <br> 
- Bomfunk MCs - Freestyler (Dirty Version - Radio Edit) <br> 
- SG_Lewis_-_Warm__PointBreak_2015_Soundtrack <br>
- Kenny_g - Havana
<br><br>_________________________________________________________________________________________________________________________________________________________________________________
Ongoing projects >>> ■ Sprextga.exe ■ Doofext.exe ■ TBSAplay.exe ■ GBview.exe ■ GB2tga.exe ■ 237unpak.exe
<br> Writing six custom programs for Doofus was really tiring.. there might not be any updates or new features for a while, 
<br> I need to rest.
_________________________________________________________________________________________________________________________________________________________________________________
<br><br>
■ **Sprextga.exe --- Sprextga v1.0a First (alpha) test version**
<br><br>
***Doofus Sprite Extractor & TGA (Photoshop TARGA) * Sprite <---> TGA <---> Sprite CONVERTER***
<br> 
  This will make it possible to edit sprites (hero boy, dog, some other sprites..) with Photoshop and then write them back into the game. 
  <br><br>
  █ The game's original executable file is compressed using PKLite, and this format is supported. 
 <br> ***(automatic PKLite unpacker feature)***
 <br> The original exe file, compressed with pkLite, is included in the sprextga.zip package.
 <br><br>
  ♦♦♦ ***SPECIAL Thanks to BUDU/Murat for their significant support to the sprextga program !***
  

<img width="578" height="612" alt="sprextga3" src="https://github.com/user-attachments/assets/3d138eab-a0b9-4f6b-a1a8-03d1ae056493" />

<br><br>


_________________________________________________________________________________________________________________________________________________________________________________


**(1) - DOOFUS gamedata.g-d EXTERNAL ARCHIVE FILE EXTRACTOR+REASSEMBLER(Combiner) --- Doofext3.exe v2.0** 

■  **Doofext.exe** (%100 Full working version)


<img width="785" height="372" alt="doofext" src="https://github.com/user-attachments/assets/88a94817-b89b-4074-9913-b2aeecc7edca" />


The game's main executable file is compressed/protected with PKLite. 
After unpacking it, the executable file becomes fully open to reverse engineering, and the real work begins from this point. 
**As a first step, I started by writing a small tool that opens the game's external data archive file "gamedata.g-d," and this is complete. 
Now, unlike previous reverse engineering attempts, there's no need for a Java-based program. 
Its using the MS-DOS command-line `doofext.exe`,** <br> 
all files in the "gamedata.g-d" archive can be easily <br> 
**(-x) unpacked** into the "\GD" folder, and then <br>
**(-c) reassembled(pack) to re-create** the "gamedata.g-d" file. **(Packer)** <br>

Doofext.exe (Doofus gamedata.g-d asset deployment subsystem) 

  ~ usage syntax options:
  
doofext -x     : eXtracts gamedata.g-d target entities into local \GD\ folder **(UNPACK)**
  
doofext -c     : reCombines(reassembles) \GD\ folder contents dynamically back into archive **(PACK)**
  
doofext -as    : displays original hardcoded file sizes matrix parameters (file name lister)  *** use this: doofext -as>log.txt




_________________________________________________________________________________________________________________________________________________________________________________



**(2)** - **STANDALONE ADLIB MUSIC PLAYER "The Bone Shaker Architect" Engine --- TBSAplay.exe v0.4**

**■ This player is the original Adlib-Player engine within the Doofus game. After much effort, it was extracted from the game and made to run standalone in the MS-DOS command line.**

<img width="899" height="548" alt="adlib" src="https://github.com/user-attachments/assets/83161383-c465-45cc-b2d3-a08a6a1b4afe" />




" Believe the unbelievable " The game Doofus uses Adlib music files in tbs format (*.tbs files) **ALL soundtrack files included** :-)
**Player will be available as a standalone for the first time** :-) **<ins>The 0riginal Adlib-Player Engine</ins>** in the Doofus game operates as a complex mechanism(TSR). 
Extracting this player from within the game and making it work independently was a really laborious and tiring task.

In the initial attempts, the sounds and music were distorted and not working properly. 
There were problems in the early stages of the standalone adlib player project. I tried repeatedly, 
and timing issues arose when I extracted the adlib player from the game; these have now been resolved.
**<ins>A great deal of effort and labor was expended exclusively for this job!</ins>**

█ **TBSAplay.exe** v0.4 <br><br>
**Tested with** **■ DOSBOX (OK) %100 working** , **■ DOSBox Staging (OK) %100 working** , **■ DOSBOX-X (OK) %100 working** <br>
<br>The problem in DOSBOX-X has been solved... The player is working 100%, I had increased the CPU cycle speed by 4x <br>
And I forgot about this CPU-Cycle speed setting , I realized it too late...(to speed up exe compilation processes), <br>
so adlib-player was having a timing problem :-) The issue is resolved. The player works flawlessly in all DOS emulators. 
<br><br>
Original classic DOSBOX 
<br><br>
->> change/modify-settings ->> dosbox-0.74.conf ->> 
<br><br>
[sblaster] <br>
oplmode=opl3 <br>
oplemu=compat <br>
oplrate=44100 <br>
***CPU cycle speed should be at the default normal speed (!) otherwise, an echo problem occurs in the sound***
<br><br>
■  Tbsaplay.exe v0.4  %100 WORKING
<br><br>
~ usage: 
<br><br>
tbsaplay.exe 0055_59e.tbs 




_________________________________________________________________________________________________________________________________________________________________________________


**(3) - DOOFUS GB-IMAGE-FILES(*_3f2.DAT) VIEWER --- GBview.exe 1.5k UPDATED** 

<img width="1503" height="466" alt="images" src="https://github.com/user-attachments/assets/b10ee8cd-fde6-443c-a110-b0d639713cf3" />




■  **GBview.exe** (%100 Full working version)

0004_3f2.dat = Company Logo image (Prestige Softwareentwicklung GmbH logo)

0005_3f2.dat = Game Logo image (logo + dog head) DUAL-image / SourceCode updated 1.5k

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


<img width="709" height="374" alt="image" src="https://github.com/user-attachments/assets/742463b1-f75a-46d1-946d-6ebc685263fb" />




_________________________________________________________________________________________________________________________________________________________________________________

**(4) DOOFUS GB-IMAGE-FILES(*_3f2.dat) to TGA Photoshop CONVERTER --- GB2tga.exe v1.1**


■  **GB2tga.exe** v1.1 working version tested with one direction GB-Image to TGA(TARGA) PHOTOSHOP. This tool can also convert TGA image file to GB-image BACK (v2.0)
   Doofus image files are NOT plain image files; they contain assembler graphical code snippets in the header, 
   and therefore, translating them from TGA to GB-image to a fully working format is a really difficult and laborious task. 
   Reverse Operation TGA to GB(game-image) NOT working with version 1.1.. only one way.
     
~ usage: 

GB2tga.exe 0004_3f2.dat 


and >>> GB2tga tool will convert your Doofus-GB-image into a TGA(TARGA) Photoshop file = "0004_3f2.tga" 

with version 1.1 (download version) only one-way forward operation is possible: GB to TGA (Photoshop)

<img width="1225" height="526" alt="gb2tga" src="https://github.com/user-attachments/assets/f890abef-0a9b-4d42-9e9b-593d7e8afe07" />




   **ADVANCED v2.0 Version INTERNAL ONLY - PRIVATE (NOT released) TESTED and the program works perfectly in both directions, 100% correctly working = GB(gameimage)to TGA & TGA to GB(gameimage)**
   **With version 2.0**, you can take the graphics from the game, modify them with Photoshop, and then put them back in game without any issues, game is working :-)
   In version 2.0, the x86 asm vga code is added to the beginning of the newly converted graphics, and the graphics data is repackaged and converted back to the original GB-image standard. 
   :-) Version 2.0 was completed. Doofus image files are not just plain images; the image file header contains x86 assembly VGA code, and the game uses this code at runtime.
   **v2.0 forward and backward conversion technology is 100% functional and has been tested**

_________________________________________________________________________________________________________________________________________________________________________________


**(5) - 237UNPAK 1.0 DOOFUS 237/327.dat files Universal UNPACKER** 
<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **(v1.2 v6a INTERNAL ONLY/PRIVATE PACKER/Compressor)**
<br>
<br>

<img width="962" height="465" alt="237unpak" src="https://github.com/user-attachments/assets/0e1ecda6-125d-4ced-ad65-a77d09d8adcb" />



■ **237unpak.exe** : Specially designed LZSS Decompression + Compression engine, capable of processing >>> *_237.dat  &  *._327.dat files.

<ins>**In version 1.0, only the UNPACK/Decompressor feature works ■ The advanced PACKER/Compressor feature is only available in version 1.2**</ins>
This tool **Decompresses/Unpacks** the 0010_237.dat(This file is packaged and located inside the gamedata.g-d archive.)and all *.237/327 files.. 
you can modify it, then **Compresses/Packs** it back to its 0riginal state, allowing the game to open and run the file **<ins>without corruption.</ins>**
***This ensures the game opens and runs without corrupting the file; otherwise, the game gets stuck on a black screen, crashes, and becomes corrupted.***
The 0010_237.dat file contains the programmer names and text messages that appear on the demo loop before the start menu.
Files *_237 and *_327 contain memory operations and x86 program codes, plus some other things used in the game.

<img width="661" height="575" alt="lzss" src="https://github.com/user-attachments/assets/4cc02c12-5675-4144-b038-9c272a59e5da" />


***There's a very important point and detail I want to highlight here... The LZSS code used in the Doofus game was designed and released solely for the Decompressor/Unpack process. 
**<ins>There's no LZSS compressor code in the game itself :-)</ins>** ?! The Compressor/Packer code is only in the hands of the programmers at the software company that produced the game. 
Normally, only the decompressor/unpacker code runs within the game, and no other code exists :-) After much effort and with the help..I examined the decompressor code within the game and 
reverse-engineered it to write a Compressor/Packer code from scratch (237UNPAK.exe).This tool compresses/packs the game files in parallel with, or even with better compression ratios than, 
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
