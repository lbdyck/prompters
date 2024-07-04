# prompters
A collection, growing, of shell scripts to guide/prompt the use of various shell 
commands.

***Note that the names of the tools are subject to change if anyone has a better name
for them***

This project was started out of my frustration at (a) finding the right shell command 
and then (b) using it. For years (decades actually) I've developed
ISPF menus and dialogs that help users to find and use MVS, OS/390, 
and z/OS applications.

**NOTE** Be sure to check out the [Prompters Wiki ](https://github.com/lbdyck/prompters/wiki)

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
3. The use of `gsed` from the z/OS Open Tools is a pre-req just as `gum` is.

## [dsfs-menu])dsfs-menu)

This prompter will prompt for one of the `dsadm` commands used with `dsfs` on z/OS. 
It will then prompt for the various options allowed and then invoke the command.

## [mantastic](mantastic)

This tool will prompt for a string (i.e. `git`) and will display a selection list 
of all man pages with the string in the page description.

It may be invoked one of two ways:

`mantastic` will prompt for the string

`mantastic string` will bypass the prompt and immediately present the selection list.

`mantastic man-page -d` to immediately display the man page.

`mantastic -h` or `-help` or `?` to display a short help message.

**Note** The use of `mandb` to update the man page database is highly (strongly) recommended.

## zoauhelper

This is an initial swag at providing a tool to help with `zoau`. The `zoau` man pages are not
usable with the z/OS Open Tools version of `man` and are not indexed for the z/OS standard
`man` command. 

This is an attempt to provide some help.

## [zothelper](zothelper)

This tools will prompt for one of the available `zopen` options and then construct the 
appropriate command.

If the selected command is not support by `zothelper` then the commands help will be displaywed.

Currently `clean`, `install`, and `remove` are supported.

## zotfile

This is very much a work in progress. A swag at a easy to use file manager for the shell user
using `gum`. It is definitely a *use at your own risk* and any/all comments/suggestions/contributions
are welcome.

## [tspin](tspin)

This is a demonstation script to show the various gum spin spinner options.

