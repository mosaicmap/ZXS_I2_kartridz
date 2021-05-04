# ZXS_I2_kartridz

Simple ROM cartridge for [Sinclair ZX Interface 2](https://en.wikipedia.org/wiki/ZX_Interface_2).

**This is basically updated Droy's [ZX Cart](http://trastero.speccy.org/cosas/droy/cartuchos/cartuchos_s.htm)**. My version contains an EEPROM chip **W27C512** instead of the 27\*128 or 27\*256. The main reason is that the W27C512 is more common and cheaper than 27\*128 and 27\*256 chips nowadays (Search for W27C512 on eBay...) W27C512 has also a bigger capacity. One cartridge can hold up to four 16 KiB ROM banks. Of course, only one ROM file can be active at one time.  

![photo_with_case](images/ZXS_I2_kartridz_photo_w_case.jpg)


## Notes 

A HW programmer is required for uploading the ROM file to the EEPROM chip. For example, a relatively cheap universal programmer *MiniPro TL866CS* or *MiniPro TL866 II* from eBay is sufficient. Another option may be a homemade EEPROM programmer made of an Arduino; check for example [eeprom_programmer by StormTrooper](https://github.com/StormTrooper/eeprom_programmer) and similar projects.

To simplify ROMs upload it is possible concat four ROM files to a single file. Command under Linux/Unix: ``cat 1.rom 2.rom 3.rom 4.rom > myCompilation.rom``; under Windows/MS-DOS: ``copy /b 1.rom + 2.rom + 3.rom + 4.rom myCompilation.rom``

Jumpers A14 and A15 decide which 16 KiB ROM bank is active. (A14 and A15 are address pins of the W27C512, not A14 and A15 of the ZX Spectrum Edge connector)

This is only a simple ROM cartridge for 16 KiB ROMs. If you want a better cartridge, check for example sophisticated [Paul Farrow's ZXC4 cartridge](http://www.fruitcake.plus.com/Sinclair/Interface2/Cartridges/Interface2_RC_ZXC4.htm)


## EAGLE project

The project contains: schematic ``ZXS_I2_kartridz.sch`` and board ``ZXS_I2_kartridz.brd``. Also ``lbr/zxs_i2_rom_edge_connector.lbr`` is required.

It was created with a freeware version of Autodesk EAGLE.

![screenshot-schematic](images/ZXS_I2_kartridz_27512_schematic.png)

![screenshot-pcb](images/ZXS_I2_kartridz_27512_pcb.png)



## ROMs

See nice [overview by Paul Farrow](http://www.fruitcake.plus.com/Sinclair/Interface2/Cartridges/Interface2_RC_Cartridges.htm)

### Officialy released games (1984)

Originaly was released only 10 games. Namely:

- Backgammon
- Cookie
- Chess
- Horace and the Spiders
- Hungry Horace
- Jetpac
- Planetoids
- PSSST
- Space Raiders
- Tranz Am

You can download all ROM files of these games as [archive carts.zip](http://trastero.speccy.org/cosas/droy/cartuchos/carts.zip)


### Unreleased prototypes (cancelled)

- Popeye
- Q*Bert
- Gyruss
- Star Wars - The Arcade Game
- Return of the Jedi - Death Star Battle
- Loco Motion
- Montezuma's Revenge


### Sinclair BASIC for ZX Spectrum (1982) 


### Alternative BASIC interpreters

- OpenSE BASIC (mirrors: [worldofspectrum](https://worldofspectrum.org/archive/software/utilities/opense-basic-andrew-s-owen), [spectrumcomputing](https://spectrumcomputing.co.uk/entry/27510/ZX-Spectrum/OpenSE_BASIC))
- Gosh Woderful BASIC by Geoff Wearmouth ([mirror](https://8bit.yarek.pl/upgrade/zx.roms/gw03.zip))
- [Busy Soft ROM](https://busy.speccy.cz/tvorba/zxromky.htm)
- [prettybasic](https://github.com/reclaimed/prettybasic)
- ...


### Diagnostics 

Very useful ROMs for testing hardware of the ZX Spectrum.

- [Retroleum Diag ROM](http://blog.retroleum.co.uk/smart.zip) 
- [ZX-Diagnostics ROM by Brendan Alford](https://github.com/brendanalford/zx-diagnostics/releases)


### Experimental games

- DeathStar (8 KiB) (See [on fruitcake.plus.com](http://www.fruitcake.plus.com/Sinclair/Interface2/Cartridges/Interface2_RC_New_3rdParty_DeathStar.htm))





