# LPIC 1 Exam Objects for both 101 and 102 parts

The following are the areas in which you must be proﬁcient in order to pass the 101 exam.
This exam is broken into four topics (101–104), each of which has three to eight objectives.
Each objective has an associated weight, which reﬂects its importance to the exam as a
whole. The four main topics are:
Subject Area

* 101 System Architecture
* 102 Linux Installation and Package Management
* 103 GNU and Unix Commands
* 104 Devices, Linux Filesystems, Filesystem Hierarchy Standard
* 101 System Architecture

## 101.1 Determine and Configure hardware settings (Chapter 3)

* Enable and disable integrated peripherals
* Configure systems with or without external peripherals such as keyboards
* Differentiate between the various types of mass storage devices
* Set the correct hardware ID for different devices, especially the boot device
* Know the differences between coldplug and hotplug devicesxxx
* Introduction
* Determine hardware resources for devices
* Tools and utilities to list various hardware information (e.g., lsusb, lspci, etc.)
* Tools and utilities to manipulate USB devices
* Conceptual understanding of sysfs, udev, hald, dbus
* The following is a partial list of the used files, terms, and utilities: /sys, /proc, /dev,
modprobe, lsmod, lspci, lsusb

## 101.2 Boot the System (Chapter 5)

* Provide common commands to the boot loader and options to the kernel at boot time
* Demonstrate knowledge of the boot sequence from BIOS to boot completion
* Check boot events in the log file
* The following is a partial list of the used files, terms and utilities: /var/log/messages,
dmesg, BIOS, bootloader, kernel, init

# 101.3 Change runlevels and shutdown or reboot system (Chapter 5)
* Set the default run level
* Change between run levels including single user mode
* Shutdown and reboot from the command line
* Alert users before switching run levels or other major system events
* Properly terminate processes
* Knowledge of basic features of systemd and Upstart
* The following is a partial list of the used files, terms and utilities: /etc/inittab,shutdown, init, /etc/init.d, telinit

# 102 Linux Installation and Package Management

## 102.1 Design hard disk layout (Chapter 3)

* Allocate filesystems and swap space to separate partitions or disks
* Tailor the design to the intended use of the system
* Ensure the /boot partition conforms to the hardware architecture requirements for booting
* Knowledge of basic features of LVM
* The following is a partial list of the used files, terms and utilities: / (root) filesystem, /var filesystem, /home filesystem, swap space, mount points, partitionsExam 101 Objectives
xxxi

## 102.2 Install a boot manager (Chapter 5)

* Providing alternative boot locations and backup boot options
* Install and configure a boot loader such as GRUB Legacy
* Perform basic configuration changes for GRUB 2
* Interact with the boot loader
* The following is a partial list of the used files, terms, and utilities, /boot/grub/menu.lst, grub.cfg and other variations, grub-install, MBR, superblock

## 102.3 Manage shared libraries (Chapter 2)

* Identify shared libraries
* Identify the typical locations of system libraries
* Load shared libraries
* The following is a partial list of the used files, terms and utilities, ldd, ldconfig, /etc/ld.so.conf, LD_LIBRARY_PATH

## 102.4 Use Debian package management (Chapter 2)

* Install, upgrade and uninstall Debian binary packages
* Find packages containing specific files or libraries which may or may not be installed
* Obtain package information like version, content, dependencies, package integrity and installation status (whether or not the package is installed)
* The following is a partial list of the used files, terms and utilities: /etc/apt/sources.list, dpkg, dpkg-reconfigure, apt-get, apt-cache, aptitude

## 102.5 Use RPM and YUM package management (Chapter 2)

* Install, re-install, upgrade and remove packages using RPM and YUM
* Obtain information on RPM packages such as version, status, dependencies, integrity and signatures
* Determine what files a package provides, as well as find which package a specific file comes from
* The following is a partial list of the used files, terms and utilities: rpm, rpm2cpio, /etc/yum.conf, /etc/yum.repos.d/, yum, yumdownloaderxxxii
Introduction

# 103 GNU and Unix Commands

## 103.1 Work on the command line (Chapter 1)

* Use single shell commands and one line command sequences to perform basic tasks on
the command line
* Use and modify the shell environment including defining, referencing and exporting
environment variables
* Use and edit command history
* Invoke commands inside and outside the defined path
* The following is a partial list of the used files, terms and utilities: ., bash, echo, env, exec, export, pwd, set, unset, man, uname, history

## 103.2 Process text streams using filters (Chapter 1)

* Send text files and output streams through text utility filters to modify the output using standard UNIX commands found in the GNU textutils package
* The following is a partial list of the used files, terms and utilities: cat, cut, expand, fmt, head, od, join, nl, paste, pr, sed, sort, split, tail, tr, unexpand, uniq, wc

