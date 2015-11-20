# Broadcom WICED SDK Port for Amazon Dash Button

Unlock the true potential of the Amazon Dash Button.

![Image](http://i.imgur.com/8wumrmc.jpg)

## Build Instructions
* Download WICED SDK version 3.3.1 from [Broadcom]( https://community.broadcom.com/docs/DOC-2312)
* Extract the zip file
* Apply patch 
```sh
$ patch -p1 -s < ../amazon.patch
```
* Build
```sh
$ ./make AMAZONDASH-demo.garage
```
* Download to the board 
```sh
$ ./make AMAZONDASH-demo.garage download run JTAG=stlink-v2
```

## Example UART Output
```
Starting WICED v3.3.1
Platform AMAZONDASH initialised
Started ThreadX v5.6
Initialising NetX_Duo v5.7_sp2
Creating Packet pools
WWD SDIO interface initialised
WLAN MAC Address : 6C:0B:84:7F:99:50
WLAN Firmware    : wl0: Nov  7 2014 16:03:45 version 5.90.230.12 FWID 01-45f08bbf
IPv4 network ready IP: 192.168.0.1
Setting IPv6 link-local address
IPv6 network ready IP: FE80:0000:0000:0000:6E0B:84FF:FE7F:9950
```
## WiFi Garage - PoC Video
[![YouTube Demo Video](http://img.youtube.com/vi/6wzxGu91c1I/0.jpg)](http://www.youtube.com/watch?v=6wzxGu91c1I)

## Working
* WiFi
* RGB LED
* Button
* UART Port

## Todo
* SPI flash
* I2C Microphone

## Thanks to
* [dekuNukem](https://github.com/dekuNukem/Amazon_Dash_Button)
* [emilf](https://github.com/MXCHIP-EMW/WICED-for-EMW)
