# 1.1

# Linux Distributions

## Distribution Definition:

A distribution is a collection of software components that form a complete operating system. A Linux distribution consists of the following essential components:

* Linux Kernel: The foundation of the operating system, connecting the application layer to the hardware layer. Hardware is incorporated into the file hierarchy through the /dev and /sys directories, and process information is mapped in /proc.

* GNU Core Utilities: Basic file, shell, and text manipulation utilities of the GNU operating system. These utilities are expected to exist on every operating system.

* X Server (Optional): A display server for the X Windows system, a framework for a GUI environment. It is an architecture-agnostic framework for remote graphical user interfaces and input devices, designed to be used over network connections.

* Desktop Environment (Optional): A graphical interface that allows users to interact with the operating system using a mouse. Common Linux desktop environments include Gnome, KDE, Unity, Cinnamon, MATE, and Xfce.

The distribution release version can be found by running the command 

    lsb_release -a.

## Linux Kernel:

The Linux kernel is free and open-source software that serves as the core of the operating system. It is responsible for managing system resources and providing a layer of abstraction between the hardware and the software. To check the kernel version, use the command uname -r.

## GNU Core Utilities

The GNU Core Utilities are a collection of essential command-line tools that provide basic functionality for Linux systems. These utilities include common Unix tools like ls, cp, mv, and rm. To check the version of the GNU Core Utilities, use the command ls --version.

## X Server

The X Server is an optional component that provides a graphical environment for Linux systems. It allows users to run graphical applications and provides a framework for managing windows, mouse input, and other graphical elements. To check the version of the X Server, use the command sudo X -version (elevated permissions are required to run this command using sudo).

## Desktop Environment

A desktop environment is an optional component that provides a complete graphical interface for Linux systems. It includes a window manager, desktop icons, a file manager, and other tools for interacting with the system. Common desktop environments for Linux include Gnome, KDE, Unity, Cinnamon, MATE, and Xfce.

# Linux Embedded Systems

## Embedded System Definition:

A combination of hardware and software for a purpose.
- Application
- Libraries
- High-level Abastrations
- Networking/File Systems
- Low Level Interfaces
- Hardware

## Examples
- Android
- Raspberry Pi
- Smart TV's
- In Vehicle entertainment systems
- Networking equipment

# Linux in the Cloud

## The Cloud:
A collection of datacenters providing compute, storage and other software and services over the internet

- Regions
- Availability Zones
- Subnets

# 1.2

# Major Open Source Applications

# Desktop Applications

## Desktop Applications
Open source applications for the desktop and office use
- Office Applications
    - OpenOffice
        - Writer (word processer software)
        - Calc (spreadsheet software)
        - Impress (presentation software)
        - Draw (illistration software)
        - Base (datebase software)
        - Math (mathematical equation software)

    - LibreOffice (fork of OpenOffice)

- Web Browser
    - Firefox
- Mail Client
    - Thunderbird
- Image Editing
    - GIMP

# Development Languages

## Shell
- Shell scripts are designed to be run by the command line interpretor using various scripting languages.  
- Bash is the most common shell used in Linux

## C
- A general purpose programming language designed to be compiled to require minimal runtime support.
- C programs can be compiled to run on a large variety of computing platforms.

## Java
- Class based, object oriented general purpose programming language designed to compile and run on any system that supports the Java runtime.

## JavaScript
- HTML, CSS, and JavaScript make up the core technologies of the world wide web.

## Perl
- Orginially developed in 1987 to be general purpose UNIX scripting language
- Perl has become a high-level general purpose programming language 
- Perl supports both procedural and object oriented programming

## Python
- Interpreted general purpose programming language similar to Perl
- Python's source code is usually easier to read
- Python has extensive object oriented programming support

## PHP
- PHO Hypertext Processer was orginially designed for web development
- PHP code can be embedded into HTML

# Package Management Tools

## Package
- A collection of files needed to install an application

## Package Management 
- How installation packages are tracked and managed

# Debian Based Systems
- Debian 
- Ubuntu

## Dpkg
- Short for Debian package, is a package archive format that contains package metadata.  
- DEB files are package installation files for Debian based Linux distributions.
- Debian based systems that use dpkg files for package installation can take advantage of APT (Advanced Package Tool) for managing packages and their dependencies.
- To install a Dpkg package:
    - `sudo dpkg -i package_name`

- To uninstall a Dpkg package:
    - `sudo dpkg --remove application_name`

## apt-get
- Advanced Package Tool (APT) is a free and open source interface that works with core libraries to handle the installation and removal of software packages on Debian based systems
- APT automates the retrieval and validation of softwware packages as well as other dependancies.
- APT allows users to search for and install packages from repositories.
- Various GUI front-ends are available for with APT, such as Synaptic or Ubuntu Software Center.

# Red Hat Based Systems
- Red Hat
- Fedora
- CentOS
- SUSE

