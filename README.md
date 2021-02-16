# FPGA_CryptoMining


Hardware Requirements:

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
