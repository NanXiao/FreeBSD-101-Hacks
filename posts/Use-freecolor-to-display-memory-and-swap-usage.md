Use "freecolor" to display memory and swap usage
----
`Freecolor` on `FreeBSD` is equal to `free` on `GNU/Linux`. Install it:  

	# cd /usr/ports/sysutils/freecolor
	# make install clean 

Display the memory and swap usage in bar format:  

	# freecolor
	Physical  : [#################################..] 94%   (1907820/2018396)
	Swap      : [###################################] 100%  (1048540/1048540)

Display usage in traditional "`free`" format:  

	# freecolor -m -o
	             total       used       free     shared    buffers     cached
	Mem:          1971        107       1863          0          0          0
	Swap:         1023          0       1023
Reference:  
[FreeBSD find out RAM size Including Total Amount of Free and Used Memory Size](http://www.cyberciti.biz/faq/freebsd-command-to-get-ram-information/).