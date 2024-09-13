Date: 2024-07-18
Hub: [[linux]]
Tags: #book
URL/Title: Learning Modern Linux

A program that runs inside the [[terminal]] and acts as a command interpreter. Shell uses [[streams]] for input and output handling and supports variables and scripting. 

Shell is formally defined in sh and there is even a [[POSIX]] shell, but commonly reference as bash shell is the main one used today (the guy who made the originally common used shell was named bourne and bash is a play on bourne again shell). 

##### Special symbols:
- &: When placed at the end of a command it will run the command in the background
- \\\\: When placed in a line it allows the command to continue on the next line for better readability
- |: Connects standard out to standard in without having to store the data, the common example of cating a file and using pipe to grep some text from that file

##### Variables:
Classic use case of not wanting to hard code a value variables can be used to store and change a value. 
- Environment variables: Shell wide settings, can be listed with env, to set use [[export]] to create one and to access put a $ in front of it. 
- Shell variables: Valid in current execution, listed with set in bash
List of common shell and environment variables:
```
Variable Type Semantics
EDITOR Environment The path to program used by default to edit les
HOME POSIX The path of the home directory of the current user
HOSTNAME bash shell The name of the current host
IFS POSIX List of characters to separate elds; used when the shell splits words on expansion
PATH POSIX Contains a list of directories in which the shell looks for executable programs (binaries or scripts)
PS1 Environment The primary prompt string in use
PWD Environment The full path of the working directory
OLDPWD bash shell The full path of the directory before the last cd command
RANDOM bash shell A random integer between 0 and 32767
SHELL Environment Contains the currently used shell
TERM Environment The terminal emulator used
UID Environment Current user unique ID (integer value)
USER Environment Current user name
_ bash shell Last argument to the previous command executed in the foreground
? bash shell Exit status; see “Exit status” on page 39
$ bash shell The ID of the current process (integer value)
0 bash shell The name of the current process
```

##### Exit status
Exit status is similar to just an error code where 0 defines a success and any other number is an error and a reasoning for why it happened.

##### Built in commands
Shells have a number of built in commands that can be listed with the help command, some can also be found in usr/bin.
- which + a command will show what directory the command is in
- type + a command shows how the command is alias, so what the full command ex. ll for me is aliased to ls -alF

##### Job Control
When a command is run it will take control of the terminal stdin and stdout, or running in the foreground. If this isn't desired you can have a process move to run in the background with ctrl + z. Or when attempting the command type & at the end. You can do the jobs command to list all the current jobs.

Jobs can keep running by putting the nohup command before the desired command or if you forget you can use the disown command to do the same thing. On the opposite end if you want to stop a process from continuing you can use the kill command to stop it with various levels of forcefulness.

### Common Shell Commands

```
Table 3-2. Shell navigation and editing shortcuts
Action Command Note
Move cursor to start of line Ctrl+a -
Move cursor to end of line Ctrl+e -
Move cursor forward one character Ctrl+f -
Move cursor back one character Ctrl+b -
Move cursor forward one word Alt+f Works only with left Alt
Move cursor back one word Alt+b -
Delete current character Ctrl+d -
Delete character left of cursor Ctrl+h -
Delete word left of cursor Ctrl+w -
Delete everything right of cursor Ctrl+k -
Delete everything left of cursor Ctrl+u -
Clear screen Ctrl+l -
Cancel command Ctrl+c -
Undo Ctrl+_ bash only
Search history Ctrl+r Some shells
Cancel search Ctrl+g Some shell
```

##### Command line file manipulation
- echo - prints to stdout
- cat - prints file to stdout
- > - puts stream into file as in "hello" > ex.txt
- >> - same as > but for appending
- sed - used to find and replace in a file (similar to vim style)
- diff  - differences between files
- head - can specify to cat file from top a specific amount of lines
- tail - same as head but from the bottom
- date - used to get a printout of the time and date

##### Modern shells:
- FIsh: User friendly shell with lots of configuration and history and autocomplete packed in, while still being very similar to bash.
- Z-shell: Bourne like shell