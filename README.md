SMN900P_MI3_Kernel
==================

Sprint Samsung Note 3 Kernel based on MI3


################################################################################

1. How to Build
	- get Toolchain
		From android git server , codesourcery and etc ..
		 - arm-eabi-4.6
		
	- edit Makefile
		edit "CROSS_COMPILE" to right toolchain path(You downloaded).
		  EX)  CROSS_COMPILE= $(android platform directory you download)/android/prebuilt/linux-x86/toolchain/arm-eabi-4.6/bin/arm-eabi-
          Ex)  CROSS_COMPILE=/usr/local/toolchain/arm-eabi-4.6/bin/arm-eabi-          // check the location of toolchain
  	
		$ export ARCH=arm
		$ make msm8974_sec_defconfig VARIANT_DEFCONFIG=msm8974_sec_hltespr_defconfig DEBUG_DEFCONFIG= SELINUX_DEFCONFIG=selinux_defconfig  SELINUX_LOG_DEFCONFIG=selinux_log_defconfig TIMA_DEFCONFIG=tima_defconfig
		$ make

2. Output files
	- Kernel : arch/arm/boot/zImage
	- module : drivers/*/*.ko

3. How to Clean	
		$ make clean
################################################################################
