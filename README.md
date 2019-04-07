# SNES for DE1-SoC of MiSTer.

This is the port of [srg320's FpgaSnes](https://github.com/srg320/FpgaSnes) core.

## Installing
copy *.rbf to root of SD card. Put some ROMs (*.SCF/*.SMC/*.BIN) into SNES folder

## Developer notes:
This SNES Core is experimental release - SNES on DE1-SoC hardware abstraction module (based on MiSTer SNES Sorgelig release 20181208 162718dc1af2180cae0432b775d2b103f497a0f8 - before move WRAM to BRAM version, otherwise SNES FPGA code does not fit to 5CSEMA5F31C6 FPGA chip with cyclone V m10k block types. The original srg320 project used Cyclone III which used m10k as block type, DE10-Nano and DE10-Standard can use m9k for all dpram blocks defined in the latest builds, but DE1-Soc has less LE-s, so went back to 162718dc1af2180cae0432b775d2b103f497a0f8 commit.
