# shell-tools

This repo is for testing/playing with shell scripts.


<h3>Simple Bash Tools</h3>


<h4>alertMe</h4>

Helper tool, alarmclock with Window prompt.

- [alertMe for Linux/Gnome](tools_simple/alertMe_gnome) (**depends on zenity**)
- [alertMe for Apple/OSX](rehaut/shell-tools/tools_simple/alertMe_MAC) (*old untested version*)


<h4>shacomp</h4>

Wrapper for shaXsum. I don´t want to compare the two SHA keys by hand.
Thats the usecase for this script. Put it somewhere in your <code>$PATH</code> and type into the console:

	<code>
	$ shacomp path/to/mydownload.zip originalSHA algorythm(e.g. 1,256,...)
	</code>


<h4>subPing</h4>

A fast ping sript for subnet responce scanning. Scans a whole subnet (eg. xxx.xxx.xxx ) in a second.

	<code>
	# scans 192.168.178.1 to 192.168.178.255
	$ subPing 192.168.178
	</code>


<h4>takeBreak</h4>

Helper tool alarmclock, reminding user in taking a break every X hours (old OS X only - relies on AppleScript).

It is commited to the cronjobs with <code>crontab -e</code> on my System with following entry:

<code>
30 09-20/2 * * 1-5 /usr/local/bin/takeBreak >>/path/to/your/logdirectory/stdout.log 2>>/path/to/your/logdirectory/stderr.log
</code>

The code gets activated each weekday (MO-FR), between 09:30 and 20:30, every second hour and the standart out and error is written to logfiles.
When fired, a voice says "Hey! Make a break!" and then a display dialog pops up and I can choose between ignoring or setting the computer into sleepmode.