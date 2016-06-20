Use "ps" to display process status
----
If you run "`ps`" command without any options, it will only show **your** processes who have a controlling terminal:  

	# ps
	PID TT  STAT    TIME COMMAND
	854 v0  Is+  0:00.00 /usr/libexec/getty Pc ttyv0
	710 v1  Is+  0:00.00 /usr/libexec/getty Pc ttyv1
	711 v2  Is+  0:00.00 /usr/libexec/getty Pc ttyv2
	712 v3  Is+  0:00.00 /usr/libexec/getty Pc ttyv3
	713 v4  Is+  0:00.00 /usr/libexec/getty Pc ttyv4
	714 v5  Is+  0:00.00 /usr/libexec/getty Pc ttyv5
	715 v6  Is+  0:00.00 /usr/libexec/getty Pc ttyv6
	716 v7  Is+  0:00.00 /usr/libexec/getty Pc ttyv7
	847  0  Ss   0:00.04 -csh (csh)
	883  0  R+   0:00.00 ps
If you also want to see processes who don't have a controlling terminal, add "`-x`" option:  

	# ps -ax
	PID TT  STAT     TIME COMMAND
	  0  -  DLs   0:00.10 [kernel]
	  1  -  ILs   0:00.05 /sbin/init --
	  2  -  DL    0:00.05 [cam]
	  3  -  DL    0:00.00 [mpt_recovery0]
	  4  -  DL    0:00.00 [sctp_iterator]
	  5  -  DL    0:00.04 [pagedaemon]
	  6  -  DL    0:00.00 [vmdaemon]
	  7  -  DL    0:00.00 [pagezero]
	  8  -  DL    0:00.08 [bufdaemon]
	  9  -  DL    0:00.01 [vnlru]
	 10  -  DL    0:00.00 [audit]
	 11  -  RL   50:35.75 [idle]
	 12  -  WL    0:08.20 [intr]
	 13  -  DL    0:00.02 [geom]
	 14  -  DL    0:00.91 [rand_harvestq]
	 15  -  DL    0:00.44 [usb]
	 16  -  DL    0:00.20 [syncer]
	302  -  Is    0:00.01 dhclient: em0 [priv] (dhclient)
	364  -  Is    0:00.00 dhclient: em0 (dhclient)
	379  -  Is    0:00.00 /sbin/devd
	524  -  Ss    0:00.02 /usr/sbin/syslogd -s
	652  -  Is    0:00.00 /usr/sbin/sshd
	655  -  Ss    0:00.10 sendmail: accepting connections (sendmail)
	658  -  Is    0:00.00 sendmail: Queue runner@00:30:00 for /var/spool/clientmqueue (sendmail)
	662  -  Ss    0:00.01 /usr/sbin/cron -s
	844  -  Ss    0:00.06 sshd: root@pts/0 (sshd)
	854 v0  Is+   0:00.00 /usr/libexec/getty Pc ttyv0
	710 v1  Is+   0:00.00 /usr/libexec/getty Pc ttyv1
	711 v2  Is+   0:00.00 /usr/libexec/getty Pc ttyv2
	712 v3  Is+   0:00.00 /usr/libexec/getty Pc ttyv3
	713 v4  Is+   0:00.00 /usr/libexec/getty Pc ttyv4
	714 v5  Is+   0:00.00 /usr/libexec/getty Pc ttyv5
	715 v6  Is+   0:00.00 /usr/libexec/getty Pc ttyv6
	716 v7  Is+   0:00.00 /usr/libexec/getty Pc ttyv7
	847  0  Ss    0:00.04 -csh (csh)
	897  0  R+    0:00.00 ps -ax

This time, there are more results whose `TT` columns are `-`.  

The most used "`ps`" command is "`ps auwwx`" which displays all running processes detailed info, and this is similar to "`# ps -ef`" on `GNU/Linux`:  

 	# ps auwwx
	USER  PID %CPU %MEM   VSZ  RSS TT  STAT STARTED     TIME COMMAND
	root   11 99.2  0.0     0   16  -  RL    5:48PM 54:14.29 [idle]
	root    0  0.0  0.0     0  160  -  DLs   5:48PM  0:00.10 [kernel]
	root    1  0.0  0.0  9492  772  -  ILs   5:48PM  0:00.05 /sbin/init --
	root    2  0.0  0.0     0   32  -  DL    5:48PM  0:00.05 [cam]
	root    3  0.0  0.0     0   16  -  DL    5:48PM  0:00.00 [mpt_recovery0]
	root    4  0.0  0.0     0   16  -  DL    5:48PM  0:00.00 [sctp_iterator]
	root    5  0.0  0.0     0   32  -  DL    5:48PM  0:00.05 [pagedaemon]
	root    6  0.0  0.0     0   16  -  DL    5:48PM  0:00.00 [vmdaemon]
	root    7  0.0  0.0     0   16  -  DL    5:48PM  0:00.00 [pagezero]
	root    8  0.0  0.0     0   32  -  DL    5:48PM  0:00.08 [bufdaemon]
	root    9  0.0  0.0     0   16  -  DL    5:48PM  0:00.01 [vnlru]
	root   10  0.0  0.0     0   16  -  DL    5:48PM  0:00.00 [audit]
	root   12  0.0  0.0     0  208  -  WL    5:48PM  0:08.78 [intr]
	root   13  0.0  0.0     0   48  -  DL    5:48PM  0:00.02 [geom]
	root   14  0.0  0.0     0   16  -  DL    5:48PM  0:00.98 [rand_harvestq]
	root   15  0.0  0.0     0  160  -  DL    5:48PM  0:00.47 [usb]
	root   16  0.0  0.0     0   16  -  DL    5:48PM  0:00.21 [syncer]
	root  302  0.0  0.1 14656 2148  -  Is    5:48PM  0:00.01 dhclient: em0 [priv] (dhclient)
	_dhcp 364  0.0  0.1 14656 2236  -  Is    5:48PM  0:00.00 dhclient: em0 (dhclient)
	root  379  0.0  0.2 13628 4932  -  Ss    5:48PM  0:00.00 /sbin/devd
	root  524  0.0  0.1 14520 2092  -  Ss    5:48PM  0:00.02 /usr/sbin/syslogd -s
	root  652  0.0  0.3 61316 6564  -  Is    5:48PM  0:00.00 /usr/sbin/sshd
	root  655  0.0  0.3 24156 5380  -  Ss    5:48PM  0:00.10 sendmail: accepting connections (sendmail)
	smmsp 658  0.0  0.2 24156 5044  -  Is    5:48PM  0:00.00 sendmail: Queue runner@00:30:00 for /var/spool/clientmqueue (sendmail)
	root  662  0.0  0.1 16624 2212  -  Is    5:48PM  0:00.01 /usr/sbin/cron -s
	 
References:  
[ps	-- process status](https://www.freebsd.org/cgi/man.cgi?query=ps&sektion=1&manpath=freebsd-release-ports);  
[Processes and Daemons](https://www.freebsd.org/doc/handbook/basics-processes.html);  
[Show all processes in FreeBSD](http://raghukumarc.blogspot.com/2011/11/show-all-processes-in-freebsd.html).