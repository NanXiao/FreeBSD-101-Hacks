# Enable root login over SSH
----
By default, `FreeBSD` box doesn't allow `root` user login over `SSH`, to enable it, you need to modify `SSH` daemon configuration file (`/etc/ssh/sshd_config`).  

Change the following line:  

	#PermitRootLogin no
to: 
 
	PermitRootLogin yes
Then restart `SSH` daemon:  

	# /etc/rc.d/sshd restart
Reference:  
[How to enable root login over SSH on FreeBSD 8.2](http://blog.bobbyallen.me/2011/07/22/how-to-enable-root-login-over-ssh-on-freebsd-8-2/).