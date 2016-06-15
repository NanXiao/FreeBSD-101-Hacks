Upgrade system
----
You should make use of "`freebsd-update`" utility to upgrade your system non-periodically to keep your system safe and not stale. E.g., after installing a fresh `10.3` version:  

	# freebsd-version -ku
	10.3-RELEASE
	10.3-RELEASE   
You should update the patches released by `FreeBSD` team:  

	# freebsd-update fetch install
When it is done, check the system version again:  

	# freebsd-version -ku
	10.3-RELEASE-p4
	10.3-RELEASE-p5
Yeap! your system is refreshed now!

References:  
[FreeBSD Man Pages](https://www.freebsd.org/cgi/man.cgi?query=freebsd-update&sektion=8);  
[What are the first commands I run after installing FreeBSD? Or How to patch FreeBSD? Or How to install ports on FreeBSD?](http://www.rhyous.com/2009/11/03/what-are-the-first-commands-i-run-after-installing-freebsd/).