# OS-X-LibMPSSE-SPI

A quick port of FTDI's LibMPSSE-SPI to Mac OS X. Should still compile for Linux and Windows as well. 

For Mac OS X, just cd into the Build/MacOSX directory and make. Once it is built, run sudo make install to install the library and header files in /usr/local/ 

Or move the libMPSSE.dylib into /usr/local/lib and the header files in Release/include/ and Release/include/MacOSX to /usr/local/include/ and you should be good to go.
