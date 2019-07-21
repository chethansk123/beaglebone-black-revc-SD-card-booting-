# beaglebone-black-revc-SD-card-booting-
procedure of booting BBB from SD card and the files required for successful booting.
BEAGLEBONE BLACK REV C

1	LUNUX SD CARD BOOTING PROCESS

As per the AM335x processor the mode of booting priorities based on the switch S2 on board have two boot configurations.

1.	S2 Released (SYSBOOT[4:0]=11100)
    The boot order will be 
    1.	MMC1 (eMMC)
    2.	MMC0 (SD card)
    3.	UART0
    4.	USB0
2.	S2 pressed (SYSBOOT[4:0]=11100)
    The boot order will be 
    1.	SPI0
    2.	MMC0(SD card)
    3.	USB0
    4.	UART0
  
Procedure for booting Linux from SD card :

1.	Take SD card of minimum capacity of 4GB and it has to be partitioned into two sections. 
2.	One is a BOOT section of 1 GB capacity and another one as ROOT file system of remaining space. BOOT section Partition is a     type of FAT32 and ROOT file system partition is a type of ext3.
3.	The available files MLO, uboot and Env files should be copied to the BOOT partition of the SD card.
4.	The complete Linux image files and board .dtb file should be copied to the ROOT file system partition.
