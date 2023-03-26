# Stringer Word Processor
## A low-tech digital word processing unit

Stringer is a small form factor lo-tech computer purpose built for offline writing.

### Problems 

1. Common computers are sophisticated multitasking devices that threaten to distract us.
2. Complex and proprietary systems are difficult to repair or maintain creating E-Waste.
3. Most modern electronic devices are dependent on online connectivity and accounts.
4. Other writing devices do not provide modern macros and scripting capability.

### Project Outline

This projects seeks to create a hardware device constructed from robust, high reliability modular open hardware components in combination with free & open software.  

### Ideas

* Artisitc PCB's throughout (Edition Based)
* Sandwiched PCB construction with spacers, framed like a window. PCB slots into wooden frame
* Ortholinear keyboard with extensions on either side for many macro keys
* Grid of small tactile switches for macros (Saving, Battery Check, Reboot, Config files)
* Custom stringer config for os, wm, terminal, tmux, vim to suite the hardware and operational focus
* Easy deconstruction for repair
* Fully Open Schematics, Build notes, Scripts, Software configs
* Hosted Stringer image on site

### Project build requirements

* A lower power draw Single Board Computer (SBC)
* A lower power draw display (E-ink or Small LCD)
* Uninteruptable power supply (UPS)
* Capability of running, charging and transferring data through a single cable.
* The unit will have multiple disks in mirrored raid configuring.
* The unit will be ruggedized to endure long term use and neglect.

### Project software requirements

* Barebones operating system with power usage optimizations (Debian minimal, Nix OS)
* Minimal Desktop environment (i3, DWM, Awesome, )
* Minimal Terminal (Suckless ST, Alacritty, Kitty)
* Terminal Multiplexor (TMUX)
* Minimal Text Editor (VIM 9) with GOYO, LimeLight, VIM-PENCIL, Proselint, Ale. [Great Resource](https://github.com/MiragianCycle)
* ZSH specially configured for writing and GIT (If/When online).
* BTRFS. (Snapshotting, RAID, Error Correction)

---

## Project Notes:

## Comparables:

https://hackaday.com/2020/06/09/teardown-the-writer-word-processor/
https://yarh.io/

