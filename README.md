# HackTheElection
Firmware dumps and some notes from the Diebold AccuVote TSX at the voting machine hacking village at Defcon 25


## Files in this repository
### diebold
Firmware dump from the main storage. The folder contains the raw dump (reset.bin), the OpenOCD config files used (pxa255.cfg and um232h.cfg), and the results of running Binwalks extract tool (\_reset.bin.extracted)

### battery\_eeprom.bin
A dump of the 1024 bit (128 byte) eeprom near the pic at the bottom of the board. This contains the string "BQ2060A" which is a reference to the followign IC located just below the eeprom: http://www.ti.com/lit/ds/slus500d/slus500d.pdf

### modem\_eeprom.bin
A dump of the Atmel eeprom located on the removable modem board near the phone jack. As far as I can tell, this contains data for the Conexant SmartDAA modem on the same board. 
