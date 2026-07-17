
DOOFUS GAME GAMEDATA.G-D EXTERNAL ARCHIVE FILE EXTRACTOR + REASSEMBLER(Combiner)

■ Doofext.exe

I wanted to contribute to the modification of Doofus by making some small additions, 

The game's main executable file is compressed/protected with PKLite. 
After unpacking it, the executable file becomes fully open to reverse engineering, and the real work begins from this point. 
As a first step, I started by writing a small tool that opens the game's external data file "gamedata.g-d," and this is complete. 
Now, unlike previous reverse engineering attempts, there's no need for a Java-based program. 
Using the MS-DOS command-line `doofext.exe`, 
all files in the "gamedata.g-d" image data archive can be easily (1) unpacked into the "\GD" folder, and then (2) reassembled to re-create the "gamedata.g-d" file. 

_________________________________________________________________________________________________________________________________________________________________________________

■ GBview.exe

I'm currently working on a new project (Doing what has never been done before, 
a small step but a giant leap onto the moon's surface.), 
a"GBViewer.exe" Graphics-Viewer that can display *.dat image files containing "GB headers". 
It's possible to view the game's graphics(some of *.dat files) using this tool after extracting them from the gamedata.g-d file. Initial tests have been successful, 
but there are some visual issues. The graphics code is very complex, and writing a tool that reads, analyzes, manages, and displays this code correctly is a very laborious task.