## 103.3 Perform basic file management (Chapter 4)

* Copy, move and remove files and directories individually
* Copy multiple files and directories recursively
* Remove files and directories recursively
* Use simple and advanced wildcard specifications in commands
* Using find to locate and act on files based on type, size, or time
* Usage of tar, cpio, and dd
* The following is a partial list of the used files, terms and utilities: cp, find, mkdir, mv,ls, rm, rmdir, touch, tar, cpio, dd, file, gzip, gunzip, bzip2, file globbing

## 103.4 Use streams, pipes and redirects (Chapter 1)

* Redirecting standard input, standard output and standard error
* Pipe the output of one command to the input of another command
* Use the output of one command as arguments to another command
* Send output to both stdout and a file
* The following is a partial list of the used files, terms and utilities: tee, xargsExam 101 Objectives xxxiii

## 103.5 Create, monitor and kill processes (Chapter 2)

* Run jobs in the foreground and background
* Signal a program to continue running after logout
* Monitor active processes
* Select and sort processes for display
* Send signals to processes
* The following is a partial list of the used files, terms and utilities: &, bg, fg, jobs, kill,nohup, ps, top, free, uptime, killall

## 103.6 Modify process execution priorities (Chapter 2)

* Know the default priority of a job that is created
* Run a program with higher or lower priority than the default
* Change the priority of a running process
* The following is a partial list of the used files, terms and utilities: nice, ps, renice, top

## 103.7 Search text files using regular expressions (Chapter 1)

* Create simple regular expressions containing several notational elements
* Use regular expression tools to perform searches through a filesystem or file content
* The following is a partial list of the used files, terms and utilities: grep, egrep, fgrep,sed, regex(7)

## 103.8 Perform basic file editing operations using vi (Chapter 5)

* Navigate a document using vi
* Use basic vi modes
* Insert, edit, delete, copy and find text
* The following is a partial list of the used files, terms and utilities: vi, /, ?, h, j, k, l, i,o, a, c, d, p, y, dd, yy, ZZ, :w!, :q!, :e!

# 104 Devices, Linux Filesystems, Filesystem Hierarchy Standard

## 104.1 Create partitions and filesystems (Chapter 3)

* Use various mkfs commands to set up partitions and create various filesystems such as:ext2, ext3, xfs, reiserfs v3, vfat
* The following is a partial list of the used files, terms and utilities: fdisk, mkfs, mkswapxxxiv Introduction

## 104.2 Maintain the integrity of filesystems (Chapter 3)

* Verify the integrity of filesystems
* Monitor free space and inodes
* Repair simple filesystem problems
* The following is a partial list of the used files, terms and utilities: du, df, fsck, e2fsck,mke2fs, debugfs, dumpe2fs, tune2fs, xfs tools (such as xfs_metadump and xfs_info)

## 104.3 Control mounting and unmounting of filesystems
(Chapter 3)

* Manually mount and unmount filesystems
* Configure filesystem mounting on bootup
* Configure user mountable removeable filesystems
* The following is a partial list of the used files, terms and utilities: /etc/fstab, /media,mount, umount

## 104.4 Manage disk quotas (Chapter 4)

* Set up a disk quota for a filesystem
* Edit, check and generate user quota reports
* The following is a partial list of the used files, terms and utilities: quota, edquota,repquota, quotaon

## 104.5 Manage file permissions and ownership (Chapter 4)

* Manage access permissions on regular and special files as well as directories
* Use access modes such as suid, sgid and the sticky bit to maintain security
* Know how to change the file creation mask
* Use the group field to grant file access to group members
* The following is a partial list of the used files, terms and utilities: chmod, umask, chown,chgrp

## 104.6 Create and change hard and symbolic links (Chapter 4)

* Create links
* Identify hard and/or soft links
* Copying versus linking files
* Use links to support system administration tasks
* The following is a partial list of the used files, terms and utilities: lnExam 102 Objectives xxxv

## 104.7 Find system files and place files in the correct location
(Chapter 4)

* Understand the correct locations of files under the FHS
* Find files and commands on a Linux system
* Know the location and propose of important file and directories as defined in the FHS
* The following is a partial list of the used files, terms and utilities: find, locate,updatedb, whereis, which, type, /etc/updatedb.conf

# Topic 105: Shells and Shell Scripting

## 105.1: Shells and Shell Scripting

* Set environment variables (e.g. PATH) at login or when spawning a new shell.
* Write Bash functions for frequently used sequences of commands.
* Maintain skeleton directories for new user accounts.
* Set command search path with the proper directory.

## 105.2 Customize or write simple scripts

