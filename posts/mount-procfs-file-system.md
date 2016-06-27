Mount procfs file system
----
`FreeBSD` doesn't mount `procfs` file system by default, if you need it, you can mount it yourself:  

	mount -t procfs proc	/proc
If you want the `procfs` is automatically mounted at boot time, you can add the following line in `/etc/fstab` file: 

	proc	     /proc   procfs  rw	0 0  

References:  
[procfs: Gone But Not Forgotten](https://www.freebsd.org/doc/en/articles/linux-users/procfs.html);  
[procfs -- process file system](https://www.freebsd.org/cgi/man.cgi?query=procfs&sektion=&n=1).


 