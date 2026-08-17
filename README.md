■ DOOFUS --- MS DOS PLATFORM GAME MODIFICATION PROJECT (Borland C++ & x86 Assembler)

Doofus is a high-quality platform game with stunning graphics & beautiful musics .. a masterpiece made for MS-DOS.

<img width="1390" height="1105" alt="doofus2tr" src="https://github.com/user-attachments/assets/9a7eb031-e275-4125-a451-12d365167918" />

_________________________________________________________________________________________________________________________________________________________________________________

(1) - DOOFUS GAME "gamedata.g-d" EXTERNAL ARCHIVE FILE EXTRACTOR + REASSEMBLER(Combiner) = Unpacker/Packer --- Doofext.exe 

■  Doofext.exe (Full working version)

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

(2) - DOOFUS GAME GB-IMAGE-FILES(*_3f2.DAT) VIEWER --- GBview.exe 1.0d -[beta test version]-

■  GBview.exe * NOT completed yet .. tested with = 0004_3f2.dat , 0005_3f2.dat , 0008_3f2.dat , 0062_3f2.dat 

0004_3f2.dat = Company Logo image (Prestige Softwareentwicklung GmbH logo)

0005_3f2.dat = Game Logo image (Doofus game logo)

0006_3f2.dat = Doofus boy dog monkey elephant image

0008_3f2.dat = HighScore image

0062_3f2.dat = Gameover image

I'm currently working on this project (doing what has never been done before, a small step but a giant leap onto the moon's surface.), 
a"GBView.exe" Image-Viewer that can display *.dat image files containing "GB headers". 
It's possible to view the game's graphics(some of *.dat files) using this tool after extracting them from the gamedata.g-d file. Initial tests have been successful, 
but there are some visual issues. The graphics code is complex, and writing a tool that reads, analyzes, manages & palette config and displays this code correctly is a very laborious task.
It requires manual debugging using reverse engineering and extensive code analysis.. days, maybe even months.

~ usage syntax options:

gbview.exe 0005_3f2.dat


_________________________________________________________________________________________________________________________________________________________________________________

(3) DOOFUS GAME GB-IMAGE-FILES(*_3f2.dat) to TGA(TARGA)PHOTOSHOP  CONVERTER --- GB2tga.exe 

■  Gb2tga.exe , working version tested with one direction GB-Image to TGA(TARGA)PHOTOSHOP. This tool can also convert TGA image file to GB-image BACK (!?)
   HOWEVER (!) Doofus image files are NOT plain image files; they contain assembler graphical code snippets in the header, 
   and therefore, translating them from TGA to GB-image to a fully working format is a really difficult and laborious task. 
   Reverse Operation NOT tested on working game ?! It most likely won't work... there are some details involved, such as the size of the gamedata.g-d file, 
   the presence of asm VGA code in the gb-image header, etc. These aren't easy tasks !
   As you noticed, this tool is FREE (I might look into this later if I have some free time , far far future ?!).

~ usage: 

gb2tga.exe 0004_3f2.dat    
and >>> GB2TGA tool will convert your Doofus-GB-image into a TGA(TARGA) Photoshop file = "0004_3f2.tga"
_________________________________________________________________________________________________________________________________________________________________________________


(4) - DOOFUS GAME STANDALONE ADLIB MUSIC PLAYER "The Bone Shaker Architect" Engine --- TBSAplay.exe v0.4

<img width="614" height="261" alt="adlib" src="https://github.com/user-attachments/assets/5306eaf9-b413-4ec2-bd41-aee77b24fe2d" />


" Believe the unbelievable " The game Doofus uses Adlib music files in tbs format (*.tbs files) 
Player will be available as a standalone for the first time :-) The original adlib-player engine in the Doofus game operates as a complex mechanism(TSR) 
Extracting this player from within the game and making it work independently was a really laborious and tiring task.

█ TBSAplay.exe v0.4 Tested with DOSBOX(OK) , DOSBox Staging(OK) , DOSBOX-X(!):There's a timing synchronization problem in DOSBOX-X
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

(5) - 237UNPAK 1.1a - Doofus *_237/*_327 files Universal Unpacker/Packer [ INTERNAL ONLY / PRIVATE ]

<img width="962" height="465" alt="237" src="https://github.com/user-attachments/assets/b298fe3e-35a1-4aa2-8433-31e4cf1bceae" />


■ 237unpak.exe : Specially designed LZSS Decompression + Compression engine, capable of processing >>> *_237.dat  &  *._327.dat files.

This tool **decompresses/unpacks** the 0010_237.dat(This file is packaged and located inside the gamedata.g-d archive.)and all *.237/327 files.. 
you can modify it, then **compresses/repacks** it back to its 0riginal state, allowing the game to open and run the file **<ins>without corruption.</ins>**
The 0010_237.dat file contains the programmer names and text messages that appear on the demo loop before the start menu.


_________________________________________________________________________________________________________________________________________________________________________________

■ DOOFUS GAME ~ ANTI-PIRACY PROTECTION SCREEN : 

<img width="665" height="696" alt="Doofus Protection screen(between levels)-2" src="https://github.com/user-attachments/assets/11c0103c-3474-435f-ac2e-05d3575c8995" />

Memory addresses have been deleted, 

I'm N0T giving details to <ins>lamers</ins> about Cracking , **professionals dont need such an explanation anyway ;-)**



_________________________________________________________________________________________________________________________________________________________________________________

___ The projects are not finished and it seems like it will take a long time ___

___ The source codes for the projects is currently **PRIVATE** ___

___ █  Istanbul / TURKIYE / 2026 
