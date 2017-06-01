Install software
----
If you don't have any specific requirements for needed software, you can use `pkg` utility to install the pre-built package on `FreeBSD`, and it looks like using `yum` or `apt-get` on `GNU/Linux` boxes. E.g., install `python` on your host:  

	# pkg install python 
	......
	===========================================================================

	Note that some standard Python modules are provided as separate ports
	as they require additional dependencies. They are available as:
	
	bsddb           databases/py-bsddb
	gdbm            databases/py-gdbm
	sqlite3         databases/py-sqlite3
	tkinter         x11-toolkits/py-tkinter
	
	===========================================================================
Now you can run `python` now:  

    # python
    Python 2.7.11 (default, Jun  5 2016, 01:23:11)
    [GCC 4.2.1 Compatible FreeBSD Clang 3.4.1 (tags/RELEASE_34/dot1-final 208032)] on freebsd10
    Type "help", "copyright", "credits" or "license" for more information.
    >>>
But the end logs of installing `python` prompts we still need to install other `4` packages: `py-bsddb`, `py-gdbm`, `py-sqlite3` and `py-tkinter`, otherwise "`import sqlite3`" will complain:  

	>>> import sqlite3
	Traceback (most recent call last):
	  File "<stdin>", line 1, in <module>
	  File "/usr/local/lib/python2.7/sqlite3/__init__.py", line 24, in <module>
	    from dbapi2 import *
	  File "/usr/local/lib/python2.7/sqlite3/dbapi2.py", line 28, in <module>
	    from _sqlite3 import *
	ImportError: No module named _sqlite3
This introduces another installation method: using ports. This method will download, compile and install from source code, and the benefit of this approach is you can do some customizations if you want. You can find all ports under `/usr/ports` directory. Now you begin to install `py-bsddb` (follow this method to set up `py-gdbm`, `py-sqlite3` and `py-tkinter`):  
	
	# cd /usr/ports/databases/py-bsddb
	# make install clean

After all are installed, we can use `sqlite` in `python` now:  

	# python
	Python 2.7.11 (default, Jun  5 2016, 01:23:11)
	[GCC 4.2.1 Compatible FreeBSD Clang 3.4.1 (tags/RELEASE_34/dot1-final 208032)] on freebsd10
	Type "help", "copyright", "credits" or "license" for more information.
	>>> import sqlite3

The other method is installing from `DVD`:  
(1) Put `DVD` in the drive;  
(2) Mount `DVD`:  

	mkdir -p /dist
	mount -t cd9660 /dev/cd0 /dist
(3) Install the package (E.g., `xorg`):  

	env REPOS_DIR=/dist/packages/repos pkg install xorg
References:  
[Packages and Ports: Adding Software in FreeBSD](https://www.freebsd.org/doc/en_US.ISO8859-1/articles/linux-users/software.html);  
[Get started with FreeBSD: A brief intro for Linux users](http://www.infoworld.com/article/2858288/unix/intro-to-freebsd-for-linux-users.html);  
[FreeBSD 10 install packages from DVD](https://forums.freebsd.org/threads/44430/#post-300633).
