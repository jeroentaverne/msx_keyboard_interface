👋 Hi, I’m Jeroen Taverne

I have created an interface to connect a USB keyboard to a MSX computer, currently there are three versions:
- For Philips NMS8250, NMS8255 and NMS8280 with the 26 pin connector
- For Sony machines with the 13 pin keyboard connector like HB-F700, HB-F500, HB-F900
- For Viktor HC-90 and HC-95 with the 20 pin connector (no pictures yet)

It consists of a small box (3D printed) with internal small computer which reads the USB keycodes and simulates the keypresses on the keyboard matrix.

Extra features are added which are normally not possible with the real MSX keyboard.

With a gaming keyboard no ghosting is possible with this interface. Some non gaming keyboards don't allow pressing cursor keys and space button at the same time. Playing games like Nemesis or Quarth could couse issues. That's why the left and right windows keys can be used as space as well with this my keyboard interface. Also see this post: https://www.msx.org/forum/semi-msx-talk/emulation/bluemsx-24-25-keyboard-emulation

The firmware can be upgraded by connecting it to Windows/MAC/Linux using the micro USB connection. The firmware update is just drag and drop a file.

You can order it by sending me an email with the keyword MSX in the subject to: j.taverne@gmail.com
For support and feature requests you can also send me an email or post a message through github.

![alt text](https://github.com/jeroentaverne/msx_keyboard_interface/blob/main/photos/sony1.jpg)
![alt text](https://github.com/jeroentaverne/msx_keyboard_interface/blob/main/photos/sony3.jpg)
![alt text](https://github.com/jeroentaverne/msx_keyboard_interface/blob/main/photos/photo1.jpg)

MSX USB keyboard interface (firmware version 2.06 and higher)

WARNING: NEVER connect the interface or USB keyboard while the MSX is powered on!

Setup:

- The interface doesn't need external power, the micro USB connector stays disconnected during normal use.
- Insert the interface into the keyboard connector of the MSX. Make sure for the Philips/Viktor version the "TOP SIDE" text is pointing to the top.
- USB hubs and Apple keyboards can be used but results may vary.
- Turn on the MSX without any floppy disk or cartridge inserted.
- The NUMLOCK indicator on the keyboard should turn on now to indicate correct USB connection with the keyboard.
- Make sure the computer enters the BASIC screen.
- Now you can select the BIOS language of the MSX machine. This is required to get the extra function keys, help page and optional layout translation working properly.

	CTRL+ALT+F1 : US International BIOS (default)
	CTRL+ALT+F2 : German BIOS
	CTRL+ALT+F3 : French BIOS
	CTRL+ALT+F4 : Spanish BIOS
	CTRL+ALT+F5 : Japanese BIOS

- Optionally you can enable keyboard layout translation when the USB keyboard layout doesn't match the BIOS language. This way it's for instance possible to connect an US International keyboard to a German or Japanese MSX machine. This is disabled by default. Make sure the BIOS language is also set correctly.

	SHIFT+CTRL+ALT+F1 : US International USB keyboard
	SHIFT+CTRL+ALT+F2 : German USB keyboard
	SHIFT+CTRL+ALT+F3 : disable translation
	SHIFT+CTRL+ALT+F4 : disable translation
	SHIFT+CTRL+ALT+F5 : disable translation

- Check if the keyboard works properly now by doing some typing. Press F12 to check if the help page is shown properly. Press ESC to stop the automatic typing.
- The current settings can be stored in FLASH memory now by pressing CTRL+ALT+S.
- When everything works as expected you can insert floppy disks and cartridges again and try some games or other software.

Firmware update:

- First check the current version by pressing shift+F12. Never update with a lower version!
- New firmware (.uf2 files) can be found here: https://github.com/jeroentaverne/msx_keyboard_interface
- Never install any .uf2 file from an unknown source!
- Turn off the MSX.
- Disconnect the USB keyboard.
- Remove the interface from the MSX.
- Connect the interface to a PC or Mac machine using a standard micro USB cable.
- A USB drive should be installed and become visible in explorer or file manager.
- Copy or drag the .uf2 file to the USB drive.
- The update will take place and will only takes a few seconds.
- After the update the USB drive will disappear.
- Disconnect the interface from the micro USB cable.
- Follow above setup steps again.

Extra keys:

F6		: files
F7		: load
F8		: _system
F9		: lprint
F10		: _format
F11		: screen 0:width 80:color 15,1,1
F12		: show firmware version and help page
shift+F6	: dir
shift+F7	: copy
shift+F8	: basic
shift+F9	: set screen
shift+F10	: _format
shift+F11	: NA
shift+F12	: show firmware version

SCROLL LOCK key	: SELECT key
PAUSE/BREAK key	: STOP key
END key		: CTRL+N key (go to end of line)
Left CTRL key		: CTRL key
Left ALT key		: GRAPH key
Right ALT key		: CODE key
Right CTRL key		: “DEAD” key before or after right shift key
Windows keys		: SPACE key for shooting/jumping in games when no gaming keyboard is used
CTRL+ALT+SPACE 	: enable/disable auto fire (10Hz) on SPACE and Windows keys
CTRL+ALT+L		: show current layout without and with shift
CTRL+ALT+D		: start USB keycode debugger
CTRL+ALT+M		: start keyboard matrix monitor
CTRL+ALT+S		: store settings in FLASH
CTRL+ALT+R		: retrieve settings from FLASH

For orders and firmware change requests, please send me an email: j.taverne@gmail.com
