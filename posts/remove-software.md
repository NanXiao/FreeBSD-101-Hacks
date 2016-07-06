Remove software
----
After installing application, you can use "`pkg delete`" command to remove it:  

	# pkg delete lsof
	Checking integrity... done (0 conflicting)
	Deinstallation has been requested for the following 1 packages (of 0 packages in the universe):
	
	Installed packages to be REMOVED:
	        lsof-4.90.b,8
	
	Proceed with deinstalling packages? [y/N]: y
	[1/1] Deinstalling lsof-4.90.b,8...
	[1/1] Deleting files for lsof-4.90.b,8: 100%
You can also enter the port directory, and execute "`make deinstall`" instruction:  

	# pwd
	/usr/ports/sysutils/lsof
	# make deinstall
	===>  Deinstalling for lsof
	===>   Deinstalling lsof-4.90.b,8
	Updating database digests format: 100%
	Checking integrity... done (0 conflicting)
	Deinstallation has been requested for the following 1 packages (of 0 packages in the universe):
	
	Installed packages to be REMOVED:
	        lsof-4.90.b,8
	[1/1] Deinstalling lsof-4.90.b,8...
	[1/1] Deleting files for lsof-4.90.b,8: 100%

Reference:  
[Using the Ports Collection](https://www.freebsd.org/doc/handbook/ports-using.html).