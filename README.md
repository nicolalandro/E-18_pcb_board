# E-18_pcb_board
Easy pcb ready to print on JLCPCB drawed with kicad and all material that I reach by learning how to develop this board.

![](imgs/JLCPCB.png)

## PCB Files

* kicad file: ./e18sock/e18sock.kicad_pcb
* ready to print file: [grab4_1.zip](e18sock/grab4_1.zip)

## Dev files
Into the folder e18DevTools we can find some manual and the check connection excutable.
The program like the IDE is for windows, so on linux with wine you must follow this guide:

```
dmesg | grep tty 
sudo chmod a+rw /dev/ttyUSB0

ln -fs /dev/ttyUSB0 ~/.wine/dosdevices/com1
ls -l ~/.wine/dosdevices/

wine regedit
```
* create string entries in HKEY_LOCAL_MACHINE\Software\Wine\Ports 
  * where the entry name is the Windows device name (COM1) 
  * and the entry value is the path to the Unix device. (/dev/ttyUSB0)
*  shut down Wine 
```
wineserver -k 
```
* the next time Wine runs a program, your changes will take effect. 
```
wine ./ConfigureTool_Setting_Ebyte_zigbee_v1.20.exe
```
