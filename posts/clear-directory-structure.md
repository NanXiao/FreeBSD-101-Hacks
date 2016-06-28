Clear directory structure
----
`FreeBSD` has a clear separation between base operating system and user-added applications, that means everything which does not belong to the base operating system is under `/usr/local` directory, and the `/usr/local` directory contains a directory structure that mostly mirrors the structure found in the `/` or `/usr` directory.  

For example, the application installed from port tree or `package` command will be located in `/usr/loca/bin` or `/usr/local/sbin`, corresponding to `/bin`, `/sbin`, `/usr/bin` and `/usr/local/sbin`; and `/etc` directory contains configuration files for the base operating system while `/usr/local/etc` for user-added applications.  

References:  
[A Comparative Introduction to FreeBSD for Linux Users](https://www.digitalocean.com/community/tutorials/a-comparative-introduction-to-freebsd-for-linux-users);  
[Directory Structure](https://www.freebsd.org/doc/handbook/dirstructure.html);  
[Ten Things I like About FreeBSD](https://bsdmag.org/download/the_begginers_guide/).
 