# prompters
A collection, growing, of shell scripts to guide/prompt the use of various shell commands.

This project was started out of my frustration at (a) finding the right shell command and then (b) using it. For years (decades actually) I've developed
ISPF menus and dialogs that help users to find and use MVS, OS/390, and z/OS applications.

## Overview

These prompters are shell scripts that use the `gum` tool for display and prompting.

See https://github.com/charmbracelet/gum for particulars about `gum`.

The z/OS port of `gum` can be found here https://github.com/ZOSOpenTools.

**caveat** These are some of my first shell scripts so bear with me - contributors are welcome to assist/improve.

### Notes:

1. While I would like to use `gum pager` I found that the z/OS port of `pager` didn't work so for now these use `less` which does work.

## dsfs-menu

This prompter will prompt for one of the `dsadm` commands used with `dsfs` on z/OS. It will then prompt for the various options allowed and then invoke the command.

## mantastic

This tools will prompt for a string (i.e. `ssh`) and will display a selection list of all man pages with the string in the page description.

It may be invokeed one of two ways:

`mantastic` will prompt for the string

`mantastic string` will bypass the prompt and immediately present the selection list.

