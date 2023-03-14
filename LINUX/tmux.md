# TMUX
## A terminal multiplexor

### This tool is extremely helpful for terminal based work because it enables:

* Easy window splits
* Caching of terminal sessions. So one can exit and enter different terminal setups for different jobs.
* Keeping remote connections alive.

### Commands

Attach to a previous, most recent session.

	tmux attach

Attach to a target session if multiple session are open.

	tmux attach -t 'target session name'

Create a new named session

	tmux new -s name

Exit a session to enter another

	tmux detach

List current sessions

	tmux ls

Kill a session, meaning remove from cache

	ctrl+b
	:kill-session 
