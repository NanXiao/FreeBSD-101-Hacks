Update Ports Collection
----
The stuff under `/usr/ports` is referred as Ports Collection, and we can employ `portsnap` command to update it:  

(1) If it is the first time to use `portsnap`, you should run following command:  

	# portsnap fetch extract
Otherwise, you can encounter errors as shown here:  

	......
	/usr/ports was not created by portsnap.
	You must run 'portsnap extract' before running 'portsnap update'.

(2) Hereafter, you only need to execute "`portsnap fetch update`" to update the Ports Collection.  

Reference:  
[Using the Ports Collection](https://www.freebsd.org/doc/handbook/ports-using.html);  
[A question about using portsnanp to upgrade ports tree](https://lists.freebsd.org/pipermail/freebsd-questions/2016-June/272255.html).