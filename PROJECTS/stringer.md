# Stringer Word Processor
## A low-tech digital word processing unit

Stringer is a small form factor computer purpose built for offline writing, local hosting and sometimes serving.

### Why? 

#### Dedicated Tool

Common computers are sophisticated multitasking devices that threaten to distract us. Writing requires deep focus without the siren call of media consumption. A dedicated writing device and environment is a cathartic reprieve from our overstimulated minds. Distraction free writing tools are popular for this reason.

#### Legacy Tool

Complex and proprietary systems are difficult to repair and E-Waste is an ever-growing issue. This can be remedied through considerate design. Building a task specific tool that is built simply, physically robust, reliable and highly repairable keeps it away from the trash.

#### Offline & Secure

There are commercial writing devices that offer a reliable distraction free experience. However, they lack some fundamental functionality that stringer would provide, that is customizability, openness and the ability to function offline.

### Project Status

The unit is currently in the intermediate design stages. I am gathering gathering 

---

### Project Outline

This projects seeks to create a hardware device constructed from robust, high reliability modular components and free & open software. The unit will be fully self contained 'All-in-one' design requiring a single charging/data cable much like an Imac. The unit can be connected to an external keyboard/mouse to create a standalone writing station and/or be plugged into power/network to serve documents on a network. This design will emphasize long term off-grid useage by being capable of running offline and connecting to renewable energy sources, perfect for a writer living in the courntryside. 

### User Stories

TBA

### Project build requirements

* A lower power draw Single Board Computer (SBC)
* A lower power draw display (E-ink or Small LCD)
* Uninteruptable power supply (UPS)
* Capability of running, charging and transferring data through a single cable.
* The electronic assembly will be built into a single rectangular hinged or magnetized wooden box.
* The unit will have multiple removeable backup disks that periodically copy folder contents.
* The unit will be ruggedized to endure long term use and neglect.

### Project software requirements

* Barebones operating system with power useage optimizations Possible candidate operating systems are Diet Pi, Alpine Linux, and Nix OS
* Minimal Desktop environment (i3 or DWM?)
* Minimal Terminal (Suckless ST or Alacritty)
* Terminal Multiplexor (TMUX)
* Minimal Text Editor (VIM 9) with GOYO, LimeLight, VIM-PENCIL, Proselint, Ale. [Great Resource](https://github.com/MiragianCycle)
* ZSH specially configured for writing and GIT (If/When online).
* SHELL & RSYNC for automated folder backups to removeable disks.

---

## Project Notes:

## Comparables:

https://hackaday.com/2020/06/09/teardown-the-writer-word-processor/
https://yarh.io/

