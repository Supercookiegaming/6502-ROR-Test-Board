# 6502-ROR-Test-Board

The 6502 ROR Test Board is a simple computer that tests if the ROR insruction is present on the 6502. I/O space is from 0x0000 to 0x7FFF. Rom space starts at 0x8000 and ends at 0xFFFF. The LED is tied to bit 7 and is set when the CPU R/W is low (writing). The data is then latched into the D-Latch and will be held until updated. The Yes ROR LED is turned on when the cpu writes to any memeory in the I/O space and bit 7 is high, all other bits do nothing. The No ROR LED is turned on whent he cpu writes to any memeory in the I/O space and bit 7 is low.
![alt text][logo]

[logo]: https://github.com/Supercookiegaming/6502-ROR-Test-Board/blob/main/Renders/3D/KiCad%209%203D%206502%20ROR%20Test%20Board%20Render%20V2.0T.png
I used https://www.masswerk.at/6502/assembler.html to assemble the rom code and create a BIN file. When using https://www.masswerk.at/6502/# to emulate the board, use the code marked as "Emulator". When the ROR bug is enabled 0x0010 will be 00 and when it is disabled 0x0010 will be 80.

When Building your own board its best to use sockets.

V2.0S uses mostly SMD parts (mostly 0603). V2.0T only has through hole components. 

EasyEDA and KiCad 9 files are now available for both boards. 

The design is free for personally use only.

V2.0S and V2.0T both now support zif sockets for the 6502 and AT28C256, the imporved reset circuit design, ground M3 mounting points, and better silkscreen instructions and pinouts.
