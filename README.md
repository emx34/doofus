■ DOOFUS --- MS DOS PLATFORM GAME MODIFICATION PROJECT (Borland C++ & x86 Assembler)

Doofus is a masterpiece platform game made for MS-DOS. A high-quality platform game with stunning graphics.

(!) Tested with DOSBOX-X (https://dosbox-x.com/)

<img width="1390" height="1105" alt="doofus2" src="https://github.com/user-attachments/assets/695c99ae-8f01-4f6d-9873-9d89f9a7e829" />

_________________________________________________________________________________________________________________________________________________________________________________

(1) - DOOFUS GAME "gamedata.g-d" EXTERNAL ARCHIVE FILE EXTRACTOR + REASSEMBLER(Combiner) --- Doofext.exe 

■  Doofext.exe -(Full working version)-

I wanted to contribute to the modification of Doofus game by making some small additions, 

The game's main executable file is compressed/protected with PKLite. 
After unpacking it, the executable file becomes fully open to reverse engineering, and the real work begins from this point. 
As a first step, I started by writing a small tool that opens the game's external data archive file "gamedata.g-d," and this is complete. 
Now, unlike previous reverse engineering attempts, there's no need for a Java-based program. 
Using the MS-DOS command-line `doofext.exe`, 
all files in the "gamedata.g-d" image data archive can be easily (1) unpacked into the "\GD" folder, and then 
(2) reassembled to re-create the "gamedata.g-d" file. 

Doofext.exe (Doofus gamedata.g-d asset deployment subsystem) 

  ~ usage syntax options:
  
doofext -x     .. eXtracts gamedata.g-d target entities into local \GD\ folder
  
doofext -c     .. reCombines(reassembles) \GD\ folder contents dynamically back into archive
  
doofext -as    .. displays original hardcoded file sizes matrix parameters (file name lister)  *** use this: doofext -as>log.txt

_________________________________________________________________________________________________________________________________________________________________________________

(2) - DOOFUS GAME *.DAT GB-IMAGE-FILE VIEWER --- GBview.exe 1.0d -[beta test version]-

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

(3) DOOFUS GAME *_3f2.dat GB-IMAGE-FILES to TGA(TARGA)PHOTOSHOP  CONVERTER --- GB2tga.exe 

■  Gb2tga.exe , Working verion Tested with one direction GB-Image to TGA(TARGA)PHOTOSHOP. This tool can convert TGA image file to GB-image BACK (!?)
   HOWEVER (!) Doofus image files are NOT plain image files; they contain assembler graphical code snippets in the header, 
   and therefore, translating them from TGA to GB-image to a fully working format is a really difficult and laborious task. 
   Reverse Operation NOT tested on working game ?! It most likely won't work... there are some details involved, such as the size of the gamedata.g-d file, 
   the presence of asm VGA code in the gb-image header, etc. These aren't easy tasks !
   As you noticed, this tool is FREE (I might look into this later if I have some free time , far far future ?!).

~ usage: 

gb2tga.exe 0004_3f2.dat    
and >>> GB2TGA tool will convert your Doofus-GB-image into a TGA(TARGA) Photoshop file = "0004_3f2.tga"
_________________________________________________________________________________________________________________________________________________________________________________


(4) - DOOFUS GAME STANDALONE ADLIB MUSIC PLAYER  "(T)he (B)one (S)haker (A)rchitect" Engine --- TBSAplay.exe 0.1beta

■  Tbsaplay.exe * WORKING BUT NOT READY YET (!)   
   █ Finally 0.1 First beta test relaase :-) working but BUGGY.. delayed , speed not fixed yet .. Im working on it 

" Believe the unbelievable " The game Doofus uses Adlib music files in "*.tbs" format. 
Player will be available as a standalone for the first time :-) The player operates as a complex mechanism (TSR)

~ usage: 

tbsaplay.exe 0055_59e.tbs 

_________________________________________________________________________________________________________________________________________________________________________________

___ The projects are not finished and it seems like it will take a long time ___

___ The source codes for the projects is currently *PRIVATE* ___


