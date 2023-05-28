Tiny486:  An AMD Élan-based handheld 486.
===

Description
---

The goal of this project is to learn about PC architecture, and to successfully implement a 486-class PC using an AMD Élan System on a Chip.  This drastically reduces the number of required ICs for a basic PC implementation while still providing an understanding of PC architecture and peripherals.  The final product should be a handheld PC / SBC that is ideal for VGA DOS games, including a 640x480 LCD, Sound Blaster Pro 2.0 compatible sound and OPL3, 16MB of RAM, and CompactFlash-based storage with an external floppy connector.  

Initial Prototype
---

The initial prototype of this project is designed to be simple, to get a feel for the project and how to use the Élan.  It will include the SoC, VESA Local Bus VGA, Sound, Serial, Parallel, and CF support.  No Super IO chip is being used for the prototype, and therefore there will be no floppy support.  Address decoding for port 80h LEDs and IDE will be done with a CPLD, and an ATTiny MCU will be used to convert PS/2 keyboard protocol into XT protocol for use with the internal keyboard controller on the SoC.

Component Selection
---

| Function | Part Number | Description | Documentation |
|----------|-------------|-------------|-----------|
| SoC | SC410-100AC | AMD Élan 486SX SOC @ 100MHz | [Datasheet](https://raw.githubusercontent.com/Ilikemining1/Tiny486/main/Datasheets/21028.pdf), [Evaluation Board](https://raw.githubusercontent.com/Ilikemining1/Tiny486/main/Datasheets/21906.pdf), [Register Details](https://raw.githubusercontent.com/Ilikemining1/Tiny486/main/Datasheets/21032.pdf), and [User Manual](https://raw.githubusercontent.com/Ilikemining1/Tiny486/main/Datasheets/21030.pdf) |
| VGA | F65545-B2 | Chips 65545 VGA Controller | [Datasheet](https://raw.githubusercontent.com/Ilikemining1/Tiny486/main/Datasheets/f65545.pdf) |
| Sound (Primary) | CS4236B-JQ | Crystal CS4236B Single Chip Audio | [Datasheet](https://raw.githubusercontent.com/Ilikemining1/Tiny486/main/Datasheets/cs4236b.pdf) |
| Sound (Secondary) | YMF262-M | Yamaha YMF262 OPL3 FM Synth | [Datasheet](https://raw.githubusercontent.com/Ilikemining1/Tiny486/main/Datasheets/ymf262.pdf) |
| DRAM | K4E641612B or MT4LC4M16R6 | 4M x 16 4K Refresh EDO DRAM | [Datasheet](https://raw.githubusercontent.com/Ilikemining1/Tiny486/main/Datasheets/K4E661612B.PDF) |
