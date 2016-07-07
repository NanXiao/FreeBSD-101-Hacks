Kldstat command
----
On `FreeBSD`, you can use `kldstat` command to display the status of any files dynamically linked into the kernel:  

	# kldstat
	Id Refs Address            Size     Name
	 1    6 0xffffffff80200000 17bc6a8  kernel
	 2    1 0xffffffff81a11000 56c6     fdescfs.ko
	 3    1 0xffffffff81a17000 2ba8     uhid.ko

If you want more detailed info, you can use `-v` option:  

	# kldstat -v
	Id Refs Address            Size     Name
	 1    6 0xffffffff80200000 17bc6a8  kernel (/boot/kernel/kernel)
	 Contains modules:
	  Id Name
	  386 if_lo
	  398 newreno
	  373 elf32
	  372 elf64
	  374 shell
	.....

Reference:  
[KLDSTAT(8)](https://www.freebsd.org/cgi/man.cgi?kldstat(8)).

