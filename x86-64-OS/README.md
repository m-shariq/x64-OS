This code is for 64-bit opearting system and special thanks to the youtube channel series (https://www.youtube.com/playlist?list=PLZQftyCk7_SeZRitx5MjBKzTtvk0pHMtp). for the help in making this.

## Pre Requisite ## 
You need VS Code. link (https://code.visualstudio.com/download).
You need Docker. link (https://www.docker.com/products/docker-desktop).
You need qemu. link (https://qemu.weilnetz.de/w64/qemu-w64-setup-20210409.exe).
You need linux kernel for docker. link (https://docs.microsoft.com/en-us/windows/wsl/install-win10#step-4---download-the-linux-kernel-update-package).

## Get Started ##
First of all you have to open all the source code in your visual studio code (by opening vs code as an administrator) then you have to open terminal and open new command prompt to run the following commands in order:

1. Command 1: docker build buildenv -t myos-buildenv
2. Command 2: docker run --rm -it -v %cd%:/root/env myos-buildenv
3. Command 3: make build-x86_64
4. Command 4: exit
Before running 5th command, you must ensure that u have qemu in your paths in enviroment variables.
5. Command 5: qemu-system-x86_64 -cdrom dist/x86_64/kernel.iso

After all these you will get NUST logo on your screen in different coloring pattern. you can also make your own changing on screen by going to following folder. (src/impl/kernel/main.c)

## Conclude ##
If you consider any change in this, you can suggest it and also once again special thanks to (davidcallanan) on github.