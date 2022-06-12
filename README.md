# Marty

## Introduction

Marty is a cross-platform IBM PC emulator written in Rust. It should build on Windows, Linux and MacOS (Including M1)

### Why another PC emulator?

This was a hobby project to see if I could write an emulator from scratch. This was also my first project learning Rust, so please be kind.
I do not claim to be an expert in either emulators or Rust. 

This emulator is nowhere near cycle-accurate. It will not run the 8088mph demo anytime soon, but I do hope to improve accuracy over time.

## Requirements

Marty requires an original IBM PC 5150 BIOS ROM be placed in a /roms folder. I hope to support a free BIOS at some point which I can distribute or at least link to. In the meantime Google is your friend.

Place floppy images in a /floppy folder and Marty will find them on start-up. Floppy images up to 360k are supported.

## Features

Currently Marty will emulate an original IBM 5150 PC with a CGA card. 

The CGA emulation is nowhere near finished, but basic graphics and text modes are supported.

The PPI, PIC, PIT, DMA chips are all at least partially implemented, although most of them with the bare minimum features needed to boot
a few games and likely contain lots of bugs. 

The Floppy disk controller is implemented for read-only operation at the moment.

There is currently no sound.

Marty has a GUI with a few useful debugging displays including the current instruction disassembly, memory, and various internal chip states. 

## Missing features: (Planned)

* Complete CGA support including low res graphics modes and composite monitor simulation
* PC Speaker sound
* Writing to floppy and saving floppy images
* Better debugger and breakpoint system

## Known Issues

* Keyboard input is a bit spotty, possibly due to missed interrupts or bad timing.
* Only DOS 2.0 supported. DOS 3.0+ fails to boot.

## Wishlist features: (Maybe)

* Hard disk emulation
* EGA/VGA graphics
* Mouse support

## Probably never implementing:

* SVGA
* Soundblaster/Adlib sound
* 80286+ processors

## Screenshots
![tools](https://user-images.githubusercontent.com/7229541/173169915-58b0bb5f-663c-41de-be3c-66952297558e.png)

![cat](https://user-images.githubusercontent.com/7229541/173169921-32b5dbad-0cb7-4cfa-921f-09ba7f946e85.png)

![kq1](https://user-images.githubusercontent.com/7229541/173169927-a06d7c23-2611-4a7e-8fd9-244ec50c55d8.png)