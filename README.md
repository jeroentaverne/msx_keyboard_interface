👋 Hi, I’m Jeroen Taverne

I have created an interface to connect a USB keyboard to a MSX computer, currently there are two versions:
- For Philips NMS8250, NMS8255 and NMS8280 with the 26 pin connector
- For Sony machines with the 13 pin keyboard connector like HB-F700, HB-F500, HB-F900
- For Viktor HC-90 and HC-95 with the 20 pin connector

It consists of a small box (3D printed) with internal small computer which reads the USB keycodes and simulates the keypresses on the keyboard matrix.

Extra features are added which are normally not possible with the real MSX keyboard.

Some keyboards don't allow pressing cursor keys and space button at the same time because of ghosting. Playing games like Nemesis or Quarth could couse issues. That's why the left and right windows keys can be used as space as well with this my keyboard interface. Also see this post: https://www.msx.org/forum/semi-msx-talk/emulation/bluemsx-24-25-keyboard-emulation

The firmware can be upgraded by connecting it to Windows/MAC/Linux using the micro USB connection. The firmware update is just drag and drop a file.

You can order it by sending me an email with the keyword MSX in the subject to: j.taverne@gmail.com
For support and feature requests you can also send me an email or post a message through github.

![alt text](https://github.com/jeroentaverne/msx_keyboard_interface/blob/main/photos/sony1.jpg)
![alt text](https://github.com/jeroentaverne/msx_keyboard_interface/blob/main/photos/sony3.jpg)
![alt text](https://github.com/jeroentaverne/msx_keyboard_interface/blob/main/photos/photo1.jpg)

WARNING: NEVER connect the interface or USB keyboard while the MSX is powered on!

Setup:

- The interface doesn't need external power, the micro USB connector stays disconnected during normal use
-	Insert the interface into the keyboard connector of the MSX. Make sure for the Philips version the "TOP SIDE" text is pointing to the top.
-	Connect an USB keyboard which matches the layout of the original MSX keyboard, else the symbols will be in the wrong locations. For instance: Sony HB-F700P needs US international keyboard. HB-F700S need Spanish keyboard. HB-F700D need German keyboard. HB-F700F needs French keyboard. NMS8250/00 needs US international keyboard. NMS8250/16 needs Spanish keyboard.
-	USB hubs and USB keyboards with built in USB hub are currently not supported
-	Turn on the MSX without any floppy disk or cartridge inserted.
-	The NUMLOCK indicator on the keyboard should turn on now to indicate correct connection.
-	Make sure the computer enters the BASIC screen.
-	Now you can select the language of the MSX machine. This is required to make the extra function keys and helppage working properly. For Spanish machines it also enables character translation because the Spanish USB keyboard layout is much different from the original Spanish MSX layout.
- CTRL+ALT+F1 : Dutch / International
- CTRL+ALT+F2 : German
- CTRL+ALT+F3 : French
- CTRL+ALT+F4 : Spanish
- CTRL+ALT+F5 : Japanish

-	Check if the keyboard works properly now by doing some typing. Press F12 to check if the helppage is shown properly. Press ESC to stop the auto typing.
-	The current keyboard setting can be stored in FLASH now by pressing CTRL+ALT+S.
-	Extra function keys are available, see below.
-	For debugging purposes a USB keycode debugger and keyboard matrix monitor can be started, see below.
-	When everything works as expected you can insert floppy disks and cartridges again and try some games or other software.

Firmware update:

From version 2.00 and up the firmware for Philips and Sony interfaces is the same.

Latest firmware (.uf2 files) can be found here: https://github.com/jeroentaverne/msx_keyboard_interface

-	Make sure you received or downloaded a .uf2 file from this github page. Never use any other .uf2 file!
-	Turn off the MSX.
-	Disconnect the USB keyboard.
-	Remove the interface from the MSX.
-	Connect the interface to a PC or Mac machine using a standard micro USB cable.
-	A USB drive should be installed and become visible.
-	Copy /drag the .uf2 file to the USB drive.
-	The update will take place and will only takes a few seconds.
-	After the update the USB drive will disappear.
-	Disconnect the interface from the micro USB cable.
-	Follow above setup steps again.

Extra keys:

- F6: files
- F7: load
- F8: _system
- F9: lprint
- F10: _format
- F11: screen 0:width 80:color 15,1,1
- F12: show help page
- shift+F6: dir
- shift+F7: copy
- shift+F8: basic
- shift+F9: set screen
- shift+F10: _format
- shift+F11: none at the moment
- shift+F12: show version

- Key before the “1” key : Most right key on the third row
- Most right key on the third row : Most right key on the first row
- SCROLL LOCK key : SELECT key
- PAUSE key : STOP key
- END key : CTRL+N key (go to end of line)
- Left CTRL key : CTRL key
- Left ALT key : GRAPH key
- Right ALT key : CODE key
- Right CTRL key : “DEAD” key before or after right shift key
- Windows keys : SPACE key for shooting/jumping in games
- CTRL+ALT+F1 : set US/NL machine
- CTRL+ALT+F2 : set German machine
- CTRL+ALT+F3 : set French machine
- CTRL+ALT+F4 : set Spanish machine
- CTRL+ALT+F5 : set Japanish machine
- CTRL+ALT+L : show current layout without and with shift
- CTRL+ALT+D : start USB keycode debugger
- CTRL+ALT+M : start keyboard matrix monitor
- CTRL+ALT+S : store settings in FLASH
- CTRL+ALT+R : retrieve settings from FLASH

Tested with:

- Multiple wired Apple keyboards
- Multiple USB hubs
- Motospeed mechanical RGB keyboard (no ghosting)
- Battletron mechanical RGB keyboard (no ghosting) (sold by Action)
- Logitech G105 gaming keyboard (no ghosting)
- Logitech wireless keyboard with Unifying receiver
- Lenovo EKB-536A
- Logitech K120
- Microsoft wired keyboard 400
- Sweex KB060US
- DELL SK-8115
- Konig CSKMCU100US
- Razor Black Widow
- CoolerMaster MASTERKEYS MK750
