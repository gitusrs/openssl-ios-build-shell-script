# openssl-ios-build-shell-script
Build openssl with shell script-only support to use on iOS, and bitcode is supported.

# Usage
1.Download openssl source code(openssl-*.tar.gz). 

2.Move openssl-build.sh into the folder where the openssl-*.tar.gz is cotained.

3.Edit openssl-build.sh, set the value of OPENSSL_COMPRESSED_FN and -miphoneos-version-min( supported minimal iOS version ).
If you want to support the bitcode, find "export CC=${CLANG} -arch ${ARCH} -miphoneos-version-min=6.0", add the -fembed-bitcode option at end of line.

4.cd the the folder where the openssl-*.tar.gz is cotained.

5.Execute openssl-build.sh, libraries are created at "openssl-version-build/universal/".


