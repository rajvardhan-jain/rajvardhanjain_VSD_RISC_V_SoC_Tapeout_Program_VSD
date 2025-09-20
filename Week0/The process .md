RISC-V Reference SoC Tapeout Program VSD

Tools Installation
All the instructions for installation of required tools can be found here:

System Requirements
6 GB RAM
50 GB HDD
Ubuntu 20.04 or higher
4 vCPU
(Please use virtual box only if you have only 1 ssd, it will save you 2 days)

Resizing the Ubuntu window to fit the screen
$ sudo apt update
$ sudo apt install build-essential dkms linux-headers-$(uname -r)
$ cd /media/spatha/VBox_GAs_7.1.8/
$ ./autorun.sh

TOOL CHECK
Yosys
$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make               # If make is not installed
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ sudo make install

![Yosys](https://github.com/user-attachments/assets/dd4615af-6c7d-4e9b-a912-626cc146898f)

Iverilog
$ sudo apt-get update
$ sudo apt-get install iverilog

![iverilog](https://github.com/user-attachments/assets/35229939-8da8-4319-ae36-b37b5af6b1f5)

gtkwave
$ sudo apt-get update
$ sudo apt install gtkwave

![gtkwave](https://github.com/user-attachments/assets/07e8b15e-1ccd-4055-ac37-37350e7a2d5c)




