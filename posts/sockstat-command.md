Sockstat command
----
On `FreeBSD`, we can employ `sockstat` command to list both open Internet and `UNIX `domain sockets:  

	# sockstat
	USER     COMMAND    PID   FD PROTO  LOCAL ADDRESS         FOREIGN ADDRESS
	root     sshd       45768 3  tcp4   192.168.80.129:22     192.168.80.1:60803
	root     sshd       22144 3  tcp4   192.168.80.129:22     192.168.80.1:54834
	root     sshd       19097 3  tcp4   192.168.80.129:22     192.168.80.1:58174
	smmsp    sendmail   662   3  dgram  -> /var/run/log
	root     sendmail   659   3  tcp4   127.0.0.1:25          *:*
	root     sendmail   659   4  dgram  -> /var/run/logpriv
	root     sshd       656   3  tcp6   *:22                  *:*
	root     sshd       656   4  tcp4   *:22                  *:*
	......

We can see the output of `sockstat` lists which process owns the socket, the file descriptor number of the socket, etc. So it is a really awesome tool to diagnose network related issues.  

Reference:  
[SOCKSTAT(1)](https://www.freebsd.org/cgi/man.cgi?query=sockstat&sektion=1).


