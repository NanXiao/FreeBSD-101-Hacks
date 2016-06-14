Get system version
----
There are `2` versions of `FreeBSD`: kernel and userland. Use "`freebsd-version -ku`" can output both versions:  

	# freebsd-version -uk
	10.3-RELEASE-p4
	10.3-RELEASE-p5
The first one is kernel version info. You can see the versions of both kernel and userland is `10.3`, but kernel patch level is `p4`, while userland is `p5`. That's because in some cases, only the userland requires a patch whilst kernel not, so kernel patch level doesn't change. If there is no option, "`freebsd-version`" prints userland version only:  

	# freebsd-version
	10.3-RELEASE-p5
 

"`uname -r`" command also outputs the kernel version:  

	# uname -r
	10.3-RELEASE-p4

Reference:  
[Why the outputs of “freebsd-version” and “freebsd-version -k” are different?](http://stackoverflow.com/questions/37800913/why-the-outputs-of-freebsd-version-and-freebsd-version-k-are-different).