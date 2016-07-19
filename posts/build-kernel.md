Build kernel
----
If you want to build a custom kernel yourself, you need to install the source code firstly (you can take [post](../posts/install-source-code.md) as a reference). Then enter the configuration directory of your machine:  

	# cd /usr/src/sys/`uname -m`/conf

Copy a new kernel configuration file:  

	# cp GENERIC NAN_FIRST_BUILD
You can modify the new configuration file (`NAN_FIRST_BUILD`) according to your needs.   

Build the kernel:  

	# cd /usr/src
	# make buildkernel KERNCONF="NAN_FIRST_BUILD"

Once it is finished, install the fresh kernel binary and reboot: 

	# make installkernel KERNCONF="NAN_FIRST_BUILD"
	# reboot

Check the kernel version, you will find now the OS is harnessing your newly built kernel now:  

	# uname -a
	FreeBSD FreeBSD 10.3-RELEASE-p5 FreeBSD 10.3-RELEASE-p5 #0: Tue Jul 19 17:52:57 CST 2016     root@FreeBSD:/usr/obj/usr/src/sys/NAN_FIRST_BUILD  amd64

Reference:  
[How to build a custom kernel in FreeBSD](https://www.youtube.com/watch?v=KVNxaKu11F0).
	

	
	