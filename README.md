# Mini Shell 💻

Final project of the course Operative Systems I, from UIB. This project was made with the collaboration of [Marc Link](https://github.com/linkcla) and [Carlos Gálvez](https://github.com/Carlgm-18) 🫱🏽‍🫲🏽.

This is only the last part of the project, which was developed by levels and can be found [here](https://github.com/jcasben/Programacion-Ing-Informatica/tree/master/2-Ing-Informatica/1-Cuatrimestre/sistemas-operativos-I/practica2).

## Overview 🔍

This project consists in a minimal version of a shell where we can execute some internal commands that we developed and the rest of the commands that can be executed on Linux. With this shell we can also stop processes and then restart them in the foreground or in the background.

## Getting it started 🚀

1. First of all, you have to clone this repository. You can do it this way opening a terminal on the desired directory:

```bash
git clone https://github.com/jcasben/mini_shell.git
```

2. Once you have it, you can run this command to make an executable of the program:

```bash
make mini_shell
```

3. Now you can execute the program:

```bash
./mini_shell
```

**IMPORTANT:** this project was made on top of WSL (Windows Subsystem for Linux), so it only works on linux based operative systems.

## Functionalities ⚙️

Our mini shell has some self implemented methods, which are the following ones:

- cd: it changes the directory where we are located. It also has the implementation of accepting paths with white spaces. Usage: cd \<path>

- export: sets values for enviroment variables such as USER. Usage: export \<variable>=\<value>

- source: executes all the commands that are written in a file. Usage: source \<path-to-file>

- jobs: displays the jobs list, where the background processes are "stored". Usage: jobs

- fg: brings a background or stopped process to the foreground. Usage: fg \<job-number>

- bg: reactivates an stopped process and leaves it in the background. Usage: bg \<job-number>

This shell also can execute any other linux command thanks to the `execvp()` function, which creates a child process that executes this command while the parent waits it to finish. More information about this function [here](https://www.qnx.com/developers/docs/6.5.0SP1.update/com.qnx.doc.neutrino_lib_ref/e/execvp.html).

- You can stop a process using the combination Ctrl + Z
- To exit the mini shell, you can use the command `exit` or the combination Ctrl + D.