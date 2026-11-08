# FPGA_CryptoMining


Hardware Requirements:

## 📖 The Book

This project is **Chapter 13, "FPGA Crypto Mining"**, in a book:

**Chips, Code, and Cartridges: Turn Curiosity into Creation with 13 Hands-On Projects, from 8-bit Classics to FPGAs**

It walks through thirteen of my own hardware and software projects, from 8-bit classics to FPGAs, for beginners and curious makers. Each chapter explains how one project works and how to build it, with colour diagrams and real code from its repository.

### 👉 [Get the book on Amazon](https://link.amazon/B013Yaq9y)

<sub>As an Amazon Associate, the author earns from qualifying purchases. Buying through this link
supports these projects at no extra cost to you.</sub>

FPGA Dev Board Altera DE-10 Nano
PC with Windows 10.


Software Requirements:

FPGA Dev Board Altera DE-10 Nano
Windos 10
Cygwin
Python 3.7.9 (will not work with Python 3.9)
pip 21.0 from /usr/lib/python3.7/site-packages/pip (python 3.7)
Altera Quartus Lite 18.1


Use a Cygwin shell window to run the mining software.

Set the following environment variables:

export QSYS_ROOTDIR="/cygdrive/c/intelFPGA_lite/18.1/quartus/sopc_builder/bin"
export QUARTUSPATH="/cygdrive/c/intelFPGA_lite/18.1/quartus/bin64"


Open one cygwin window, and run:

cd ./src
./autocompile.sh de10_nano


Open another cygwin window, and run:
(edit and add user pool username, or Digibyte Address before running)

cd ./src/pool/stratum
./mine.sh


Open another cygwin window and run:
cd ./src/miner
$QUARTUSPATH/quartus_stp.exe -t mine.tcl


# Mining pool used for this build: https://odo.dgb256.online/
