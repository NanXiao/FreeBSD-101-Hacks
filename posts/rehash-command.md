Rehash command
----
After removing the application in the directory listed in the `$PATH` variable, you  may even see the command prompt when you type the first characters:  

	# pkg delete lsof
	Checking integrity... done (0 conflicting)
	Deinstallation has been requested for the following 1 packages (of 0 packages in the universe):
	
	Installed packages to be REMOVED:
	        lsof-4.90.b,8
	
	Proceed with deinstalling packages? [y/N]: y
	[1/1] Deinstalling lsof-4.90.b,8...
	[1/1] Deleting files for lsof-4.90.b,8: 100%
	# ls
	ls        ls-F      lsextattr lsof      lspci     lsvfs
While running it will prompt "`Command not found.`" definitely:  

	# lsof
	lsof: Command not found.
Np matter install or remove application , you need to run `rehash` command in `csh` to causes the shell to recompute a table of where commands are located.  

Reference:  
[Misc Tips & Tricks](http://www.freebsdmadeeasy.com/tutorials/freebsd/freebsd-tricks.php);  
[Rehash](http://www.panix.com/~spkemp/examplex/csh/rehash.htm).




 