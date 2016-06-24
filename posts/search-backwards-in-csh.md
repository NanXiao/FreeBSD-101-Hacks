Search backwards in csh
----
In `bash`, `Ctrl + R` provides the handy "search backwards" feature which isn't shipped by `csh` by default. If you want to use the similar function in `csh`, you can employ `csh` built-in `bindkey` command to implement it:  

	# cat .cshrc
	......

	bindkey "^R" i-search-back
Then you can use "search backwards" when pressing `Ctrl + R`:

	root@FreeBSD:~ # pkg install subversion   
	bck:pk

References:  
[Ctrl-R to search backwards for shell commands in csh](http://stackoverflow.com/questions/1387357/ctrl-r-to-search-backwards-for-shell-commands-in-csh).