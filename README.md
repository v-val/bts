# BTS
C++ toolset builder.

Script [straightforward, bash] for getting sequence of tools fetched, configured, build and installed.  
Provides minimal assistance comparing to script you'd write yourself:
- sources fetched and extracted with same command `bts_get` independently on source: supported are all key VCS types and archive formats.
- functions `bts_configure`, `bts_make`, `bts_cmake`, `bts_cmake_build_install` wrap respected commands substituting common options and environment variables automatically
- steps successfully executed once not repeated in subsequent `bts` runs
- any error is fatal
- log is written
- few more fancy commands and auto-set vars for you pleasure. 

Written long ago to get automated build of most recent GCC versions and C / C++ libraries and tools on Linux distros far beyond EOL.
First it was CentOS 6, then CentOS 7, then I added minimal support for MinGW on Windows 7 and 10.

These days [Conan](https://conan.io) and [Vcpkg](https://vcpkg.io/en/) offer this functionality.
However, while there's no question about production superiority of these two, I found uneasy to quickly migrate to one of these
keeping fineness of manual build I have with BTS.

Hence, fellow developers seeking low effort start, easy integrations and good documentation are suggested to use other C/C++ package managers.
BTS in its current state is not very different from bash script, its only advantage is flexibility. 

As mentioned, it's been used on RHEL systems and very minimally on MinGW / MSys.   
Extension to other Linux would be simple, just update around "___# NB: OS-specific___" marks, there are only few of them.

Documentation is in progress.  
For the moment please contact me if need help in using BTS or just submit a ticket.

## Requirements
* cut
* egrep, grep
* perl
* tee

## Trivial example
```bash
cat<<EOF | BTS_ROOT=/dev/shm/bts-dummy bts /dev/stdin

bts_init

while bts_step "Hello world"
do
    echo "HELLO, WORLD"
done

EOF
```

