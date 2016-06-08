# Configure proxy
----

If your `FreeBSD` box works behind a proxy, you may need to configure proxy to make it access network.  

For `csh` or `tcsh`, set proxy in `/etc/csh.cshrc`:  

	setenv HTTP_PROXY http://web-proxy.xxxxxx.com:8080
	setenv HTTPS_PROXY https://web-proxy.xxxxxx.com:8080
For `sh`, set proxy in `/etc/profile`:  

	export HTTP_PROXY http://web-proxy.xxxxxx.com:8080
	export HTTPS_PROXY https://web-proxy.xxxxxx.com:8080

Reference:  
[Using FreeBSD inside a controlled network – A required HTTP Proxy and No FTP](http://www.rhyous.com/2012/04/13/using-freebsd-inside-a-controlled-network-a-required-http-proxy-and-no-ftp/).