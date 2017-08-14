# CMake-for-SDL2-Whitespace-Error

For those wanting to use CLion for C/C++ coding using the SDL2 library for game development, there may be some issues with the CMake file. One that yielded very little search results online for a solution is this:  

Target "Target" links to item "-L/usr/lib/x86_64-linux-gnu -lSDL2 " which has leading or trailing whitespace.  This is now an error according to policy
  CMP0004.

Literally only 5 search results come up for this error, so this is a fix for it. Instead of just explicitly stating the include statements, write string(STRIP ${SDL2_INCLUDE_DIRS} SDL2_INCLUDE_DIRS)}.

NOTE: This can be used for other libraries as well if your CMake is acting up. Simply use this statement and substitute the SDL2 stuff with the library you're using. 
