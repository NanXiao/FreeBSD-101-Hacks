Install source code
----
Download `FreeBSD` source code according architecture, version:  

	fetch ftp://ftp.freebsd.org/pub/`uname -s`/releases/`uname -m`/`uname -r | cut -d'-' -f1,2`/src.txz

Uncompress the source package:  

	tar -C / -xvzf src.txz
Make sure the `src` is included in `Components` line in `/etc/freebsd-update.conf`, so when using `freebsd-update` to update system, also the source code is refreshed. 

	# cat /etc/freebsd-update.conf
	......
	# Components of the base system which should be kept updated.
	Components src world kernel
	......


References:  
[A question about downloading FreeBSD kernel code](https://lists.freebsd.org/pipermail/freebsd-questions/2016-July/272497.html);  
[Install FreeBSD kernel source after installed freebsd](https://www.netroby.com/view/3595).