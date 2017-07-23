Fix git SSL certificate problem
----
When you face "`git clone`" error like this:  

	# git clone https://github.com/NanXiao/FreeBSD-101-Hacks.git
	Cloning into 'FreeBSD-101-Hacks'...
	fatal: unable to access 'https://github.com/NanXiao/FreeBSD-101-Hacks.git': SSL certificate problem: certificate is not yet valid

The simplest solution may be just disable `SSL` verification: 

	# git config --global http.sslVerify false

Reference:  
[SSL certificate rejected trying to access GitHub over HTTPS behind firewall](https://stackoverflow.com/questions/3777075/ssl-certificate-rejected-trying-to-access-github-over-https-behind-firewall).

	
	
