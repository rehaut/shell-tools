# BASH

This repo is for testing/playing with/learning about shell scripts.
The excecutables here are tested and made for OSX Unix.

In the directory "Shell_Scripts" you´ll find some tools for your dayly work, I made for myself.
Feel free to copy them, but know that I´m not responsible if you executed without adjustments.


<h3>Tool Documentation</h3>


<b>takeBreak</b>

This little helper reminds me in taking a break every two hours (OS X only - relies on AppleScript).

It is commited to the cronjobs with <code>crontab -e</code> on my System with following entry:

<code>
30 09-20/2 * * 1-5 /usr/local/bin/takeBreak >>/path/to/your/logdirectory/stdout.log 2>>/path/to/your/logdirectory/stderr.log
</code>

The code gets activated each weekday (MO-FR), between 09:30 and 20:30, every second hour and the standart out and error is written to logfiles.
When fired, a voice says "Hey! Make a break!" and then a display dialog pops up and I can choose between ignoring or setting the computer into sleepmode.


<b>shacomp</b>

Do you check the Hashcode provided by the owner when downloading a file?
So I do and I don´t want to compare the two SHA by hand.
Thats the usecase for this script. Put it somewhere in your <code>$PATH</code> and type into the console:

<code>
$ shacomp path/to/mydownload.zip originalSHA algorythm(e.g. 1,256,...)
</code>
