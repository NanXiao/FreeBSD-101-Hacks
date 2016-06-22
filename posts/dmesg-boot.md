/var/run/dmesg.boot
----
`/var/run/dmesg.boot` file contains the `FreeBSD` boot messages, and this is very helpful for checking hardware related info:  

	# cat /var/run/dmesg.boot | grep -i CPU
	CPU: Intel(R) Core(TM) i5-4310U CPU @ 2.00GHz (2594.03-MHz K8-class CPU)
	cpu0: <ACPI CPU> on acpi0
Because the capacity of system message buffer is limited, `FreeBSD` employs `/var/run/dmesg.boot` in case the content of buffer is flushed.  

References:  
[Devices and Device Nodes](https://www.freebsd.org/doc/handbook/basics-devices.html);  
[Back To Basics: Unix Differences in Performing Tasks](http://www.longitudetech.com/linux-unix/back-to-basics-unix-differences-in-performing-tasks/). 