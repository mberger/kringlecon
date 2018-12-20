### This challenge is to uploac the elf's report.txt to the samba share at //localhost/report-upload

[Video](https://www.youtube.com/watch?v=W6_JaApK0xM)

Here's the firt screen... lets go
```
kkkkkkkkkkkkkOKXXXXXXXkxddo;,,,,,,,,,,,,,,,,,,,,,,,,cddxkXXXXXXXkc,,,,,,,,,,,,,
kkkkkkkkkkkkkkkk00KXXXXXkl,,,,,,,,,,,,oKOc,,,,,,,,,,,:xXXXX0kdc;,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkKXXXKx:,,,,,,,,;dKXXXX0l,,,,,,,,cxXXXXk,,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkk0XXXXX0xoc;,;dKXXXXXXXX0l;:cokKXXXXKo,,,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkkk0KXXXXXXXXXXXXXXXXXXXXXXXXXXXXKkl,,,,,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkkkkkkOO00XXXXXXXXXXXXXXXXXXXxc:;,,,,,,,,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkkkkkkkO0XNWWNNXXXXXXXXXXNNWWN0o,,,,,,,,,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkkkkkO0XWMMMMMMNXXXXXXXNWMMMMMMNKo,,,,,,,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkkkk0XXWMMMMMMMMNXXXXXXWMMMMMMMMNX0c,,,,,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkkOKXXNMMMMMMMMMWXXXXXNMMMMMMMMMWXXXx,,,,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkOXXXXNMMMMMMMMMMXXXXXNMMMMMMMMMWXXXXk,,,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkKXXXXNMMMMXl:dWWXXXXXNMXl:dWMMMWXXXXXd,,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkk0XXXXXXNMMMo   KNXXXXXXNo   KMMMNXXXXXX;,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkKXXXXXXXNWMM0kKNXXXXXXXXN0kXMMWNXXXXXXXo,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkXXXXXXXXXXNNNNXXXX0xxKXXXXNNNNXXXXXXXXXx,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkXXXXXXXXXXXXXXXXX'    oXXXXXXXXXXXXXXXXd,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkk0XXXXXXXXXXXXXXXX.    cXXXXXXXXXXXXXXXXc,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkOXXXXXXXXXXXXXXXXXdllkXXXXXXXXXXXXXXXXk,,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkk0XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXkl,,,,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkk0XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXOkkkl;,,,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkkkOXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXKkkkkkkko;,,,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkkkkk0XXXXXXXXXXXXXXXXXXXXXXXXXXXKOkkkkkkkkkkd:,,,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkkkkkkkOKXXXXXXXXXXXXXXXXXXXXXXKOkkkkkkkkkkkkkkd:,,,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkkkkkkkkkkO0KXXXXXXXXXXXXXXK0Okkkkkkkkkkkkkkkkkkkd:,,,,,,,,
kkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkOO000000OOkkkkkkkkkkkkkkkkkkkkkkkkkkxc,,,,,,
kkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkxl,,,,
kkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkxl,,
kkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkx;

Thank you Madam or Sir for the help that you bring!
I was wondering how I might rescue my day.
Finished mucking out stalls of those pulling the sleigh,
My report is now due or my KRINGLE's in a sling!

There's a samba share here on this terminal screen.
What I normally do is to upload the file,
With our network credentials (we've shared for a while).
When I try to remember, my memory's clean!

Be it last night's nog bender or just lack of rest,
For the life of me I can't send in my report.
Could there be buried hints or some way to contort,
Gaining access - oh please now do give it your best!

-Wunorse Openslae


Complete this challenge by uploading the elf's report.txt
file to the samba share at //localhost/report-upload/
elf@38fa2dd7ebbc:~$
```
The report is a simple text file
```
Stall mucking report

Dasher - routine
Dancer - routine
Prancer - confiscated second salt lick
Vixen - minor repair/adjustment to water system
Comet - routine
Cupid - routine
Donner - routine
Blitzen - refilled headache medicine
Thrasher - routine
Thunder - requested hay! oats! hay! oats!
Blaster - stall... took extra mucking
Blunder - caught with excessive carrot contraband again
Blogger - discussed social media policies again
Bragger - what appeared to be a prosthetic red nose
Wed Dec 19 16:11:48 UTC 2018
```

A ps gets us this:
```
PID TTY      STAT   TIME COMMAND
    1 pts/0    Ss     0:00 /bin/bash /sbin/init
   10 pts/0    S      0:00 sudo -u manager /home/manager/samba-wrapper.sh --verbosity=none --no-check-certificate --extraneous-command-argument --do-not-run-as-tyler --accept-sage-advice -a 42 -d~ --ignore-sw-holiday-special --suppress --suppress //localhost/report-upload/ directreindeerflatterystable -U report-upload
   16 pts/0    S      0:00  \_ /bin/bash /home/manager/samba-wrapper.sh --verbosity=none --no-check-certificate --extraneous-command-argument --do-not-run-as-tyler --accept-sage-advice -a 42 -d~ --ignore-sw-holiday-special --suppress --suppress //localhost/report-upload/ directreindeerflatterystable -U report-upload
   30 pts/0    S      0:00      \_ sleep 60
   11 pts/0    S      0:00 sudo -E -u manager /usr/bin/python /home/manager/report-check.py
   17 pts/0    S      0:00  \_ /usr/bin/python /home/manager/report-check.py
   15 pts/0    S      0:00 sudo -u elf /bin/bash
   18 pts/0    S      0:00  \_ /bin/bash
   34 pts/0    R+     0:00      \_ ps afx
   35 pts/0    S+     0:00      \_ less
   23 ?        Ss     0:00 /usr/sbin/smbd
   24 ?        S      0:00  \_ /usr/sbin/smbd
   25 ?        S      0:00  \_ /usr/sbin/smbd
   27 ?        S      0:00  \_ /usr/sbin/smbd
   ```


Typical samba put command 
``` smbclient //server/share -c 'cd c:/remote/path ; put local-file' ```

