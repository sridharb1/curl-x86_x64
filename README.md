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
  * I switched to the released 7.69.1 branch.
  * git clone [curl-x86_x64](https://github.com/sridharb1/curl-x86_x64.git)
    to another folder
  * Copy the contents of this folder downloaded above to the projects/Windows/VC15
    folder of the curl source tree. Let it overwrite files as needed.
  * `curl -vV` (output of my curl.exe that you can compare to verify)
  ``` shell
  curl 7.69.1-DEV (x86_64-pc-win32) libcurl/7.69.1-DEV OpenSSL/1.1.1g zlib/1.2.11 brotli/1.0.7 libssh2/1.9.0_DEV
  Release-Date: [unreleased]
  Protocols: dict file ftp ftps gopher http https imap imaps ldap ldaps pop3 pop3s rtsp scp sftp smb smbs smtp smtps telnet tftp
  Features: AsynchDNS HTTPS-proxy IPv6 Largefile NTLM SSL UnixSockets brotli libz
  ```

# Note #

To compile curl, you need 

  * [zlib, tested w/ v1.2.11](https://github.com/madler/zlib)
  * Use my [zlib-x86_x64](https://github.com/sridharb1/zlib-x86_x64) to compile zlib on Windows.
  * [OpenSSL, tested w/ v1.1.1g-DEV](https://github.com/openssl/openssl)
  * You can use my [openssl-x86_x64](https://github.com/sridharb1/openssl-x86_x64) to compile openssl on Windows.
  * [libssh2, tested w/ v1.9.0](https://github.com/libssh2/libssh2.git)
  * You can use my [libssh2-x86_x64](https://github.com/sridharb1/libssh2-x86_x64.git) to compile libssh on Windows
  * [brotli, tested w/ v1.0.7+](https://github.com/google/brotli)
  * You can use my [brotli-x86_x64](https://github.com/sridharb1/brotli-x86_x64) to compile brotli on Windows.
