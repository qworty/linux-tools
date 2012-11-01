linux-tools
===========

some of my linux tools. they are mostly perl scripts and you needn't judge me for coding style,
i am already ashamed.

you'll find that some of them have arbitrary values in them that are useful to me,
so that's not very nice for a github repo. but i would advice you check each one manually
before actually using them ;)

clear-desktop
-------------
i cron this each night, it moves all files from ~/desktop that are older than 28 days to
/tmp/, so that my desktop stays clean. it checks both ctime and mtime so that files that
have a mod time in the past (they come from a zip for ex.) won't get deleted right away.

pacman-meld
-----------
i run this after i upgrade my arch workstation or my centos server.
it works for the local machine by default, but if you root-mount a remote server
you can run `pacman-meld /mnt/server-1` and it will work.

what it does is scan the filesystem for *.(pac|rpm)(save|new) files, and start the excellent
'meld' tool on the original file. it's an easy way to merge configuration file changes
after a full system update.

sysresccd-makeusb
-----------------
you can use this if you have a SystemRescueCD USB stick that you have personalized items on,
and you want to upgrade it from a new ISO. in this script itsself is an array with paths to
your personalized files/dirs. you run this script and give it the path to the new ISO,
it will copy your personalized files to a safe place, start the USB ISO installer, then
copies your files back to the newly written stick.

playtmpflash
------------
i bind this to Win+F11, and when i watch a flash video on a webpage, i pause it and press
the key combo. it then fetches the flash file from the flashplugin process, copies it back
to its /tmp/ location (flashplugin unlinks it at start) and starts mplayer on it. that way
you can watch any flash video in fullscreen and you don't need to watch it in your browser.

