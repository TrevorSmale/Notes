# LPIC 101 501 Course

* Created by the Linux Professional Institute
* LPI LPIC-1 consists of two exams
* Exam 1:
* 60 questions (multiple-choice, multiple-select, fill in the blank)
* 90 minutes to complete exam
* Exam 1 has over 250 Linus items in its objectives

## This course is closely mapped to the objective of the first exam portion '101 501'

* Over 100 hundred videos with an average runtime of 7 miunutes
* Each chapter comes with a quiz to affirm knowledge

## Practice setup

Two recommended distrobutions are:

* CentOS v7 (RedHat based)
* Ubuntu Desktop 18.04 LTS (Debian Based)

Why thsese older versions?

Because they were both release at the time of the LPIC 1 certification and most closely match the exam objectives.

## Basic Commands

tty = what virtual terminal space one is in
whoami = lists the username
pwd = Print working Directory or Present Working Directory
ls = list command, lists all the files and directories in the present working directory
exit = will log the user out

# Unerstanding the virtual directory system

filesystem hirearchy standard (FHS) is similar accross many distrobutions

/boot - Boot loader files
/etc - Config files (system & apps)
/home - User files
/media - Removable media
/mnt - Removable media (older location)
/opt - Third-party apps
/tmp - Temporary files
/usr - Linux program data
/var - Variable data (example: log files)

sub directories

/usr/bin - Linux user program binaries
/usr/sbin - Linux admin program binaries
/usr/local - Local installation program data

