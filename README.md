# ac-analyser-board
AC Power Analyser for low voltage three-phase supplies

https://www.slideshare.net/FebinPaul5/automatic-power-factor-correction-73296799

## Development Preparation

* Use a ESP8266 NodeMCU board to run firmware during development

* Install NodeMCU serial driver on your machine
  * https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers
  * Restart Mac to make it work properly

* Connect NodeMCU board to your machine using virtual USB through Wifi (VirtualHere) to avoid burning it if connected to "hot" circuits!
  * Go to https://www.virtualhere.com/home
  * Download and install server on a Raspberry Pi
  * Download and install client on your notebook
  * Mac Catalina not supported yet (!)
  * Connect NodeMCU USB to Raspberry Pi
  * Connect VirtualHere on your machine to the Raspberry PI IP server
  * On VirtualHere client on your machine, connect it to the remote USB device port (it will create a local usb device)
  * Use the newly created device port to connect to the NodeMCU device connected to Raspberry Pi
  * Now if you have any "AC 220V problem" on the USB port, it will burn just the Raspberry Pi!

* Install Visual Code. Open it and install extension "PlatformIO"

## Development Problems

* When using stutzthings esp board v2.1, upload will only work after resetting ESP8266 manually into bootloader (even with DTR and RTS connected, ck boot is not working for some reason). Connect GND to GPIO0 and then connect GND to RST for reset it. Keep GPIO0 with GND and start upload on PlatformIO.



