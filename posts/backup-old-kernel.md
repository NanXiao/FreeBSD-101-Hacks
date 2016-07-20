Backup old kernel
----
Every time, when a new kernel is installed, the last installed kernel will be backed up in a directory who is called `kernel.old`. So it is important to remember to save a copy of usable kernel in case the newly-built kernel can't work. For example:  

	# mv /boot/kernel.old /boot/kernel.good	
	# mv /boot/kernel /boot/kernel.bad
	# mv /boot/kernel.good /boot/kernel

During boot, you can press `5` to select which kernel to run:  
![image](https://raw.githubusercontent.com/NanXiao/FreeBSD-101-Hacks/master/images/boot_kernel.JPG)
![image](https://raw.githubusercontent.com/NanXiao/FreeBSD-101-Hacks/master/images/boot_old_kernel.JPG)
	