* Use standard sh syntax (loops, tests).
* Use command substitution.
* Test return values for success or failure or other information provided by a command.
* Execute chained commands.
* Perform conditional mailing to the superuser.
* Correctly select the script interpreter through the shebang (#!) line.
* Manage the location, ownership, execution and suid-rights of scripts.

# Topic 106: User Interfaces and Desktops

## 106.1 Install and configure X11

* Understanding of the X11 architecture.
* Basic understanding and knowledge of the X Window configuration file.
* Overwrite specific aspects of Xorg configuration, such as keyboard layout.
* Understand the components of desktop environments, such as display managers and window managers.
* Manage access to the X server and display applications on remote X servers.
* Awareness of Wayland.

## 106.2 Graphical Desktops

* Awareness of major desktop environments
* Awareness of protocols to access remote desktop sessions

# 106.3 Accessibility

* Basic knowledge of visual settings and themes.
* Basic knowledge of assistive technology.

# Topic 107: Administrative Tasks

## 107.1 Manage user and group accounts and related system files

* Add, modify and remove users and groups.
* Manage user/group info in password/group databases.
* Create and manage special purpose and limited accounts.

## 107.2 Automate system administration tasks by scheduling jobs

* Manage cron and at jobs.
* Configure user access to cron and at services.
* Understand systemd timer units.

## 107.3 Localisation and internationalisation

* Configure locale settings and environment variables.
* Configure timezone settings and environment variables.

# Topic 108: Essential System Services

## Topic 108: Essential System Services

* Set the system date and time.
* Set the hardware clock to the correct time in UTC.
* Configure the correct timezone.
* Basic NTP configuration using ntpd and chrony.
* Knowledge of using the pool.ntp.org service.
* Awareness of the ntpq command.

## 108.2 System logging

* Basic configuration of rsyslog.
* Understanding of standard facilities, priorities and actions.
* Query the systemd journal.
* Filter systemd journal data by criteria such as date, service or priority
* Configure persistent systemd journal storage and journal size
* Delete old systemd journal data
* Retrieve systemd journal data from a rescue system or file system copy
* Understand interaction of rsyslog with systemd-journald
* Configuration of logrotate.
* Awareness of syslog and syslog-ng.

# 108.3 Mail Transfer Agent (MTA) basics

* Create e-mail aliases.
* Configure e-mail forwarding.
* Knowledge of commonly available MTA programs (postfix, sendmail, exim) (no configuration)

# 108.4 Manage printers and printing

* Basic CUPS configuration (for local and remote printers).
* Manage user print queues.
* Troubleshoot general printing problems.
* Add and remove jobs from configured printer queues.

# Topic 109: Networking Fundamentals

## 109.1 Fundamentals of internet protocols

* Demonstrate an understanding of network masks and CIDR notation.
* Knowledge of the differences between private and public "dotted quad" IP addresses.
* Knowledge about common TCP and UDP ports and services (20, 21, 22, 23, 25, 53, 80, 110, 123, 139, 143, 161, 162, 389, 443, 465, 514, 636, 993, 995).
* Knowledge about the differences and major features of UDP, TCP and ICMP.
* Knowledge of the major differences between IPv4 and IPv6.
* Knowledge of the basic features of IPv6.

## 109.2 Persistent network configuration

* Understand basic TCP/IP host configuration
* Configure ethernet and wi-fi network configuration using NetworkManager
* Awareness of systemd-networkd

## 109.3 Basic network troubleshooting

* Manually configure network interfaces, including viewing and changing the configuration of network interfaces using iproute2.
* Manually configure routing, including viewing and changing routing tables and setting the default route using iproute2.
* Debug problems associated with the network configuration.
* Awareness of legacy net-tools commands.

## 109.4 Configure client side DNS

* Query remote DNS servers.
* Configure local name resolution and use remote DNS servers.
* Modify the order in which name resolution is done.
* Debug errors related to name resolution.
* Awareness of systemd-resolved

# Topic 110: Security

## 110.1 Perform security administration tasks

* Audit a system to find files with the suid/sgid bit set.
* Set or change user passwords and password aging information.
* Being able to use nmap and netstat to discover open ports on a system.
* Set up limits on user logins, processes and memory usage.
* Determine which users have logged in to the system or are currently logged in.
* Basic sudo configuration and usage.

## 110.2 Setup host security

* Awareness of shadow passwords and how they work.
* Turn off network services not in use.
* Understand the role of TCP wrappers.

## 110.3 Securing data with encryption

* Perform basic OpenSSH 2 client configuration and usage.
* Understand the role of OpenSSH 2 server host keys.
* Perform basic GnuPG configuration, usage and revocation.
* Use GPG to encrypt, decrypt, sign and verify files.
* Understand SSH port tunnels (including X11 tunnels).