## RPM
- Red Hat Package Manager
- Red Hat Package Manager is widely used package management system
- Red Hat based systems that use .rpm files for package installation can take advantage of YUM for managing packages and their dependencies.
- To install a RPM package
    - `sudo rpm -i package_name`

- To uninstall a RPM package:
    - `sudo rpm -e application_name`

## yum
- Yellowdog Updater Modified
- Free and open source package management utility for RPM based systems
- YUM allows for automated updates and package dependancy management
- Fedora uses a rewrite of YUM named DNF


## Compiling from Source
1. Extract files
    - `tar xzf file_name`
2. `cd` into extracted file folder
    - `cd file_folder`
3. Configure the files using the `configure` script
    - `./configure`
4. Compile the source code
    - `make`
5. Install the binaries
    - `sudo make install`
6. Run the application
    - `application_name`
7. Uninstall the application
    - `sudo make uninstall`

# Server Applications

## Server Applications
Open source applications that provide client services.

- Web Server Applications
    - Apache
        - Apache allows web content to be served by a host and may use compiled modules to extend the core functionality of the service.

    - NGINX
        - Used for reverse proxy, load balancing, mail proxy and HTTP caching.
        - There are closed source components available the extend NGINX's functionality

- Database Server Applications
    - MySQL
        - Open-source relational database.
        - Together with Linux, Apache, and PHP/Perl/Python it makes up the LAMP stack

    - MariaDB
        - Fork of MySQL

- File Sharing Applications
    - Samba
        - Open source file sharing software that permits file sharing with Windows clients using Common Internet File System (CIFS)
        - Typically used on a local network - not over the internet
        - Samba performs:
            - File and Print services
            - Authentication and Authorization
            - Name Resolution
            - Service Announcements

    - NFS
        - NFS (Network File System) is a distributed file system protocol permitting client hosts to access file and directories over the network as local storage

- Private Cloud Applications
    - ownCloud
        - A client/server suite of applications for creating and using file hosting services.
        - Functionality is similar to dropbox, however the files are stored on your own connected hardware.
        - Enterprise features are not open-source

    - Nextcloud
        - Fork of ownCloud
        - All features are open-source

# 1.3

# Licensing

# Free Software Foundation (FSO)
# Open Source Initiative (OSI)

The Open Source Initiative and Free Software Foundation are two movements that place approvals on open-source licenses.

**Open Source Initiative**


**Free Software Foundation**
- Only supports free, pure open-source software.
- Software must guarantee the following four freedoms
    - Run the software any way you wish for any purpose
    - Study how the software works and modify it as you wish
    - Freedom to redistribute copies of the software
    - Freedom to redistribute copies of your modified version of the software
- The FSF considers any software that does not meet the above criteria to be non-free and unethical


**FOSS**
- Free and Open Source Software
- **Free** is a reference to the price of the software

**FLOSS**
- Free/Libre/Open Source Software
- **Free** is in reference to freedom

# Open-Source Licensing

## Open-source licensing models and Types
Open source licensing provides rules and guidelines for the work my be used, permitting others to contribute without first seeking permission

# Licensing Examples

## Public Domain
**CCO 1.0**
- Least Restrictive
- Creative Commons 1.0 Universal Public Domain Dedication is a declaration that all works are in the public domain.
- You can copy, modify, distribute and perform the work, even for commercial purposes, all without asking permission.

## Permissive
**BSD**
- Some Restrictions
- BSD Licenses are a segment of permissive software licenses with minimal restrictions imposed on usage and distribution.
- Redistributions of source must contain copyright license
- Redistributions of binary must contain copyright license
- All advertising materials mentioning features or use of this software must display the following acknowledgement:
    - This product includes software developed by the -organization-
- Neither the name of the -organization- nor the names of it's contributors may be used to endorse or promote products derived from this software without specific written permissions.


## Copyleft
**GPL**
- Most Restrictive
- Being a copyleft license, derivative work may only be distributed under the same license terms.
**This license permits**
- Commercial Use
- Modification
- Distribution

**Restricts**
- Sublicensing

**and must**
- Include the original work
- Stated changes

# Open-source Philosophy

## Philospophy
- The basic premise of open-source software is that source code is available for anyone to freely view, use, modify, or redistribute

## Forking
- When developers use the source code from one project to start and entirely new parallel project.

## Licensing
- **Permissive:**  No restrictions on licensing or derivative work
- **copyleft:**  Derivative work must use the same license as the original software

# 1.4

# ICT Skills

# Desktop Skills

## Popular Linux Desktops

**Lightweight Desktops**
- LXDE
- XFCE
- Mate

**Feature Rich Desktops**
- Cinnamon
- Gnome
- KDE
- Unity

## Userspace and privacy
- Each user has a `/home/` directory

- **Root**
    - User A
    - `/home/`

    - User B
    - `/home/`

    - User C
    - `/home/`

- Users may be able to view files, but they cannot edit other users files
- If you have root access, you have access to everything

# Getting to the CLI

