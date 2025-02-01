---
marp: true
theme: uncover
class: invert
---

# An Intro to the Terminal
By: Joachim Horshauge

---
## Terminal Emulator
* Mac OS X: Terminal (default), iTerm 2
* Windows: ConEmu, Windows Terminal, PuTTy
* Linux: Gnome Terminal, Konsole, XTerm

--- 

## The Shell
The shell interprets a user’s commands and tells the server’s operating system what to do with them

#### Common shells
* bash (default on linux)
* zsh (default on mac)

---

## The Command Prompt

```
joachim@my-pc:~$
```

* **joachim**: The username of the current user
* **my-pc**: The hostname of the computer or server
* **~**: The current directory. ~ is the home directory and it represents /Users/joachimhorshauge
* **$**: The prompt symbol. 

--- 
## Running Commands
An instance of a running command is known as a process

* Foreground process
* Background process
---
## Running Commands

Write your command and press enter
```bash
joachim@my-pc:~$ ls
Applications
Desktop
Documents
...
```
---
## Running Commands with Arguments

Write your command and press enter
```bash
joachim@my-pc:~$ ls -la
-rw-r--r--    1 joachimhorshauge  staff     41 Dec 24 14:27 .bashrc
lrwxr-xr-x    1 joachimhorshauge  staff    35B Dec 20 12:40 .editorconfig -> dotfiles/editorconfig/.editorconfig
drwx------+  16 joachimhorshauge  staff   512B Jan 30 23:20 Documents
...
```

---

## Running Commands with Arguments
Which arguments can i use?

---

## RTFM
* Read the f*cking manual
* use the `man` command
    ```man ls ```

---

## Manual
- Very detailed documentation on what the command does

- I will show an alternative i use daily later.



---
# Navigation and Filemangement
---
## Where am I?
Use the `pwd` command i.e *print working directory* 

```bash
joachim@my-pc:~/repos$ pwd
/home/joachim/repos
```

---

## How do I change the working directory?
Use the `cd` command i.e *change directory* 

```bash
joachim@my-pc:~/repos$ cd /usr/share
joachim@my-pc:/usr/share$ pwd
/usr/share
```
---
## How do I get home?
Use the `cd` command i.e *change directory* 

```bash
joachim@my-pc:~/repos$ cd
joachim@my-pc:~$ pwd
/home/joachim
```

---
## How do I create a file?

```bash
joachim@lommeulken-vps:~/repos/hello$ ls

```

no files in the directory hello

```bash
joachim@lommeulken-vps:~/repos/hello$ touch msg
joachim@lommeulken-vps:~/repos/hello$ ls
msg
```
1 file named msg in the directory hello

--- 

## Creating Directories

Use the `mkdir` command to create a new directory.
```bash
joachim@my-pc:~$ mkdir new_folder
joachim@my-pc:~$ ls
new_folder
```
---
## Removing Files and Directories

Use the `rm` command to remove files and `rmdir` or `rm -r` to remove directories.

```bash
joachim@my-pc:~$ rm file.txt
joachim@my-pc:~$ rmdir empty_folder
joachim@my-pc:~$ rm -r folder_with_contents
```

---
## Viewing Permissions

Use the `ls -l` command to view file permissions.
```bash
joachim@my-pc:~$ ls -l
-rw-r--r-- 1 joachim staff 0 Jan 31 10:00 file.txt
```
---

## Changing Permissions

Use the chmod command to change file permissions. 
```bash
joachim@my-pc:~$ chmod 755 script.sh
```

---
## Environment Variables

Use the printenv command to view all environment variables.
```bash
joachim@my-pc:~$ printenv
HOME=/home/joachim
PATH=/usr/local/bin:/usr/bin:/bin
```
---
## Setting Environment Variables

Use the export command to set an environment variable.
```bash
joachim@my-pc:~$ export MY_VAR="Hello, World!"
joachim@my-pc:~$ echo $MY_VAR
Hello, World!
```

---
## Piping

Use the | operator to pipe the output of one command as input to another.
```bash
joachim@my-pc:~$ ls -l | grep "file"
```
---
## Redirection

Use > to redirect output to a file and < to use a file as input.

```bash
joachim@my-pc:~$ ls > file_list.txt
joachim@my-pc:~$ wc -l < file_list.txt
```
---
## Searching within Files

Use the grep command to search for text within files.

```bash
joachim@my-pc:~$ grep "search_term" file.txt
```
---
## Finding Files

Use the find command to search for files and directories.
```bash
joachim@my-pc:~$ find /home/joachim -name "*.txt"
```

---
## Viewing Running Processes

Use the ps command to view running processes.

```bash
joachim@my-pc:~$ ps aux
```
---
## Killing Processes

Use the kill command to terminate a process.

```bash
joachim@my-pc:~$ kill 1234
```
---
## Create a script file and add commands.
```bash
joachim@my-pc:~$ nano myscript.sh
```
or 

```bash
joachim@my-pc:~$ vim myscript.sh
```
 
then write your script

```bash
#!/bin/bash
echo "Hello, World!"
```
---
## Running a Script

Make the script executable and run it`

```bash
joachim@my-pc:~$ chmod +x myscript.sh
joachim@my-pc:~$ ./myscript.sh
Hello, World!
```
