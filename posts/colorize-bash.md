Colorize bash
----
(1) In your `$HOME` directory, create `..dir_colors` file:  

	# Below, there should be one TERM entry for each termtype that is colorizable
	TERM ansi
	TERM color-xterm
	TERM con132x25
	TERM con132x30
	TERM con132x43
	TERM con132x60
	TERM con80x25
	TERM con80x28
	TERM con80x30
	TERM con80x43
	TERM con80x50
	TERM con80x60
	TERM cons25
	TERM console
	TERM cygwin
	TERM dtterm
	TERM Eterm
	TERM gnome
	TERM konsole
	TERM kterm
	TERM linux
	TERM linux-c
	TERM mach-color
	TERM putty
	TERM rxvt
	TERM rxvt-cygwin
	TERM rxvt-cygwin-native
	TERM rxvt-unicode
	TERM screen
	TERM screen-bce
	TERM screen-w
	TERM screen.linux
	TERM vt100
	TERM xterm
	TERM xterm-256color
	TERM xterm-color
	TERM xterm-debian
	
	# Below are the color init strings for the basic file types. A color init
	# string consists of one or more of the following numeric codes:
	# Attribute codes:
	# 00=none 01=bold 04=underscore 05=blink 07=reverse 08=concealed
	# Text color codes:
	# 30=black 31=red 32=green 33=yellow 34=blue 35=magenta 36=cyan 37=white
	# Background color codes:
	# 40=black 41=red 42=green 43=yellow 44=blue 45=magenta 46=cyan 47=white
	NORMAL 00           # global default, although everything should be something.
	FILE 00             # normal file
	DIR 01;34           # directory
	LINK 01;36          # symbolic link.  (If you set this to 'target' instead of a
	                    # numerical value, the color will match the file pointed to)
	FIFO 40;33          # pipe
	SOCK 01;35          # socket
	DOOR 01;35          # door
	BLK 40;33;01        # block device driver
	CHR 40;33;01        # character device driver
	ORPHAN 01;05;37;41  # orphaned syminks
	MISSING 01;05;37;41 # ... and the files they point to
	
	# This is for files with execute permission:
	EXEC 01;32
	
	# List any file extensions like '.gz' or '.tar' that you would like ls
	# to colorize below. Put the extension, a space, and the color init string.
	# (and any comments you want to add after a '#')
	
	.cmd 01;32 # executables (bright green)
	.exe 01;32
	.com 01;32
	.btm 01;32
	.bat 01;32
	.sh  01;32
	.csh 01;32
	
	.tar 01;31 # archives / compressed (bright red)
	.tgz 01;31
	.arj 01;31
	.taz 01;31
	.lzh 01;31
	.zip 01;31
	.z   01;31
	.Z   01;31
	.gz  01;31
	.bz2 01;31
	.bz  01;31
	.tbz2 01;31
	.tz  01;31
	.deb 01;31
	.rpm 01;31
	.rar 01;31        # app-arch/rar
	.ace 01;31        # app-arch/unace
	.zoo 01;31        # app-arch/zoo
	.cpio 01;31       # app-arch/cpio
	.7z  01;31        # app-arch/p7zip
	.rz  01;31        # app-arch/rzip
	
	.jpg 01;35 # image formats
	.jpeg 01;35
	.gif 01;35
	.bmp 01;35
	.ppm 01;35
	.tga 01;35
	.xbm 01;35
	.xpm 01;35
	.tif 01;35
	.tiff 01;35
	.png 01;35
	.mng 01;35
	.xcf 01;35
	.pcx 01;35
	.mpg 01;35
	.mpeg 01;35
	.m2v 01;35  # MPEG-2 Video only
	.avi 01;35
	.mkv 01;35  # Matroska (http://matroska.org/)
	.ogm 01;35  # Ogg Media File
	.mp4 01;35  # "Offical" container for MPEG-4
	.m4v 01;35  # MPEG-4 Video only
	.mp4v 01;35 # MPEG-4 Video only
	.mov 01;35  # Quicktime (http://developer.apple.com/qa/qtw/qtw99.html)
	.qt 01;35   # Quicktime (http://developer.apple.com/qa/qtw/qtw99.html)
	.wmv 01;35  # Windows Media Video
	.asf 01;35  # Advanced Systems Format (contains Windows Media Video)
	.rm 01;35   # Real Media
	.rmvb 01;35 # Real Media Variable Bitrate
	.flc 01;35  # AutoDesk Animator
	.fli 01;35  # AutoDesk Animator
	.gl 01;35
	.dl 01;35
	
	.pdf 00;32 # Document files
	.ps 00;32
	.txt 00;32
	.patch 00;32
	.diff 00;32
	.log 00;32
	.tex 00;32
	.doc 00;32
	
	.mp3 00;36 # Audio files
	.wav 00;36
	.mid 00;36
	.midi 00;36
	.au 00;36
	.ogg 00;36
	.flac 00;36
	.aac 00;36
(2) Add following statements in `/etc/profile`:  

	eval $(dircolors -b ~/.dir_colors)
	
	if [[ ${EUID} == 0 ]] ; then
	    PS1='\[\033[01;31m\]\h\[\033[01;34m\] \W \$\[\033[00m\] '
	else
	    PS1='\[\033[01;32m\]\u@\h\[\033[01;34m\] \w \$\[\033[00m\] '
	fi
	
	CLICOLOR="YES";    export CLICOLOR
	LSCOLORS="ExGxFxdxCxDxDxhbadExEx";    export LSCOLORS

Reference:  
[Colorize your bash like linux.](https://forums.freebsd.org/threads/45006/).
	

	
	