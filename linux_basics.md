# Linux Basics
Welcome to Linux. The main differences you will experience compared to Windows are the following:

1. Far more use of the terminal
2. Far greater control over the inner workings of your operating system
3. Almost everything is free
4. Far greater reliability

That being said, there are some considerable changes you'll have to get used to. This guide aims to make the learning curve gentler. 

<!--ts-->
# Table of Contents
- [ ] apt
- [ ] Basic commands
	* cat
	* man
	* grep
- [ ] git
- [ ] ssh
- [ ] file system & commands
	* links
	* file descriptors
	* permissions
- [ ] vim
- [ ] bash, streams, piping
- [ ] regex/globbing
<!--te-->

# Architecture
Linux architecture has for main layers as seen below:
![Linux Architecture](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.tutorialspoint.com%2Fimages%2Funix_architecture.jpg&f=1&nofb=1)
## Kernel
Closest to the physical hardware of your computer is the **kernel**. The Linux kernel was primarily developed by Linus Torvalds which is where Linux got it's name from: a portmanteau of Linus and Unix (Unix is a family of OS). The kernel is essentially the brain of the system and is responsible for interacting with hardware, managing resources and scheduling processes. 

## Shell
Just above the kernel is the **shell**. The shell is what runs the terminal/command line/console, but the terms are [often used interchangeably](https://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line). Users communicate with the kernel through the shell using a plethora of Linux commands. These commands are one of the greatest assets of Linux as they are extremely versatile, scriptable and have great synergy.

Please see [this article](https://cumulusnetworks.com/blog/linux-architecture/) for more details.

# Terminal
While intimidating at first, the terminal will become your proffered interface for interacting with your system. Ubuntu uses Press `Ctrl-Alt-t` from anywhere to open up the terminal and a window, purple by default in Ubuntu, will pop up. Keep in mind the terminal is just a program that gives access to the shell and the default Ubuntu terminal can be replaced by a custom terminal. 

## User Interface
The first thing you'll notice as you start typing is that it uses a block cursor rather than a vertical bar which is more common in Windows. This can be configured by right clicking, selecting `Preferences`, then `Text` tab and `Cursor` options, but it is not recommended as block cursors are most commonly used. You can also find options to change the background colour and keyboard shortcuts in this preference window.

To the left of the cursor you'll see some text in the format `USER_NAME@HOSTNAME:CURRENT_WORKING_DIRECTORY$`. User name and hostname will be discussed in further detail in the [ssh section](#ssh), and the current working directory (CWD) will be discussed in the [file system](#file-system) section.

## Shortcuts
Intuitive Windows keyboard shortcuts do not work in the terminal. Copy by highlighting text, then using `Ctrl-C`, paste with `Ctrl-V` and undo with `Ctrl-_`.  There are 3 main types of keyboard shortcuts: local terminal shortcuts configurable in the [preferences menu](#user-interface), [Emacs or Vim shortcuts](https://superuser.com/questions/352983/which-emacs-shortcuts-are-useful-in-bash) (popular text editors. see [==text editors==](#text-editors)) and [line discipline shortcuts](https://unix.stackexchange.com/questions/362559/list-of-terminal-generated-signals-eg-ctrl-c-sigint) (view all line discipline shortcuts with `stty -a`). 

The most important 3 shortcuts however, are `Ctrl-c` program interrupting with `SIGINT`, tab completion,  and finally [middle click pasting](https://askubuntu.com/questions/167570/how-does-middle-click-paste-work#167591).
1. `Ctrl-c` interrupting falls under the line discipline shortcut category and works by sending a `SIGINT` to the program running in the terminal foreground. [Signals](https://www.computerhope.com/unix/signals.htm) are a more advanced topic but [==foreground/background==](#remote-work) will be covered later.
2. Tab completion is a useful time saving feature of the terminal and is essentially auto-complete for the terminal. The terminal will try to guess what to complete when tapping tab once while typing, and double tapping will show available options for completion. An example is discussed in the [==filesystem==](#filesystem) section.
3. To use middle click pasting, highlight text with your cursor, then middle click on the place you want to paste text. The clipboard used is different from the one used by `Ctrl-c/v`. Please read this [stackoverflow](https://askubuntu.com/questions/167570/how-does-middle-click-paste-work#167591) answer for more details.

==A cheat sheet may or may not be included. [good list](https://linuxhandbook.com/linux-shortcuts/)==



# Installing Programs
There are many ways to 



FIle extensions aren't real!

