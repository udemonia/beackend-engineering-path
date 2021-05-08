# Terminal Commands

## Manual Structure

1. User Commands
2. System Calls
3. C Library Functions
4. Devices and Special Files
5. File Formats and Conventions
6. Games
7. Miscellaneous
8. Special Administration

----

1 **User Commands** - Commands that can be run from the shell by a normal user (typically no administrative privileges are needed)
2 **System Calls** - Programming functions used to make calls to the Linux kernel
3 **C Library Functions** - Programming functions that provide interfaces to specific programming libraries.
4 **Devices and Special Files** - File system nodes that represent hardware devices or software devices.
5 **File Formats and Conventions** - The structure and format of file types or specific configuration files.
6 **Games** - Games available on the system
7 **Miscellaneous** - Overviews of miscellaneous topics such as protocols, filesystems and so on.
8 **System administration** - tools and Daemons Commands that require root or other administrative privileges to use

## Standard Input v Standard Output & Data Stream

data streams - - - -  standard data stream

non data stream ------

> standard input, by default, is associated with the keyboard


standard input - - - - - >   command  - - - - - > standard output

standard input - - - - - >   command  - - - - - > standard error

command line inputs ----->   command  ----------> standard output

command line inputs ----->   command  ----------> error output

redirection

you can change where a data stream goes - like updating a stream of water 💦

> cat man

"With no FILE, or when FILE is -, read standard input."

so if we don't pass cat a command option we will read the text form standard input (the keyboard)

that is why you get the blinking cursor which just turns displays what you're typing

because we can redirect data streams, we can tell it where to get its data from

**All the POWER** _the ability to combine data streams is what make it so powerful_

connecting outputs to inputs is called **piping** - we're building a pipeline of data.

### SUMMARY

there are two ways to get data into a command and 2 ways to get it out

by default standard output and standard error are attached to your terminal by default, can be changed

standard input is attached to the keyboard by default, this can be changed

## Redirection

The most powerful ability 👾

Pipeing & Redirection

> cat 1> output.txt

take the output from data stream number 1 and pipe it to output.txt

> > or >> (overwrite or append)

great blog post about redirection: http://mywiki.wooledge.org/BashGuide/InputAndOutput?#Redirection
