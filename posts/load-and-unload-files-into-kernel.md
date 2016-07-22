Load and unload files into kernel
----
You can use `kldload` command to load files into kernel. For example, enter `/boot/kernel` directory, and use `kldstat` to check currently loaded files:  

	# cd /boot/kernel
	# kldstat
	Id Refs Address            Size     Name
	 1    6 0xffffffff80200000 17bc6a8  kernel
	 2    1 0xffffffff81a11000 56c6     fdescfs.ko
	 3    1 0xffffffff81a17000 2ba8     uhid.ko
Use `kldload` to load `zfs.ko` file:  

	# kldload zfs.ko
	# kldstat
	Id Refs Address            Size     Name
	 1   15 0xffffffff80200000 17bc6a8  kernel
	 2    1 0xffffffff81a11000 56c6     fdescfs.ko
	 3    1 0xffffffff81a17000 2ba8     uhid.ko
	 7    1 0xffffffff81a1a000 1ee0c8   zfs.ko
	 8    1 0xffffffff81c09000 3330     opensolaris.ko
You can see the `zfs.ko` is loaded successfully.  

Unloading file uses `kldunload` command:  

	# kldunload zfs.ko
	# kldstat
	Id Refs Address            Size     Name
	 1    6 0xffffffff80200000 17bc6a8  kernel
	 2    1 0xffffffff81a11000 56c6     fdescfs.ko
	 3    1 0xffffffff81a17000 2ba8     uhid.ko


Reference:  
<a href="https://www.freebsd.org/cgi/man.cgi?kldload(8)">kldload</a>;  
<a href="https://www.freebsd.org/cgi/man.cgi?kldunload(8)">kldunload</a>.  
