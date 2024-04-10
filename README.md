# Dr. Mario (NES) Input Fixes

https://www.romhacking.net/hacks/8200/
https://github.com/TakuikaNinja/dr-mario-input-fixes

Dr. Mario has issues regarding its controller polling routine, which cause nasty bugs.
This hack fixes the input polling routine to address the following bugs:
- Big combo glitch - Large combos will no longer cause freezes, crashes, or other odd behaviour.
- Input corruption - DPCM samples (i.e. the drum sounds) will no longer interfere with controller inputs.

The controller polling routine now rereads one controller at a time, a method used in Super Mario Bros. 3 and many other games.
This reduces the likelihood of false negatives compared to rereading two controllers and the expansion port at the same time. 
The routine now uses the stack for temporary values instead of using conflicting zeropage variables.

This hack is based on: https://github.com/Nostaljipi/dr-mario-disassembly

## Original README

This is a disassembly of Dr. Mario for the Nintendo Entertainment System.

It builds Dr. Mario (Japan, USA) (Rev A).nes using ASM6f (https://github.com/freem/asm6f).

Thanks to Sour, author of the excellent NES emulator Mesen (https://www.mesen.ca/), which debug options were vital to this project.

Also, thanks to all contributors of the Dr.Mario articles at Data Crystal (https://datacrystal.romhacking.net/wiki/Dr._Mario) and The Cutting Room Floor (https://tcrf.net/Dr._Mario_(NES)).
