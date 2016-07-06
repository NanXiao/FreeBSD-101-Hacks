Change PATH environment variable
----
In `csh`, if you want to change `$PATH` environment variable, you should modify `.cshrc` file:  

	# cat .cshrc
	......
	set path = (/sbin /bin /usr/sbin /usr/bin /usr/games /usr/local/sbin /usr/local/bin $HOME/bin $HOME/gocode/bin)
	......
For example, you add "`/usr/local/go/bin`" into `$PATH`:  

	# cat .cshrc
	......
	set path = (/sbin /bin /usr/sbin /usr/bin /usr/games /usr/local/sbin /usr/local/bin $HOME/bin $HOME/gocode/bin /usr/local/go/bin)
	......

Then executing "`source .cshrc`" command, you will find the new `$PATH` takes effect:  

	 # source .cshrc
	# echo $PATH
	/sbin:/bin:/usr/sbin:/usr/bin:/usr/games:/usr/local/sbin:/usr/local/bin:/root/bin:/root/gocode/bin:/usr/local/go/bin

Reference:  
[Misc Tips & Tricks](http://www.freebsdmadeeasy.com/tutorials/freebsd/freebsd-tricks.php).