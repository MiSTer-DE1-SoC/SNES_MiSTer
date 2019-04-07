# SNES for DE1-SoC of MiSTer.

This is the port of SNES MiSTer Core and [srg320's FpgaSnes](https://github.com/srg320/FpgaSnes) core.

## Installing
copy *.rbf to root of SD card. Put some ROMs (*.SCF/*.SMC/*.BIN) into SNES folder

## Developer notes:
This SNES Core is experimental SNES release, because in the commits since the origin SNES project moved from WRAM to BRAM version, the SNES FPGA code, it does not fit to 5CSEMA5F31C6 FPGA chip with cyclone V m10k block types. The original srg320 project used Cyclone III which used m9k as block type with less FPGA memory usage, while DE10-Nano and DE10-Standard utilizing now 98% of FPGA  memory blocks using m10k for all dpram blocks defined in the latest builds, but DE1-Soc has a bit less FPGA memory cells if m10k the only way for using bi directional ram type, so went back to 162718dc1af2180cae0432b775d2b103f497a0f8 commit that used less FPGA memory, until DPRAM is the only supported RAM type in SNES Core.
