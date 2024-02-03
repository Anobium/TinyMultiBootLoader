For the legacy firmware see TinyMultiBootloader_Public_Firmwares.zip

For the latest supported firmware see https://sourceforge.net/p/tinypicbootload/discussion/general/thread/f3aa222fa2/#e087







v0.12.x (sept 2020)
-------------------
PC Software:
* Removal of USB suppprt
* Add HEF/SAF suppoer
* Add intra-byte delay
* Add PICKitPlus as programmer option  12.5
* UI clean up and language correction  12.5
* Added draft Help  12.6




v0.11.2 (mar 2018):
-------------------
PC Software:
* Support for USB
* Massive UI clean up and language correction

v0.11.0 (may 2016):
-------------------
PC Software:
* Project now uses "Visual Studio Express 2012"
* added: "firmware" tab for firmware infos (firmware folder, internal/external clock, default Bauds, default RX and TX pins...) and for programming PIC firmware (only) with Microchip's programmers (PicKit3, Real Ice, ICD3, PM3 and PKOB–"PICkit on board") and IPECMD software (Microchip/MPLABX/v3.30/docs/Readme for IPECMD.htm) directly from TinyMultiBootloader+ interface.
* added: in "firmware" tab, the user is able to select "firmwares" folder (by default it is in the same folder than "TinyMultiBootloader+.exe")
* added: in "firmware" tab, display firmware's device info when the firmware is selected by it's brand, device and then firmware's flavour (if more than one)
* added: in "firmware" tab, the user is able to define where is the "ipecmd.exe" file utilized to flash the PIC device
* added: in "firmware" tab, with your PIC programmer you can flash the PIC device with the selected firmware

Firmwares folder:
* added "firmwares.ini" file which store all informations about firmwares that will be diplayed in the new "firmwares" tab of the PC software.

Docs:
* changed "summary.html" with the one (bug free) of Dan.


