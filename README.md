VZIP — PPM Compressor (C / zlib)

C project that compresses a directory of .ppm image files and packages them into a single output archive called video.vzip.

Usage:
make
./vzip <directory>

What it does:
- Scans the given directory for .ppm files
- Sorts them lexicographically
- Compresses each file with zlib
- Appends all compressed outputs into video.vzip
- Prints compression rate and runtime

Build:
make

Test:
make test

Clean:
make clean
