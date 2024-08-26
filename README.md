# BTS
C / C++ toolset builder.

Script helping to get dependencies configured, built and installed as needed.  
Not a package manager: remove, update and recursive dependency tracking are not provided, not at the moment.  
Please consider **BTS** for flexibility and clarity; building specific set of tools and libraries with specific options once in a while is what it can help with.

[Conan](https://conan.io) and [Vcpkg](https://vcpkg.io/en/) are industry leaders in such a domain.
With no doubts in production superiority of these two, I found uneasy to quickly migrate to
one of them keeping fineness of manual build I have with **BTS**.

Comparing to straightforward script:
- sources fetched and extracted with one command `bts_get`: all key VCS, URL and archive types are supported.
- `bts_configure`, `bts_make`, `bts_cmake`, `bts_cmake_build_install` wrap respected commands
  with auto-substituted common options and environment variables.
- successfully executed steps are not repeated in subsequent `bts` runs.
- any error is fatal.
- log is written.
- few more fancy commands and auto-set vars available for you convenience.

<!--
Written to automate build of most recent dependencies with most recent GCC on Linux distros far beyond EOL.
First it was CentOS 6, then CentOS 7, then I added minimal support for MinGW on Windows 7 and 10.

Despite quick try of [Spack](https://github.com/spack/spack).

As mentioned, it's been used on RHEL systems and very minimally on MinGW / MSys.   
Extension to other Linux would be simple, just update around "___# NB: OS-specific___" marks, there are only few of them.

Documentation is in progress.

For the moment please contact me if seeking help in using BTS or just submit a ticket.
-->