## GitHub credential challenge

### Truffelhog
[Link](https://github.com/dxa4481/truffleHog)

#### Opening Terminal we see this:
```

                                .OXXXK,                                  
                                 '0l'cOc                                  
                                 ..';'..                                  
                               .';::::::'.                                
                            .':::::::::::::,.                             
                         .'::loc::::::::::::::,.                          
                      .'::::oMMNc::::::::::::::::,.                       
                    .,;;,,,,:dxl:::::::,,,:::;,,,,,,.                     
                    .,'  ..;:::::::::::;,;::::,.                          
                      .';::::::::::::::::::::dOxc,.                       
                   .';:::::::::okd::::::::::cXMWd:::,.                    
                .';:::::::::::cNMMo:::::::::::lc:::::::,.                 
             .'::::::::::::::::col::::::::::::;:::::::::::,.              
                   .;:::,,,:::::::::::::::::;,,,:::::'.                   
                .'::::::;;;:::::::::::dko:::::;::::::::;.                 
             .,::::::::::::::::::::::lWMWc::::::::::::::::;.              
            ..:00:...;::::loc:::::::::coc::::::::::::'.;;.....            
              :NNl.,:::::xMMX:::::::::::::::::::::::::;,,.                
               .,::::::::cxxl::::,,,:::::::::::::::::::::;.               
            .,:::::::c:::::::::::;;;:::::::;;:::::kNXd::::::;.            
         .,::::::::cKMNo::::::::::::::::::;,,;::::xKKo:::::::::;.         
       .'''''',:::::x0Oc:::::::::oOOo:::::::::::::::::::::;'''''''.       
            .,:::::::::::::::::::kWWk::::::::::::::ldl:::::;'.            
         .,::;,,::::::::::::::::::::::::::::::::::lMMMl:::::::;'.         
      .,:::::;,;:::::::::::::::::::::::::::::::::::ldl::::::::::::'.      
   .,::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::'.   
                               ..;;;;;;;;'.                               
                             .';;;;;;;;;;;;'.                             
                          .';;;;;;;;;;;;;;;;;;'.                          
                         ........................                         
                                                                          


Coalbox again, and I've got one more ask.
Sparkle Q. Redberry has fumbled a task.
Git pull and merging, she did all the day;
With all this gitting, some creds got away.

Urging - I scolded, "Don't put creds in git!"
She said, "Don't worry - you're having a fit.
If I did drop them then surely I could,
Upload some new code done up as one should."

Though I would like to believe this here elf,
I'm worried we've put some creds on a shelf.
Any who's curious might find our "oops,"
Please find it fast before some other snoops!

Find Sparkle's password, then run the runtoanswer tool.
elf@db311a1d1c18:~$ 
```
Trying anything in git fails so we need to add the user info, in this case Spaekle Redberry and her email address sredberry@kringlecon.com (dont remember where I got the email, but found it in somewhere, maybe in a log somewhere)

```
*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <(null)>) not allowed
elf@09b56c4fc9da:~/kcconfmgmt$ 
```
So I ran 
git config --global user.email "sredberry@kringlecon.com"
git config --global user.name "Sparkle Redberry"

```
commit 7b93f4be7e7b50b044739e02fa7c75b8fad32366
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Wed Nov 14 04:46:12 2018 -0500

    Add palceholder index, login, profile, signup pages while I CONTINUE TO WAIT FOR UX

commit 20c7def24307589194b7dc05cd852552c36b2b2a
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Tue Nov 13 10:18:08 2018 -0500

    Add Bower setup for front-end

commit 604e434713b4659d7f10b91ab6d20dfa58030c24
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Mon Nov 12 13:04:08 2018 -0500

    Add temp placeholders for login, profile, signup pages -- WAITING ON YOU UX TEAM

commit 31f4eaec30df0f41fc700532d7bc2f6aac94deb8
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Mon Nov 12 00:51:23 2018 -0500

    Add routes for login, logout, signup, isLoggedIn, profile access

commit ac32750bf6a4979bf37108f4438bc9695189ce14
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Sun Nov 11 15:30:15 2018 -0500

    Update index route for passport

commit d84b728c7d9cf7f9bafc5efb9978cd0e3122283d
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Sat Nov 10 19:51:52 2018 -0500

    Add user model for authentication, bcrypt password storage

commit c27135005753f6dde3511a7e70eb27f92f67393f
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Sat Nov 10 08:11:40 2018 -0500

    Add passport config

commit a6449287cf9ed9151d94fb747f6904158c2c4d71
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Fri Nov 9 14:08:04 2018 -0500

    Add passport middleware for user auth

commit 60a2ffea7520ee980a5fc60177ff4d0633f2516b
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Thu Nov 8 21:11:03 2018 -0500

    Per @tcoalbox admonishment, removed username/password from config.js, default settings i
n config.js.def need to be updated before use

commit b2376f4a93ca1889ba7d947c2d14be9a5d138802
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Thu Nov 8 13:25:32 2018 -0500

    Add passport module

commit d99d465d5b9711d51d7b455584af2b417688c267
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Wed Nov 7 16:57:41 2018 -0500

    Correct typos, runs now! Change port for MongoDB connection

commit 68405b8a6dcaed07c20927cee1fb6d6c59b62cc3
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Tue Nov 6 17:26:39 2018 -0500

    Add initial server config

commit 69cc84998e57f4fc6aca17f2a5cb9caff53f3fd3
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Mon Nov 5 20:17:51 2018 -0500

    Added speakers.js data model

commit c3ee078d17a5309fbe18426c048a9a12b495f39f
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Mon Nov 5 01:27:11 2018 -0500

    File reorganization under server/

commit b4d783d7a7f8ba9bb3aee72aeba43ba9bb99c8b0
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Sun Nov 4 04:30:39 2018 -0500

    Module cleanup

commit 9c06c0441c95323e8270f6a219439daba59017f5
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Fri Nov 2 11:05:49 2018 -0400

    Added Express EJS setup (go away, Jade)


commit 1f9bbf6d2cee75a9dd6bb483edf940f9bb71035f
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Thu Nov 1 11:30:50 2018 -0400
```
 
 Interesting line here
 ```
 commit 60a2ffea7520ee980a5fc60177ff4d0633f2516b
Author: Sparkle Redberry <sredberry@kringlecon.com>
Date:   Thu Nov 8 21:11:03 2018 -0500

    Per @tcoalbox admonishment, removed username/password from config.js, default settings i
n config.js.def need to be updated before use
```
So lets revert back to that one

``` git revert 60a2ffea7520ee980a5fc60177ff4d0633f2516b ```

now check git status and we see that there are two files that need commited, 

```
elf@09b56c4fc9da:~/kcconfmgmt$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   server/config/config.js
        deleted:    server/config/config.js.def
```
Quick more of that config.js file

```
elf@0594e6c4bbfd:~/kcconfmgmt$ more server/config/config.js 
// Database URL
module.exports = {
    'url' : 'mongodb://sredberry:twinkletwinkletwinkle@127.0.0.1:27017/node-api'
};
```

```
elf@0594e6c4bbfd:~$ ./runtoanswer 
Loading, please wait......



Enter Sparkle Redberry's password: twinkletwinkletwinkle


This ain't "I told you so" time, but it's true:
I shake my head at the goofs we go through.
Everyone knows that the gits aren't the place;
Store your credentials in some safer space.

Congratulations!

elf@0594e6c4bbfd:~$ 
```