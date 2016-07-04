Use "procstat" to get process info
----
On `FreeBSD`, you can use `procstat` command to get detailed info of process. E.g.:  

	# procstat 521
	PID  PPID  PGID   SID  TSID THR LOGIN    WCHAN     EMUL          COMM
	521     1   521   521     0   1 root     select    FreeBSD ELF64 syslogd
The above outputs describe the info of process whose `PID` is `521`: its `PID`, parent `PID`, command name, etc.  

If you want to display all processes' info, use `-a` option:  

    # procstat -a
    PID  PPID  PGID   SID  TSID THR LOGIN    WCHAN     EMUL          COMM
    0     0     0     0     0  10 -        -         -             kernel
    1     0     1     1     0   1 root     wait      FreeBSD ELF64 init
    2     0     0     0     0   2 -        -         -             cam
    3     0     0     0     0   1 -        idle      -             mpt_recovery0
    4     0     0     0     0   1 -        waiting_  -             sctp_iterator
    5     0     0     0     0   2 -        umarcl    -             pagedaemon
    6     0     0     0     0   1 -        psleep    -             vmdaemon
    7     0     0     0     0   1 -        pgzero    -             pagezero

There are many options you can use for `procstat`, i.e., if you are curious about thread info, use `-t` option:  

	# procstat -t 521
    PID    TID COMM             TDNAME           CPU  PRI STATE   WCHAN
    521 100065 syslogd          -                  0  120 sleep   select

For details of every option, please refer the [manual](https://www.freebsd.org/cgi/man.cgi?procstat).

