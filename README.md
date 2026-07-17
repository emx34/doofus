DOOFUS GAME GAMEDATA.G-D EXTERNAL ARCHIVE FILE EXTRACTOR + REASSEMBLER(Combiner)

I wanted to contribute to the modification of Doofus by making some small additions, 

The game's main executable file is compressed/protected with PKLite. 
After unpacking it, the executable file becomes fully open to reverse engineering, and the real work begins from this point. 
As a first step, I started by writing a small tool that opens the game's external data file "gamedata.g-d," and this is complete. 
Now, unlike previous reverse engineering attempts, there's no need for a Java-based program. 
Using the MS-DOS command-line `doofext.exe`, 
all files in the "gamedata.g-d" image data archive can be easily (1) unpacked into the "\GD" folder, and then (2) reassembled to re-create the "gamedata.g-d" file. 
