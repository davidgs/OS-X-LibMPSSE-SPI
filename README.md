# OS-X-LibMPSSE-SPI

A quick port of FTDI's LibMPSSE-SPI to Mac OS X. Should still compile for Linux and Windows as well. 

For Mac OS X, just cd into the Build/MacOSX directory and make. Once it is built, run sudo make install to install the library and header files in /usr/local/ 

Or move the libMPSSE.dylib into /usr/local/lib and the header files in Release/include/ and Release/include/MacOSX to /usr/local/include/ and you should be good to go.

You will need to also install the FTDI D2XX drivers (http://www.ftdichip.com/Drivers/D2XX.htm), and make sure that the AppleUSBFTDI Driver is NOT loaded. Sometimes you can just use kextunload, sometimes you cannot. Pre El Capitan (10.11) you can edit the Info.plist file in /System/Library/IOUSBKit/AppleUSBFTDI.kext and comment out references to your FTDI chip -- for the FT2232H, look for the string 6010 which is the ID. For the FT232H, it's 6010, etc. This will stop the AppleUSBFTDI.kext from loading when plugged in. 

In OS X El Capitan, you must apparently enable "rootless" but I haven't gotten that far yet.
