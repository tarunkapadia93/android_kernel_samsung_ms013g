################################################################################
HOW TO BUILD KERNEL FOR SM-G7102_CIS

1. How to Build
	- get Toolchain
	download and install arm-eabi-4.7 toolchain for ARM EABI.
	Extract kernel source and move into the top directory.

	$ make VARIANT_DEFCONFIG=msm8226-sec_ms013g_eur_defconfig msm8226-sec_defconfig SELINUX_DEFCONFIG=selinux_defconfig 
	$ make
	
2. Output files
	- Kernel : Kernel/arch/arm/boot/zImage
	- module : Kernel/drivers/*/*.ko
	
3. How to Clean	
    $ make clean
	
4. How to make .tar binary for downloading into target.
	- change current directory to Kernel/arch/arm/boot
	- type following command
	$ tar cvf SM-G7102_CIS.tar zImage
#################################################################################