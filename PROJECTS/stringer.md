# Stringer Word Processor
## A low-tech digital word processing unit

Stringer is a small form factor computer purpose built for offline writing, local hosting and sometimes serving.

### Why? 

Common computers are expensive, complex, proprietary systems that are increasingly difficult to repair or upgrade. Furthermore, the user experience of modern operating systems are ever changing, highly distracting environments centered around web connectivity and media consumption. Writing for instance requires deep focus, familiar tools and high reliability.

E-Waste is an ever-growing issue that can be mitigated through considerate Design. building a task specific tool that is physically robust, built simply and highly repairable keeps it away from the trash.

Several commercialized products by hemingwrite/freewrite are well loved by writing enthusiasts.
The unit is currently in the intermediate design stages. 

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

* Barebones operating system with power useage optimizations (Diet Pi?) or (Alpine).
* Minimal Desktop environment (Suckless DWM?)
* Minimal Terminal (Suckless ST?)
* Minimal Text Editor (VIM 9) with GOYO, LimeLight, VIM-PENCIL, Proselint, Ale. [Great Resource](https://github.com/MiragianCycle)
* ZSH specially configured for writing and GIT (When online).
* SHELL & RSYNC for automated folder backups to removeable disks.

This is a tmux test on my remote dev box

---

## Project Notes:

[RSYNC tutorial video youtube](https://www.youtube.com/watch?v=Pygr_TpZRpM)

[Tutorial for compute module carrier board](https://www.digikey.com/en/maker/projects/creating-a-raspberry-pi-compute-module-4-cm4-carrier-board-in-kicad/7812da347e5e409aa28d59ea2aaea490)