v0.10.0 (febuary 2015):
-----------------------
"piccode.ini":
* added the new TI MPS430 family.
* added the new 8051 family.
* modifications relative to type D family $12, $13, $14, $15 (2014.08.01 Dan's message: http://sourceforge.net/p/tinypicbootload/discussion/devices/thread/e3e646c0/).
* modifications relative to type C family $6D, $6E, $6F and $30 ($31 deleted) (http://sourceforge.net/p/tinypicbootload/discussion/bug/thread/47493507/)


Docs / Web site:
* "Tested compilers: TI" page added
* "Tested devices: TI" page added
* "TI MPS430" page added
* "Tested compilers: 8051" page added
* "Tested devices: 8051" page added
* "Silicon Labs C8051" page added
* "Tested compilers: Microchip PIC" page modified: SourceBoost - BoostC compiler added
* "Using PC software" page modified: upsate of the command line documentation
* "Tested Devices: Microchip PIC" page modified: added note from Dan posted on 2014.02.06 (http://sourceforge.net/p/tinypicbootload/discussion/general/thread/f759f79b/)
* "Tested Devices: Microchip PIC" updated: added new devices
* "Firmwares: Microchip PIC10", "PIC12", "PIC16" pages modified: "Loading firmware from PC app, wo/ changing RESET vector" section added (http://sourceforge.net/p/tinypicbootload/discussion/help/thread/645cfea2/)
* "Firmwares: Microchip PIC10", "PIC12", "PIC16", "PIC18", "PIC18J" pages modified: how to generate absolute code (and not relocatable code) for modified bootloaders
* Changed screenshots

PC Software:
* changed program name from "Tiny_PIC-AVR_Bootloader+" to "TinyMultiBootloader+"
* bug fix by Danny ON4CLU: if there is no COM port connected to the computer, there is no more error at startup.
* bug fix: if "Force use of "piccodes.ini" file" is checked or unchecked in the "configuration" tab, then there is no more need to restart the program to take it into account.
* bug fix: if "auto" command line parameter is passed with no COM attached to the PC, then there is no more crash.
* new "4" family for TI MPS430 devices, from Dan
* new "5" family for 8051 devices, from Dan
* removed: Help by clicking on [?(F1)] button, or by pressing "F1" key.
* added: Help Messages Tooltips (can be desactivated with the "Show Help Messages" option).
* added: "configuration" tab
* some elements of the "Debug" tab have moved to the new "Configuration" tab.
* added: DTR hadware reset option (utilised by Dan)
* added: picture in "configure" tab to explain RTS true and false times.
* added: link to the online documentation (http://tinypicbootload.sourceforge.net/)
* added: link to the online tested devices pages
* change caption of the "Write Device" button to "Simulate" if "virtual device" is checked in the "debug tab". This can avoid some unexplicable untransferred programs ;-)
* added: "remote signal software reset" option (asked by Mark): a user selectable string (configured by entering the ascii codes separated by spaces in the "Remote Reset Signal" groupbox in the Configure" tab) will be sent, so your application (not the bootloader) receives the "remote message" and reboots the device.
* command line: seek the baudrate given in arguments in the "Baud Rate" list box and not only in a predefined list (because user can add personal values in the "Baud Rate" list box)
* command line (asked by Anobium): added "exit" option, it close TinyBootloader ONLY in case of a successfull write.

v0.9.1 (december 2014):
-----------------------
*  test purpose only for "remote signal software reset" option asked by Mark

v0.9.0 (july 2014):
-------------------
"piccode.ini":
* modifications relative to type B family (2014-06-11 Dan's message: http://sourceforge.net/p/tinypicbootload/discussion/devices/thread/803271db/?limit=25#a67c).

Docs / Web site:
* Web site now uses frames
* "Tested compilers: NXP ARM" page added
* "Tested devices: NXP ARM" page added
* "PIC18J" page added
* "Microchip 16-bit PIC MCU" page added
* "PIC24" page's name modified to "Type "D""
* "dsPIC" page's name modified to "Type "E""
* "NXP ARM Cortex-M0" page added
* "About" page modified
* description of data transfer formats (from Dan) added in PIC10, PIC12, PIC16, PIC18, PIC18J, 16-bit PIC Type"D" and Type "E" pages
* difference between "D" and "E" type explained (from Dan) in "Microchip 16-bit PIC MCU" page
* "Tested Devices: PIC" updated.

PC Software:
* new "D" family for dsPIC30F, PIC24F, PIC24FV, PIC24HJ, PIC24E(Partial), dsPIC33F(Partial), dsPIC33E(Partial) devices, from Dan (Thanks a lot Dan!)
* new "E" family for PIC24FJ, PIC24E(Partial), dsPIC33F(Partial), dsPIC33E(Partial) devices, from Dan
   Remark : Distinction of the E-type and D-type = Relationship with the E-type and D-type is similar to the relationship of PIC18J and PIC18. "Flash Config Words" does not exist in the D-type.
            look at http://sourceforge.net/p/tinypicbootload/discussion/general/thread/dd60ff68/
* new "3" family for NXP ARM Cortex-M0/0+ LPC devices, from Dan
* in "checkHex" function, added some warnings during check hex file (and then return true):
    - for PIC24, dsPIC30 and dsPIC33: not verified
    - for NPX: not verified
    - for enhanced PIC16: can't tell if it's PIC18 or enhanced PIC16
* bug fix: if "config.ini" is a read-only file or is in a read-only folder there is no more error, instead a message is displayed.

TODO:
* bug fix: if there is no COM port the computer, there is no more error.
* help for "erase EEPROM" and "special baud rates"
* bug fix: if enhanced PIC16 family hex file has configuration bytes, EEPROM data, or User ID, it is no more detected as PIC18 family.
* command line: wildcard caracters can be used in file name


v0.8.3.1 (febuary 2014):
------------------------
ATtiny firmwares:
* update ATtiny13A-44A-85-861A

PIC10-12-16-18 firmwares:
* update PIC10F322
* new firmwares (beta) PIC12F1571-1572-1612 from Dan
* update of PIC12F617-752-1822-1840-1501
* new firmwares (beta) PIC16F1613 from Dan
* new firmwares projects PIC16F87-872-873-873A-887-1827 from Dan
* new firmwares PIC16F88-870-871-874-874A-876-876A-877-877A-882-883-884-886 from Dan
* update of PIC16F720-819-1455-1507-1508-1782-1823-1933
* update of PIC16F720-721-753-819-1454-1455-1459-1503-1507
* update of PIC16F1508-1509-1512-1513-1516-1517-1518-1519-1526-1527
* update of PIC16F1782-1783-1784-1786-1787-1788-1789
* update of PIC16F1823-1824-1825-1826-1827-1828-1829-1847
* new firmware for PIC18F1330

PIC32 fimwares:
* USB version: added firmware "PIC32MXxxxF512L_Virtual_COM_Install_Firmware.hex" just for the PC driver installation (look at "http://tinypicbootload.sourceforge.net/modify_pic32_firmwares.html" page)

Docs / Web site:
* "About" page modified.
* PIC18F1330 device added to "Tested Devices: PIC" page.
* In "Firmwares: PIC32" page, use of USB firmware explained.
* "Tested Devices: PIC" updated.
* "Tested Compilers: PIC" updated.

PC Software:
* bug fix: handle bug from Great Cow Basic generation ".hex" file -> number of configuration bytes are in excess
* bug fix: configuration bytes write for PIC32 is disabled, because it doesn't work fine for the moment (thanks to Davide Spazian)
* bug fix: in some conditions, 0x00 can be stuck in serial buffer. Now erase serial buffer before listening microcontroller (bug report: donvukovic / bug fix: Dan)

v0.8.3 (december 2013):
----------------------

Docs / Web site:
* Added in the "Tested PIC Compilers" page, "JALv2" tips to get it works with TinyBootloader+ (from Sunish).
* Added in the "Tested PIC Compilers" page, "PIC18 assembler" tips to get it works with TinyBootloader+ (from Dan).

PC Software:
* re-enable "RTS False" time in the debug tab. From Sunish's bug report:
    "RTS reset false (ms) option should be enabled in the form. If the software starts sending 0xC1 PIC will not respond correctly if there is no delay between rts = true and rts = false.
     With 12f1840 I found 500 and 100 to be ideal."
* changed some typo mistakes (thanks to Sunish).
* bug fix: program hang no more when programming full EEPROM memory on PIC16 family (Dan).
* modifications in "piccodes.ini" relative to size changes of some PIC and ATtiny firmwares.

Utilities:
* Dan made hte possibility to update the bootloader without the need of a programmer.
  Look in "utlities/update_bootloader_without_programmer" folder.

TODO:
* help for "erase EEPROM" and "special baud rates"
* bug fix: if enhanced PIC16 family hex file has configuration bytes, EEPROM data, or User ID, it is no more detected as PIC18 family.
* command line: wildcard caracters can be used in file name
* PIC24 family
* dsPIC family

v0.8.2 (october 2013):
----------------------


v0.8.1 (september 2013):
------------------------

PC Software:
* added Config Bytes write for PIC18 family (for the moment, just some firmwares can handle this option - look at http://tinypicbootload.sourceforge.net/tested_devices_pic.html)
* added the possibility to manually enter weird "baud rates" (like 111456) in order to adapt the baud rate to the new PIC speed (if modified by the Config Bytes Write)
* in debug tab a "special baud rates" group was added to calculate weird baud rates as a fonction of old baudrate, old and new PIC frequencies. This calculated baudrate is automatically added to the "Baud Rate" combobox.
* 'added baudrates to the "Baud Rate" combobox' are saved in "config.ini"
* progress bar display modification: restart from 0 at each new process (e.g. EEPROM write, Boot Flash write, Program Flash write, etc...)
* changed "config.ini" loading process in order to keep new versions of "TinyBootloader+" compatibles with older "config.ini".
* added "Erase EEPROM" option
* bug fix: only write the EEPROM bytes which are present in the "hex" file. Now, leave other data in EEPROM untouched
* bug fix: write EEPROM byte even if it equals 0xFF
* bug fix: for PIC16 normal and enhanced families, if there are "User ID" bytes in hex file they will be discarded (not written) instead of displaying "Error: hex file too large, writing bootloader firmware!!!".
* bug fix: some PIC16 hex files aren't detected as PIC18 ones anymore.

v0.8.0 (july 2013):
-------------------


PC Software:
* Atmel AVR ATmega devices are now supported (by Dan)!
* family for AVR ATtiny changed from "#A" to "1"
* changed device answer type. Instead of "0xID_device 0x4B" it's now "0xID_device 0xASCII(upper_case_Family_code)".
    By this way we could have 256 different devices in every family, and not 256 for the whole families.
    Old firmwares are still compatibles with this new device answer type.
* added "family" text box for virtual device in debug tab.
* modifications in "config.ini" to keep trace of modification for virtual device in debug tab.
   !!! previous version of "config.ini" file is no more compatible with "Tiny AVR/PIC Bootloader+ v0.7.1"
    (you just have to erase it, it will be created automaticaly the next time you'll use "Tiny PIC Bootloader+")!!!
* added Help by clicking on [?(F1)] button, or by pressing "F1" key, then click on a control to display its function.
* added "Online Support" link to the forum
* modifications in "piccodes.ini" relative to AVR families.

v0.7.1 (july 2013):
-------------------

PIC32MX3xx_to_7xx Firmware:
* release of a USB CDC (RS232 emulation with USB) version of the firmware for USB capable devices. Beware this version is very huge (24kB) if compared to UART version (4kB). With full compiler optimizations, it can be 16kB.
As at startup virtual COM will be available for only 1 seconde, the best way to get its number is to use [Search COM] in "Tiny AVR/PIC Bootloader+" and look at the new COM that has appeared.

PC Software:
* Drag & Drop allowed. If in the objects put on the application's window they are ".hex" or ".eep" (EEPROM for AVR) files then:
            - add the first one to "listHexFiles" list view and select it
            - write it to the device
* added in debug tab, displaying of raw data during communication with a device.
* can select if flash program memory must be programmed or not in the device (allow to write only EEPROM)
* modifications in "config.ini" to keep trace if flash program memory must be writen or not.
    !!! previous version of "config.ini" file is no more compatible with "Tiny AVR/PIC Bootloader+ v0.7.1"
    (you just have to erase it, it will be created automaticaly the next time you'll use "Tiny PIC Bootloader+")!!!
* can open EEP (EEPROM file for AVR) or HEX files. If EEP file is choosen, the program will try to search the corresponding HEX file.
* bug fix: .EEP file wrongly displayed when "show hex file during transfert" is checked

v0.7.0.2 (july 2013):
--------------------

PC Software:
* bug fix: for PIC18 family, if there are "User ID" bytes in hex file they will be discarded (not written) instead of displaying "Error: hex file too large, writing bootloader firmware!!!".
* bug fix: when in "Debug" tab "Show answer during [Check Device]" is checked, now display answer even when only 1 byte is received.
* now [Check Device] is not stopped by a not opened COM (could be usefull if COM is only available during the test but not at its start)
* modifications in "piccodes.ini" relative to changed firmware.

v0.7.0.1 (july 2013):
--------------------

PC Software:
* modifications in "piccodes.ini" relative to changed and new firmwares.

v0.7.0 (july 2013): "Tiny Pic Bootloader+" is now "Tiny AVR/PIC bootloader+"
--------------------

Docs / Web site:
* Added "AVR Tested devices" page.


v0.6.5.1 (may 2013):
--------------------


v0.6.5 (may 2013):
--------------------

Docs / Web site:
* "Tested devices" page updated.


PC Software:
* modifications in "transfertHexToArray" to handle some PIC12 and PIC16 with Configuration words at 0x8007 and not at 0x2007.
* added EEPROM write for normal (e.g. PIC16F874A, PIC16F886, etc) and enhanced (e.g. PIC12F1840, PIC16F1823, etc) midrange families.
* added EEPROM write for PIC18 family (unlike original version, works even if EEPROM > 256 bytes).
    !!! previous firmwares of PIC18 devices aren't compatible with "Tiny PIC Bootloader+" EEPROM write
    (you must use PIC18 firmwares' sources from the archive of "Tiny Pic Bootloader+" >= v0.6.5) !!!
  If you don't need EEPROM write, then old PIC18 firmwares can still be used with "Tiny Pic Bootloader+" >= v0.6.5
* added the possibility to use a virtual PIC device (only usefull for PC software developpers).
* modifications in "config.ini" to keep trace of the virtual PIC.
    !!! previous version of "config.ini" file is no more compatible with "Tiny PIC Bootloader+ v0.6.5"
    (you just have to erase it, it will be created automaticaly the next time you'll use "Tiny PIC Bootloader+")!!!
* added "Abort" button to interrupt the current operation (i.e. auto conf com, write or check pic).
* modification in "auto COM conf" algorithm: at first try the latest COM and Baudrate configuration used.
* added "auto" option in command line, in order to have automatic COM configuration even with command line:
       tinypicbootloader+.exe "c:\folder 1\folder etc\file name.hex" [COMx [BaudRate]|auto])
  example: tinypicbootloader+.exe "c:\test file.hex" auto
* modification of "piccodes.ini" for the many new midrange devices added.

v0.6.4 (may 2013):
--------------------

Docs / Web site:
* changed web site layout.
* "Quickstart" page complete.

PC Software:
* command line: added COMnum and baudrate.
  syntax:
    tinypicbootloader+.exe "c:\folder 1\folder etc\file name.hex" [COMx [BaudRate]]
  If 'COMx' or 'BaudRate' aren't passed in arguments, the previuos option used in the GUI (stored in the "config.ini" file) will be used.
  Examples: tinypicbootloader+.exe "c:\test file.hex" COM8 9600
            tinypicbootloader+.exe "c:\test file.hex" com8
            tinypicbootloader+.exe "c:\test file.hex"
* RS232 power supply (based on Dan's idea and schematic): DTR and RTS can be used to power the PIC device directly with RS232 port (only during programming!!!). These options are in the debug tab.
     Schematic for use this capacity is given in "Tiny PIC Bootloader +" web site:
          http://tinypicbootload.sourceforge.net/hardware_connection.html
     Note: As the PIC device is only powered during programming, then it works as automatic reset.
* modifications in "config.ini" to keep trace of DTR/RTS powering.
     !!! previous version of "config.ini" file is no more compatible with "Tiny PIC Bootloader+ v0.6.4" (you just have to erase it, it will be created automaticaly the next time you'll use "Tiny PIC Bootloader+")!!!
* modification for PIC16F88 in "piccodes.ini":
      $33, B, 16F 88, $2000, $100, default, 64,

v0.6.3.1 (april 2013):
--------------------

Docs / Web site:
* "Hardware Connections" page complete.

PC Software:
* added IdTypePIC for PIC10F322 (100 words and 132 words) firmwares in "piccodes.ini"

v0.6.3 (april 2013):
--------------------

PC Software:
* modifications in "configureTransfert" function in 'B' family:
     assembly code changes for "goto bootloader_address" and memory page selection.
     Now it can handle different bootloader sizes (not only 100 words), and any max flash memory.

v0.6.2.1 (april 2013):
----------------------

PC Software:
* bug fix: code simplifications for PIC16Fxxx family in "hexToArray" function, was a very bad idea! Bootloader can't work anymore with this family! Use this new version if you use PIC16 devices!!!

v0.6.2 (april 2013):
--------------------

PC Software:
* "piccodes.ini" modified to add PIC16F874 and PIC16F877
* added some comments in code
* some code simplifications for PIC16Fxxx family in "hexToArray" function
* works even if the letter for PIC family in "piccodes.ini" is in upper or lower case
* every mumeric value in "piccodes.ini" can be in hexa (starting with '$') or in decimal (without '$')
* there is two new properties in "piccodes.ini": 'bootloader size' and 'transfert block size'.
    You SHOULD live then as 'default', but if you want to tweak the bootloader you can change them in accordance to your needs, at your own risks (you can erase the bootloader firmware in the device).
    !!! previous version of "piccodes.ini" file is no more compatible with "Tiny PIC Bootloader + v0.6.2" !!!

v0.6.1 (febuary 2013):
----------------------

PC Software:
* bug fix: works even if the ".hex" file is in upper or lower case.
* 'jump to bootloader' modification for ".hex" files generated by mikroC32.

v0.6 (january 2013):
--------------------

PC Software:
* PIC32MX3xx_to_7xx family (with normal ".ld" OR with special ".ld" for boot programs of Microchip HID Bootloader) (firmware must be >= v0.6)
* warning if size of hex to program can overwrite bootloader program (i.e. > (maxMemPos - bootloader size))
* bug fix: can transfer more than 64KB
* changed in "piccodesIniFile" and "configIniFile" path initialisation '\' to '/' for linux-mono portage compatibility