**Linux Desktop**
- Open `Terminal` application.
- Once Terminal is open, you can use it to connect to other Linux systems using SSH (Secure Shell)

**SSH Command**
- ssh USER@REMOTE_HOST
- Accept Fingerprint (if you've never logged into the system before)
- Enter password

# Industry Uses

How Linux is used in virtualization and cloud computiong

## Virtualization
- Physical Host Computer - Contains Ram, Storage and CPU
    - Virtual Guest Host 1
    - Virtual Guest Host 2
    - Virtual Guest Host 3

# 2.1

# CLI Basics

# Basic Shell

The standard Linux Shell (BASH) is both a command line interpreter and programming language

## Command Prompt
- Short test string at the beginning of the command line.
- Typically shows the current user, host and working directory
    - `[USER@HOST_NAME ~]$`
- If you are the Root user the command prompt will be a `#`:
       - `[USER@HOST_NAME ~]#`
- The command prompt can be modified to show more or less information
- Input from the command line is sent to the interpreter to be parsed and executed

## Commands
- Commands are entered as text at the command line prompt
- They are parsed by the interpreter and executed by the shell as a process
- Commands are entered as text into the input stream known as Standard In (STDIN)
- These commands adhere to a syntax defined by the interpreter or the current shell

## Command Output
- The output of the entered command is displayed on the the line following the command itself
- Output will be sent to one of two streams
    - Standard Out (STDOUT)
        - Display
        - Redirection or pipeline
    - Standard Error (STDERR) 
        - Display
        - Redirection or pipeline

- **Keyboard Input** -> STDIN -> **Process** -> STDOUT/STDERR -> *Display**

# Command Line Syntax

As the shell input is read, it follows a sequence of operations, ignoring comments (`#`) and seperating the input into words and operations

1. Read Input
    2. Divide Input
        - Ignore comments (comments start with `#`)
    3. Apply Quoting
        - Ignore literal translation of something we are sending to the interpreter
    4. Parse Into Commands
    5. Apply Redirection
    6. Wait for next status
        - was the command successfull or not
8. **Display Output**


Command Options
`ls -a`
`ls -h`

To view all command options, use the `man` command
`man ls`

# Quoting

Preserve the input that contains special characters or spaces
Quoting is used to disable special treatment of certain characters and words, as well as to prevent parameter expansion and preserve what is quoted.

## Methods
**Escape Character**  
A non-quoted backslash `\` is the bash escape character and preserves the literal value of the next following character, with the single exception of a new line `\n`.
- `var1 = Some\ Value`
- `echo $var1`
- Returns:  `Some Value`

**Single Quotes**
Single quotes `'` preserve the literal value of every character contained within the quotes, including the escape character.
- `echo 'this\ is $var1'`
- Returns:  `this\ is $var1`


**Double Quotes**
Double quotes `"` perserver the literal value of most characters contained within the quotes, exceptions include 
`$`(for variables)
`'`(for single quoting)
`\`(For escaping a character)

- `echo "this\ is $var1"`
- Returns:  `this\ is Some Value`

- `echo "this is a "quote"`
- Returns:  `this is a quote`

- `echo "this is a \"quote"\"`
- Returns:  `this is a "quote"`
- Adding the backslash (`\`) preserves the quotes.

# Variables

Using variables to store values for easy reference.

A bash variable may contain a number, character or string of characters.  These variable types do not need to be declared, they are simply assigned

**Assigning a Variable**
`test_variable = "this is a variable"`

**Displaying a Variable**
`echo $test_variable`

**Default Variables**
- `$HOME` The current users working directory
- `PS1` The Primary prompt string
- `$PATH` A colon seperated list of directories where the shell looks for commands

# 2.2

# Using CLI for help

# Info Pages

Additional documentatio with more robust capability and detail.

Info pages normally provide more detailed information about a command than it's respective Man Page.
Info pages use a structure for linking pages together that can be assembled into a larger collection

The info page is invoked by preceding the command with `info`
- `info COMMAND`
- `info ls`

If no info page exists, info can pull up documentation from the Man Page.

# Man Pages

Traditional package documentation for application usage

Manual pages are the traditional form of software documentation on UNIX systems.  They are included with the software they document.

The man page for a particular command is invoked by preceding the command with `man`
- `man COMMAND`
- `man ls`

## Sections of the man command

**Name:**
Program or function name(s) followed by a terse description of the functionality.

**Synopsis:** 
A short overview of available options.

**Description:**
Detailed information of arguments and options.

**Examples:**
Common usage examples

**Exit Status**
- Return Code once a command is run
 - 1: If ok
 - 2: Minor problems
 - 3: If serious trouble
 `ls`
`echo $?`
`0`

# Linux Commands

**View Release Files**
-`cat/etc/*release*`

**View Issues Files**
-`cat/etc/*issue*`

**Distribution release version:**  
- `lsb_release -a`

**Host Name Control**
- Only words on System D based Linux Distros
- `hostnamectl`

