Upgrade to new release
----
This article takes upgrading system from `10.2-RELEASE` to `10.3-RELEASE` as an example, but you must notice this tutorial may **not** apply to other versions. So please read the related release notes.  

(1) Check current version:  

	# freebsd-version -ku
	10.2-RELEASE
	10.2-RELEASE

(2) Run "`freebsd-update upgrade`" command to upgrade current system to a new version:  

	# freebsd-update upgrade -r 10.3-RELEASE
	......
	To install the downloaded upgrades, run "/usr/sbin/freebsd-update install".
(3) The last log of "`freebsd-update upgrade -r 10.3-RELEASE`" prompts executing "`freebsd-update install`":  

	# freebsd-update install
	src component not installed, skipped
	Installing updates...
	Kernel updates have been installed.  Please reboot and run
	"/usr/sbin/freebsd-update install" again to finish installing updates.

(4) Reboot the system and execute "`freebsd-update install`" again:  

	# reboot
	# freebsd-update install
	src component not installed, skipped
	Installing updates... done.

(5) Now check the version: 

	# freebsd-version -ku
	10.3-RELEASE-p4
	10.3-RELEASE-p5
The system has been upgraded to `10.3-RELEASE` now.  

Reference:  
[freebsd-update](https://www.freebsd.org/cgi/man.cgi?freebsd-update);  
[FreeBSD 10.3-RELEASE Installation Instructions](https://www.freebsd.org/releases/10.3R/installation.html).