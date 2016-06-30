Trim a file in csh
----
In `bash`, if you want to clear out a file, the easiest command may be "`> file`":  

    # cat test.txt
    Hello world!
    # > test.txt
    # cat test.txt
    #

But in `csh`, "`> file`" will cause "`Invalid null command.`" error:  

    # cat test.txt
    Hello world!
    # > test.txt
    Invalid null command.

The solution is using "`: > file`" command:  

	# cat test.txt
	Hello world!
	# : > test.txt
	# cat test.txt
	#

Or employ "`cat /dev/null > file`".  

Reference:  
[What does a leading colon (:) mean in a script?](http://aplawrence.com/Basics/leading-colon.html).