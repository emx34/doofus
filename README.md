■ DOOFUS --- MS DOS PLATFORM GAME MODIFICATION PROJECT (Borland C++ & x86 Assembler)

<img width="1137" height="598" alt="dof" src="https://github.com/user-attachments/assets/aaa9cd96-9d74-419b-aa64-c75b8f12fa91" />


_________________________________________________________________________________________________________________________________________________________________________________

(1) DOOFUS GAME "gamedata.g-d" EXTERNAL ARCHIVE FILE EXTRACTOR + REASSEMBLER(Combiner) --- Doofext.exe 

■ Doofext.exe -(Full working version)-

I wanted to contribute to the modification of Doofus game by making some small additions, 

The game's main executable file is compressed/protected with PKLite. 
After unpacking it, the executable file becomes fully open to reverse engineering, and the real work begins from this point. 
As a first step, I started by writing a small tool that opens the game's external data file "gamedata.g-d," and this is complete. 
Now, unlike previous reverse engineering attempts, there's no need for a Java-based program. 
Using the MS-DOS command-line `doofext.exe`, 
all files in the "gamedata.g-d" image data archive can be easily (1) unpacked into the "\GD" folder, and then (2) reassembled to re-create the "gamedata.g-d" file. 

Doofext.exe (Doofus gamedata.g-d asset deployment subsystem) 

  ~ usage syntax options:
  
doofext -x     .. eXtracts gamedata.g-d target entities into local \GD\ folder
  
doofext -c     .. reCombines(reassembles) \GD\ folder contents dynamically back into archive
  
doofext -as    .. displays original hardcoded file sizes matrix parameters (file name lister)  *** use this: doofext -as>log.txt

_________________________________________________________________________________________________________________________________________________________________________________

(2) DOOFUS GAME *.DAT GB-IMAGE-FILE VIEWER --- GBview.exe

■ GBview.exe -[beta test version]- IMAGE Viewer ?! NOT completed yet .. tested with 0004_3f2.dat & 0005_3f2.dat

I'm currently working on a new project (doing what has never been done before, a small step but a giant leap onto the moon's surface.), 
a"GBViewer.exe" Graphics-Viewer that can display *.dat image files containing "GB headers". 
It's possible to view the game's graphics(some of *.dat files) using this tool after extracting them from the gamedata.g-d file. Initial tests have been successful, 
but there are some visual issues. The graphics code is complex, and writing a tool that reads, analyzes, manages, and displays this code correctly is a very laborious task.
It requires manual debugging using reverse engineering and extensive code analysis.. days, maybe even months.

~ usage syntax options:

gbview.exe 0005_3f2.dat
_________________________________________________________________________________________________________________________________________________________________________________
■ Believe tHe unbelievable >>> 
another new project is in progress : ((__The Bone Shaker Architect__))  Standalone-Adlib-Player

  NOT READY YET ..

_________________________________________________________________________________________________________________________________________________________________________________

___ The projects are not finished and it seems like it will take a long time ___

___ The source codes for the projects is currently *PRIVATE* ___

