# SNES for DE1-SoC of MiSTer.

This is the port of [srg320's FpgaSnes](https://github.com/srg320/FpgaSnes) core.

## Installing
copy *.rbf to root of SD card. Put some ROMs (*.SCF/*.SMC/*.BIN) into SNES folder

## Developer notes:
// experimental porting - proof of concept - SNES on DE1-SoC
//  hardware abstraction module (based on MiSTer SNES Sorgelig release 20181208
//	 162718dc1af2180cae0432b775d2b103f497a0f8 - before move WRAM to BRAM 
//  version, otherwise does not fit to 5CSEMA5F31C6 FPGA chip
//  with cyclone V m10k block types. Cyclone III was used m9k
