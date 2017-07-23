Install bash-completion
----
[bash-completion](https://github.com/scop/bash-completion) is a really handy tool which can help you auto-complete many commands, such as `git`. To use it, you need `2` steps:  

(1) Install it:  

	pkg install bash-completion

(2) Add following command in your `~/.profile`:  

	[[ $PS1 && -f /usr/local/share/bash-completion/bash_completion.sh ]] && \
	        source /usr/local/share/bash-completion/bash_completion.sh

	

	
	