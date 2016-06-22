Change the shell
----
If you were previously working on `Linux`, you may miss `Bash`, and not accustomed to `csh` which is shipped on `FreeBSD` by default. You can change the shell to `Bash` following the below instructions:  

(1) The `Bash` must already be installed on your `FreeBSD`, and its full path should also be included in `/etc/shells`. E.g:  

	 # pkg install bash
	Updating FreeBSD repository catalogue...
	FreeBSD repository is up-to-date.
	All repositories are up-to-date.
	The following 1 package(s) will be affected (of 0 checked):
	
	New packages to be INSTALLED:
	        bash: 4.3.42_1
	......

Then you will find the `Bash` path is presented in `/etc/shells` automatically:  

	 # cat /etc/shells
	# $FreeBSD: releng/10.3/etc/shells 59717 2000-04-27 21:58:46Z ache $
	#
	# List of acceptable shells for chpass(1).
	# Ftpd will not allow users to connect who are not using
	# one of these shells.
	
	/bin/sh
	/bin/csh
	/bin/tcsh
	/usr/local/bin/bash
	/usr/local/bin/rbash

(2) Execute `chsh -s /usr/local/bin/bash`:  

	# chsh -s /usr/local/bin/bash
	chsh: user information updated

After you login again, you can find the shell is `bash` now:  

	# echo $SHELL
	/usr/local/bin/bash

Reference:  
[Shells](https://www.freebsd.org/doc/handbook/shells.html).
	
   