PBKDF2-GCC-OpenSSL_Linux_Windows
================================

GCC and OpenSSL library based PBKDF2 implementation.  Works in Linux, as well as 32-bit and 64-bit Windows with MinGW.

You will need to have the OpenSSL libraries first - for Windows, see the link at https://www.openssl.org/related/binaries.html for the correct place to get them from.  For Linux, OpenSSL is probably already installed, but if need be, something like "sudo apt-get install openssl" should work on Debian derivatives. 

To compile on Windows, the easiest way is to install MinGW via the MinGW Builds installer, which can be found at http://sourceforge.net/projects/mingwbuilds/    (or, apparently, at links off of there since they've joined the overall MinGW-w64 project for both 32-bit and 64-bit Windows MinGW).

For compile run ./compile.sh in linux distros, compile.bat in 32 bit versions of windows and compilex64.bat in 64 bit versions of windows.
You can also run:

gcc -Wall -Wextra -O3 -lssl pbkdf2_openssl.c -o pbkdf2

you may also need to add reference path to openssl library to the end of command, most likely: /usr/lib/libcrypto.so.x.x.x:
example:
gcc -Wall -Wextra -O3 -lssl pbkdf2_openssl.c -o pbkdf2 /usr/lib/libcrypto.so.1.0.0 

