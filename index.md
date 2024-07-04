# AVAIL Intro To The Command Line Interface (CLI)

# Overview

This single-day free webinar provides an introduction to the command line interface (CLI) and a few tools for digital preservation with a focus on audiovisual assets. It's hosted by the Smithsonian Library and Archives (SLA) Audiovisual Preservation Initiative (AVMPI) and Audiovisual Archivists Interest Lunch (AVAIL).

The presentation slides can be accessed at [this link](https://brnco.github.io//AVAIL_Intro-To-CLI_Workshop/webinar.html)

# Table of Contents

[Course Description](https://github.com/brnco/AVAIL_Intro-To-CLI_Workshop#course-description)

[Agenda](https://github.com/brnco/AVAIL_Intro-To-CLI_Workshop#agenda)

[Readings and Resources](https://github.com/brnco/AVAIL_Intro-To-CLI_Workshopp#readings--resources)

[Tools list](https://github.com/brnco/AVAIL_Intro-To-CLI_Workshop#command-line-software-discussed)

[Install Instructions](https://github.com/brnco/AVAIL_Intro-To-CLI_Workshop#install-instructions)

  - [Mac / Homebrew](https://github.com/brnco/AVAIL_Intro-To-CLI_Workshop#mac-setup-instructions)
  - [Windows / WSL](https://github.com/brnco/AVAIL_Intro-To-CLI_Workshop#windows-setup-instructions)
  - [Tools](https://github.com/brnco/AVAIL_Intro-To-CLI_Workshop#install-tools)

# Course Description

With the ever-increasing scale and complexity of digital archival collections, archivists need to adapt their tools and workflows; while every institutional context is different, there are often opportunities to employ open source and command line tools to meet these challenges. Among the many benefits of utilizing the command line, the two most immediate tend to be: increased reliability of processes and more interesting work for archivists. 

This 3-hour workshop will cover the basics of the command line interface (CLI) with a focus on its use in audiovisual archival workflows and digital preservation. The command line software discussed will help archivists navigate their terminals, find/ move/ rename digital objects, understand checksums and CRCs and introduce principles of scripting and automation for handling file data at scale.

This is an introductory course and users with no programming or command line experience are welcome; any archivist who routinely moves files, verifies metadata across systems, or works with audiovisual materials will learn techniques to improve their efficiency and gain familiarity with systems and workflows which take advantage of CLI capabilities. Users don't need to have administrative privileges or the ability to install software on their local machines in order to participate. For users who can install software on their machines, there will be office hours prior to the workshop to go over any questions that arise as part of the setup (and instructions are provided [at this link](https://github.com/brnco/AVAIL_Intro-To-CLI_Workshop#install-instructions)).

# Agenda

## Hour 1

### Part 1 - History, Context, Objectives

what the command line is, what we can do with it, why it matters

### Part 2 - Intro to Commands

basic structures, navigation, inputs & outputs

## Hour 2

### Part 3 - CLI Tools for Digital Preservation

moving files, verifying integrity of files and metadata

## Hour 3

### Part 4 - More Tools + Intro to Scripting

workflow setup, loops

# Command-Line Software Discussed

While not an exhaustive list, the webinar will touch on some fundamental software to managing digital files, with an emphasis on audiovisual formats.

These tools include:

[bash](https://www.gnu.org/software/bash/)

[rsync](https://rsync.samba.org/)

[md5sum](https://linux.die.net/man/1/md5sum) + [shasum](https://linux.die.net/man/1/shasum)

[MediaInfo](https://mediaarea.net/en/MediaInfo)

[BWF MetaEdit](https://mediaarea.net/BWFMetaEdit)

# Readings & Resources

[Programming is Forgetting: Toward a New Hacker Ethic](http://opentranscripts.org/transcript/programming-forgetting-new-hacker-ethic/) by Allison Parrish

[Heroes in a Bash Shell](https://www.redhat.com/en/command-line-heroes/season-3/heroes-in-a-bash-shell) by Command Line Heroes

[The Bash Parser](http://mywiki.wooledge.org/BashParser) - what happens after you press enter on a command in the terminal

[Script Ahoy](https://dd388.github.io/crals/) - a bash helper for archivists by Dianne Dietrich and Jarret Drake

[Bash for Archivists](https://reto.ch/training/2020/202006/) - an intro course by Reto Kromer

[Man Pages](https://en.wikipedia.org/wiki/Man_page) - the Wikipedia page for "man pages" aka manual pages, describing the history and use of manual pages in the command line

# Install instructions

## Test Files

Use this link 🚧coming soon🚧 to download a set of test files that you'll use during the webinar 

## Text Editor

You will need a text editor - text editors are different than Microsoft Word. You'll be editing .txt and .sh files. On Windows, the default editor is Notepad, which will work fine. There's also Notepad++. On Mac, the default text editor is TextEdit, also fine.

I strongly recommend looking into the [Visual Studio Code (VSCode) text editor](https://code.visualstudio.com/), which is available on all platforms. It's a bit much for what we're doing today but it's the most popular text editor out there and can be customized to fit your needs.

I will mostly be using a terminal-based text editor (i.e. a text editor that opens within the terminal) named [Vim](https://www.vim.org/), which is probably already installed on your system. Vim is legendarily difficult to use, though, and I don't really recommend it for beginners. Still, if you want to dive into the deepest deep end, it's there.

## OS-specific installs

### MacOS

Macs ship with an application named “Terminal” which is their default command line interface. It will work great for this webinar

To install the tools/ software for this webinar, we will be using something called a “package manager.” Package managers help people manage their software without the use of “installers” like you might be used to, they’re very common on Linux and in programmer spaces, generally.

For Macs, the packagae manager is named Homebrew and, once you have installed it, proceed to the [tools install section](https://github.com/brnco/AVAIL_Intro-To-CLI_Workshop#install-tools)

#### Install Homebrew

If you have administrative access to your machine, you can install Homebrew with [the steps on their website](https://brew.sh) (it’s a Terminal command).

If you don't have admin access on your Mac, you can still install Homebrew and the other tools for this workshop by using the below steps.

1. Open Terminal
  - type `Cmd + Space` to search your mac
  - type `terminal` and press enter
2. In Terminal, navigate to your home folder
  - type `cd ~/` and press enter
3. install Homebrew in your home folder
  - type the below and press enter
  - `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"` and press enter
4. Once that command completes, go to Terminal -> Preferences -> Shell
  - In the "Startup" Section, check the box to "Run Command"
  - type this command into the box `export PATH=$PATH:${HOME}/brew/bin`
  - Check the box to "Run inside shell"

With either install method, you can check if your install was successful by opening Terminal and typing `brew help` - if you get help output, you're good; if you get an error, email me.

### Windows

This workshop is based on the BASH programming language/ shell, which, until recently, was not available by default on Windows as it was on Mac. Windows used a proprietary command-line interface referred to as cmd.exe, originally released in 1993. It’s like bash in its operation but there are many, many syntactical and technical differences. Because it's Windows, and they can't do anything just one way, there's another application called PowerShell which is a bit more Bash-like. While I have experience scripting on Windows, those skills are not very sharp at this time and I just don’t think I can support you at the level I’d need to in this workshop.

That being said, you are welcome to follow along in CMD/ PowerShell and make the modifications necessary, if you’d like.

Otherwise, we’re going to install Bash on your Windows machine, through the Windows subsystem for Linux (WSL). WSL is like having Linux installed, except without the headache of partitioning discs or creating bootable disc images - it’s Linux running as a Microsoft Windows application. It’s an official Windows software, so you can trust it at the same level you trust anything from them (😉)

With WSL installed, we will then use the Ubuntu Linux package manager, named apt, to install software.

Once you have installed WSL, proceed to the [tools install section](https://github.com/brnco/AVAIL_Intro-To-CLI_Workshop#install-tools)

#### Check if WSL is already installed

Use Windows Search (hit the Windows key on your keyboard), type `wsl` and hit enter. You should see a box pop up, this is cmd.exe starting WSL (sorry for the alphabet soup).

In a few seconds, you should see a prompt that looks like this `brnco@CHM3083:/mnt/c/WINDOWS/system32$` but with your login info. If you see that, great, you have WSL up and running! Otherwise, see below for official Microsoft documentation.

#### Install Windows Subsystem for Linux (WSL)

To install WSL, follow [the instructions on the Microsoft website](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

[Here is a great video](https://www.youtube.com/watch?v=X-DHaQLrBi8) describing the steps, as well

## Install command line tools

This section assumes that you have completed the above steps to install Homebrew/ WSL

This software is installed entirely via the command line. Each command is written on its own line and will appear formatted `like this`. Type the command in exactly as you see it here and press enter after each command.

### MediaInfo

MediaInfo displays structured technical metadata from a variety of audiovisual media filetypes, everything from sample rates to listing subtitle tracks

#### Mac

`brew install mediainfo`

#### WSL

`sudo apt install mediainfo`

### BWF MetaEdit

BWF MetaEdit displays and embeds metadata into a WAVE file's headers, per the Broadcast WAVE specification

#### Mac

`brew install bwfmetaedit`

#### WSL

`sudo apt install bwfmetaedit`
