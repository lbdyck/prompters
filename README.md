# prompters
A collection, growing, of shell scripts to guide/prompt the use of various shell 
commands.

***Note that the names of the tools are subject to change if anyone has a better name
for them***

This project was started out of my frustration at (a) finding the right shell command 
and then (b) using it. For years (decades actually) I've developed
ISPF menus and dialogs that help users to find and use MVS, OS/390, 
and z/OS applications.

## Overview

These prompters are shell scripts that use the `gum` tool for display and prompting.

See https://github.com/charmbracelet/gum for particulars about `gum`.

The z/OS port of `gum` can be found here https://github.com/ZOSOpenTools.

**caveat** These are some of my first shell scripts so bear with me - contributors 
are welcome to assist/improve.

### Notes:

1. The use of `more` or `less` are also valid pagers, but the `gum pager` is 
the preferred viewer.
2. These are work in progress - improvements welcome.

## dsfs-menu

This prompter will prompt for one of the `dsadm` commands used with `dsfs` on z/OS. 
It will then prompt for the various options allowed and then invoke the command.

## mantastic

This tool will prompt for a string (i.e. `ssh`) and will display a selection list 
of all man pages with the string in the page description.

It may be invoked one of two ways:

`mantastic` will prompt for the string

`mantastic string` will bypass the prompt and immediately present the selection list.

## zoinstall

This tool demonstrates constructing a zopen install command by prompting for the
packages to install and then perform a `mandb` if enabled.

## zoremove

The reverse of zopen_install to remove packages.

## tspin

This is a demonstation script to show the various gum spin spinner options.

