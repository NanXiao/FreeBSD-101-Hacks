Search software
----
If you want to search a specified application, you can use "`pkg search`" command. For example:  

	# pkg search lsof
	lsof-4.90.b,8                  Lists information about open files (similar to fstat(1))
	p5-Unix-Lsof-0.0.5_2           Unix::Lsof -- a wrapper to the Unix lsof utility
If you want to know the software's path in the ports tree, you can use `-o` option:  

	# pkg search -o lsof
	sysutils/lsof                  Lists information about open files (similar to fstat(1))
	sysutils/p5-Unix-Lsof          Unix::Lsof -- a wrapper to the Unix lsof utility
In case the Ports Collection is already installed, you can employ `whereis` command:  

	# whereis lsof
	lsof: /usr/local/sbin/lsof /usr/local/man/man8/lsof.8.gz /usr/ports/sysutils/lsof

Another tricky method is using "`echo`" command:  

	# echo /usr/ports/*/*lsof*
	/usr/ports/distfiles/lsof_4.90B.freebsd.tar.bz2 /usr/ports/sysutils/lsof

Reference:  
[Finding Software](https://www.freebsd.org/doc/handbook/ports-finding-applications.html).


