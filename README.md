# Fork reason
* Fork of mmozeiko's [portable-msvc.py](https://gist.github.com/mmozeiko/7f3162ec2988e81e56d5c4e22cde9977), extending the original script with `--linux` flag to allow installation in Linux as well.
* When passed the `--linux` flag, the script:
    * uses `msiextract` instead of `msiexec.exe` to install the MSI files,
    * creates a bash version of the original `setup_x64.bat` script to set environment variables.
# Usage
## Linux
```sh
./portable-msvc-linux.py --linux
cd msvc
. ./setup_x64.sh
# write hello world in C
wine ./VC/Tools/MSVC/14.50.35717/bin/Hostx64/x64/cl.exe hello.c
```