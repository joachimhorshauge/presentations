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







