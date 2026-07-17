<img width="958" height="409" alt="image" src="https://github.com/user-attachments/assets/03f22228-8b43-4f61-b1ef-ef5afc8d1ec0" />


(1) DOOFUS GAME GAMEDATA.G-D EXTERNAL ARCHIVE FILE EXTRACTOR + REASSEMBLER(Combiner) --- Doofext.exe

(2) DOOFUS GAME *.DAT GB-IMAGE-FILE VIEWER --- GBview.exe

_________________________________________________________________________________________________________________________________________________________________________________

■ (1) Doofext.exe -(Full working version)-

I wanted to contribute to the modification of Doofus by making some small additions, 

The game's main executable file is compressed/protected with PKLite. 
After unpacking it, the executable file becomes fully open to reverse engineering, and the real work begins from this point. 
As a first step, I started by writing a small tool that opens the game's external data file "gamedata.g-d," and this is complete. 
Now, unlike previous reverse engineering attempts, there's no need for a Java-based program. 
Using the MS-DOS command-line `doofext.exe`, 
all files in the "gamedata.g-d" image data archive can be easily (1) unpacked into the "\GD" folder, and then (2) reassembled to re-create the "gamedata.g-d" file. 

Doofext.exe (Doofus gamedata.g-d asset deployment subsystem) 

  ~ usage syntax options:

  doofext -x     ..Extracts gamedata.g-d target entities into local \GD\ folder
  
  doofext -c     ..Recombines \GD\ folder contents dynamically back into archive
  
  doofext -as    ..Displays original hardcoded file sizes matrix parameters (file name lister)  *** use this: doofext -as>log.txt

_________________________________________________________________________________________________________________________________________________________________________________

■ (2) GBview.exe -[beta test version]- IMAGE Viewer ?! NOT completed yet .. tested with 0004_3f2.dat & 0005_3f2.dat

I'm currently working on a new project (Doing what has never been done before, 
a small step but a giant leap onto the moon's surface.), 
a"GBViewer.exe" Graphics-Viewer that can display *.dat image files containing "GB headers". 
It's possible to view the game's graphics(some of *.dat files) using this tool after extracting them from the gamedata.g-d file. Initial tests have been successful, 
but there are some visual issues. The graphics code is very complex, and writing a tool that reads, analyzes, manages, and displays this code correctly is a very laborious task.
It requires manual debugging using reverse engineering and extensive code analysis—hours, days, maybe even months.

~ usage syntax options:

GBview.exe 0005_3f2.dat


___ The SourceCodes for the projects is currently *PRIVATE* ___
