Shutdown
----
Compared to some `GNU/Linux` flavors, "`shutdown -h now`" command just halts the `FreeBSD`, not turns off the power. Refer the following screen shot from my Virtual Machine:  
![image](https://raw.githubusercontent.com/NanXiao/FreeBSD-101-Hacks/master/images/shutdown-h-now.JPG)  
You can see, after running "`shutdown -h now`", the system is just halted, and press any key can reboot the system immediately.  

If you want to halt and power off the system, you should execute "`shutdown -p now`".

Reference:  
<a href="https://www.freebsd.org/cgi/man.cgi?shutdown(8)">SHUTDOWN</a>.