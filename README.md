# shell-tools

This repo is for testing/playing with shell scripts.


<h3>Tool Simple</h3>


<b>alertMe</b>

Helper tool, alarmclock with Window prompt.

- tools_simple/alertMe-gnome (depends on zenity)
- tools_simple/alertMe_MAC (old untested version)


<b>shacomp</b>

Wrapper for shaXsum. I don´t want to compare the two SHA keys by hand.
Thats the usecase for this script. Put it somewhere in your <code>$PATH</code> and type into the console:

<code>
$ shacomp path/to/mydownload.zip originalSHA algorythm(e.g. 1,256,...)
</code>


<b>subPing</b>

A fast ping sript for subnet responce scanning. Scans a whole subnet (eg. xxx.xxx.xxx ) in a second.

<code>
$ subPing 192.168.178
</code>


<b>takeBreak</b>

Helper tool, reminding user in taking a break every X hours (old OS X only - relies on AppleScript).

It is commited to the cronjobs with <code>crontab -e</code> on my System with following entry:

<code>
30 09-20/2 * * 1-5 /usr/local/bin/takeBreak >>/path/to/your/logdirectory/stdout.log 2>>/path/to/your/logdirectory/stderr.log
</code>

The code gets activated each weekday (MO-FR), between 09:30 and 20:30, every second hour and the standart out and error is written to logfiles.
When fired, a voice says "Hey! Make a break!" and then a display dialog pops up and I can choose between ignoring or setting the computer into sleepmode.

<h3>bash docs</h3>