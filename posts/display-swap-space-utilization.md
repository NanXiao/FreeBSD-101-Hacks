Display swap space utilization
----
On `FreeBSD`, you can use `pstat -s` to display swap space utilization:  

	# pstat -s
	Device          1K-blocks     Used    Avail Capacity
	/dev/da0p3        1048540        0  1048540     0%
There is another specified `swapinfo` command you can use:  

	# swapinfo
	Device          1K-blocks     Used    Avail Capacity
	/dev/da0p3        1048540        0  1048540     0%

You can also display swap info in "Human-readable" format:  

	# swapinfo -h
	Device          1K-blocks     Used    Avail Capacity
	/dev/da0p3        1048540       0B     1.0G     0%

Or display swap space size in megabyte unit:  

	# swapinfo -m
	Device          1M-blocks     Used    Avail Capacity
	/dev/da0p3           1023        0     1023     0%

References:  
[PSTAT](https://www.freebsd.org/cgi/man.cgi?query=swapinfo&sektion=8).


	