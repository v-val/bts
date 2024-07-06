# bts
C++ toolset builder.

Originally I wrote it to use recent libs and tools on obsolete platforms.  
Conan and Vcpkg do this, but I wasn't able to quickly achieve fineness of manual build with them. 

First it was CentOS 6, then CentOS 7, then I added minimal support for MinGW on Windows.

Extension to other Linux distros is trivial, just update around "___# NB: OS-specific___" marks, there are only few of them.    

Quality is POC.