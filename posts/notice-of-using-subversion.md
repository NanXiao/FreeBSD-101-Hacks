Notices of using Subversion
----
If you want to use `Subversion`, for example, updating ports tree, you should pay attention to the following issues:  

(1) If your server works behind a proxy, you should modify your `Subversion` configuration file:  

	# cat ~/.subversion/servers
	[global]
	http-proxy-host = web-proxy.xxxx.com
	http-proxy-port = 8080
	http-compression = no
Otherwise, you may encounter following errors:  

	# svn checkout https://svn.FreeBSD.org/ports/head /usr/ports
	Error validating server certificate for 'https://svn.freebsd.org:443':
	 - The certificate is not issued by a trusted authority. Use the
	   fingerprint to validate the certificate manually!
	 - The certificate hostname does not match.
	Certificate information:
	 - Hostname: FG3K6C3A15800021
	 - Valid: from Mar 21 09:15:26 2015 GMT until Mar 21 09:15:26 2025 GMT
	 - Issuer: FG3K6C3A15800021, Fortinet Ltd.
	 - Fingerprint: 1D:F4:21:20:2F:06:41:45:3F:7A:18:FB:79:F3:BB:30:36:32:22:A3
	(R)eject, accept (t)emporarily or accept (p)ermanently? p
	svn: E170013: Unable to connect to a repository at URL 'https://svn.freebsd.org/ports/head'
	svn: E000054: Error running context: Connection reset by peer
Or:  

	# svn checkout https://svn.FreeBSD.org/ports/head /usr/ports
	......
	svn: E175002: REPORT request on '/ports/!svn/me' failed

(2) If you meet similar errors like as follows executing `svn` command:  

	svn: E200030: SQLite compiled for 3.11.1, but running with 3.9.2
You should update your `SQLite`:  

	# pkg upgrade sqlite3

References:  
[Using FreeBSD inside a controlled network – A required HTTP Proxy and No FTP](http://www.rhyous.com/2012/04/13/using-freebsd-inside-a-controlled-network-a-required-http-proxy-and-no-ftp/);  
[How to configure a HTTP proxy for svn](http://stackoverflow.com/questions/1491180/how-to-configure-a-http-proxy-for-svn).