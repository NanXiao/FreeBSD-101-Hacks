Shutdown
----
Compared to some `GNU/Linux` flavors, "`shutdown -h now`" command just halts the `FreeBSD`, not turns off the power. Refer the following screen shot from my Virtual Machine:  
![image](images/shutdown-h-now.jpg)  
You can see, after running "`shutdown -h now`", the system is just halted, and press any key can reboot the system immediately.  

If you want to halt and power off the system, you should execute "`shutdown -p now`".

Reference:  
[SHUTDOWN](https://www.freebsd.org/cgi/man.cgi?shutdown(8)).