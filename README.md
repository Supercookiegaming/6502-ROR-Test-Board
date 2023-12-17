# 6502-ROR-Test-Board

The 6502 ROR Test Board is a simple computer that tests if the ROR insruction is present on the 6502. I/O space is from 0x0000 to 0x7FFF. Rom space starts at 0x8000 and ends at 0xFFFF. The LED is tied to bit 7 and is set when the CPU R/W is low (writing). The data is then latched into the D-Latch and will be held until updated. The Yes ROR LED is turned on when the cpu writes to any memeory in the I/O space and bit 7 is high, all other bits do nothing. The No ROR LED is turned on whent he cpu writes to any memeory in the I/O space and bit 7 is low.

I used https://www.masswerk.at/6502/assembler.html to assemble the rom code and create a BIN file. 

When Building your own board its best to use sockets and preferably zif sockets for the 6502 and AT28C256.
