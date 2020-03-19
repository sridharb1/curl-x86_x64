# curl-x86_x64
Native Visual Studio solution/projects to compile on Windows x86/x64/Release/Debug

# Background #
curl provides a project generator for Visual Studio targets. This is
found in the projects folder called generate.bat. This generates
decent project files for lib and src, but it is filled with all kinds
of combinations like WolfSSL, libSSH2, DLL, Release, Debug etc. In
fact, there are too many. In this solution, I focus on clean targets
like Win32/x64/Release/Debug and no more.

The solution also correctly integrates the dependencies to build
curl. I have used zlib, openssl and libssh2.

# Installation #

  * git clone [curl, tested w/ v7.69.1](https://github.com/curl/curl.git)
  * In the projects folder, run generate.bat with VC15 as the
    argument. This will create lib and src VC15 project files.
  * git clone [curl-x86_x64](https://github.com/sridharb1/curl-x86_x64.git)
    to another folder
  * Copy the contents of the folder above to the VC15 folder

# Note #

To compile curl, you need 

  * [zlib, tested w/ v1.2.11](https://github.com/madler/zlib)
  * [OpenSSL, tested w/ v1.1.1e-DEV](https://github.com/openssl/openssl)
  * You can use my [openssl-x86_x64](https://github.com/sridharb1/openssl-x86_x64) to compile openssl on Windows.
  * [libssh2, tested w/ v1.9.0](https://github.com/libssh2/libssh2.git)
  * You can use my [libssh2-x86_x64](https://github.com/sridharb1/libssh2-x86_x64.git) to compile libssh on Windows
