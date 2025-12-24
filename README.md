VZIP — Multithreaded PPM Compressor (C / pthreads / zlib)

Optimized (runtime) C code that compresses a directory of .ppm images in parallel and packages them into a single output file: video.vzip.


Usage:
./vzip <directory>

What it does:
- Scans the given directory for .ppm files and sorts them lexicographically
- Spawns up to 20 pthread workers to compress each file with zlib (deflate level 9)
- Writes each compressed result to a temporary .zzip file
- Appends all .zzip contents into one archive (video.vzip) in sorted order
- Prints compression rate and total runtime

Build:
gcc -O2 -pthread -lz -o vzip vzip.c
