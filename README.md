# formattingForAllCodingWeDo

Note that this coding style is language agnostic and coding paradigm agnostic.  
Any coder from any coding language background can easily know what is going on 
and contribute.  We use no pointers, no functions, no classes, and keep things 
really simple.  We also do not use any libraries or dependencies (for the most 
part) and everything goes into one .cpp file.  All code goes into the main while 
loop.  Any special functionality must use the Win32 API.  Besides the main.cpp 
file and .exe file, a project will just have possibly some .txt files and maybe 
some .jpg files.  That will be all that's in the folder for the most part.  For 
data structures we just use an array of strings or integers.  All code should 
include debugging Boolean statements for testing purposes.  All variables should 
be global and listed at the top in the variables declaration section.  Code comments 
should be kept to a minimum because the code variable naming convention serves 
as code comments and documentation all at once - as do the debug Boolean console
out statements littered throughout.  All major sections of code should include 
nextSection followed by the name of what that section does.  This way all the 
sections can be navigated to very quickly from an index at the top by selecting 
the index line item and hitting control + f to find that section lower down in the 
code.  Alternatively, sections can be quickly navigated through just by hitting 
control+f and typing in nextSection and hitting return.  All code should be able 
to run on any Windows computer just by double-clicking the .exe file and no 
additional dependencies or downloads should be needed.

I'm okay with you guys reusing code from these projects for whatever you want.  
Hence the MIT license I chose.  But if you want to contribute, please try to keep 
it tightly conforming to my spacing conventions, variable usage conventions, 
organizational scheme, debugging scheme, etc.  This way I can reuse the code 
easily for any project and it looks like the way I write it.  I included some 
basic library/headers I have used historically below and I'd like you to try 
to stick to those so that I don't have to download any libraries to get the code 
to run in my IDE which is Dev C++ version 4.9.9.2.  If you want a library I 
haven't used, make sure it is one that is included with that IDE.  But ideally, 
try to avoid using libraries entirely and just code from scratch.  This way as 
much of the code as possible is done using the same formatting and is easy for me 
to read.

In some cases, this github will contain entire projects, but in many cases, 
it will just contain a single algorithm that I will have on here and be able 
to copy paste into my main code base which will not be shared.  This repository 
will have many algorithms that will form my code base but will just not have the 
whole code base in one big shot because I want a lot of the pieces to be missing 
so that people can't out right just copy paste my entire robot into their own 
project which is not my goal.  At least they would have to work for it and pull 
bits and pieces from here and elsewhere.  Plus my robot's code base may have
algorithms I wrote that I do not wish to share so it will not be just pasted into 
here.

Special formatting notes: note the four spaces between each indented section of 
code.  Note the eight returns before each additional section of code separating 
the different sections.  Note the space after every if statement before the (.  
Note how the open and close brackets are each on their own line.  Until you get 
used to my formatting, it is best to copy paste preformatted code of mine and 
then replace all the variable names and replace the functionality so that you 
inherit all the proper formatting.




Here are some example libraries/headers that I'm okay with you guys using 
because they come with most IDE's prepackaged:
        
#define _WIN32_WINNT 0x0501            //tells the compiler that this is windowsXP or higher... by telling the compiler this, we gain access to the GetConsoleWindow(); command and the PrintWindow(); command  
                                         //also note that this command MUST be written in BEFORE #include <windows.h>...
                                         
                                       
#include <iostream>
#include <windows.h>
#include <Psapi.h>  //enables us to use the EnumProcesses function which lets us locate all processes with the name My Other Game.exe and close them if they are open - perfect for restarter closing strays...
#include <Shlwapi.h>  //enables us to use the PathIsDirectory function
#include <winsock2.h>  //implements the tcp/ip library for access to commands involving socket based packet sending in realtime using tcp protocol for my realtime communications needs for fightingPits and for realtime remote desktopping...
#include <iomanip>
#include <time.h>    //allows getting system time
#include <math.h>     //allows use of sqrt() function...
#include <graphics.h>      //the header we need to use for creating of windows using borland's winBGlm library...
#include <fstream>     //must include this header in order to access files
#include <wininet.h>    //implements ftp command library for access to commands like InternetOpen and InternetConnect; also had to include this library in "tools">"compiler options">"add these lines to linker" as -lwininet... the library wininet is included with dev C++ in its libraries folder...
#include <GL/gl.h>  //header file for the openGL32 library
#include <GL/glu.h>  //header file for the glu32 library which is the openGL utility library
#include <security.h>  //Header file for secured socket communications SSPI client and server stuff with authentication; goes with secur32.lib
