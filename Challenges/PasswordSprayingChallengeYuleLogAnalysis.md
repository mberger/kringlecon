

```
                                                                                
                             .;:cccckkxdc;.                                     
                         .o0xc;,,,,,XMMMMMkc:,.                                 
                       lXMMMX;,,,,,,XMMMMK,,coddcclOkxoc,.                      
                     lk:oNMMMX;,,,,,XMMWN00o:,,,,,:MMMMMMoc;'                   
                   .0l,,,,dNMMX;,,,,XNNWMMMk,,,,,,:MMMMMx,,,,:;.                
                  .K;,,,,,,,xWMX;,,;Kx:kWMMMk,,,,,:MMMM0,,,,,,,:k'              
                 .XklooooddolckWN:l0:,,,;kWMMO,,,,:MMMN;,,,,,cOWMMd             
               ;oooc;,,,cMMMMMMxkO0,,,,,,,:OMM0,,,:MMWc,,,,lKMMMMWKo            
            ;OMMWl,,,,,,cMMMMMO,,,:cc,,,,,,,:0M0,,:MMd,,,oXMMWKxc,,,c           
          cOdXMMMWl,,,,,cMMMMX,,,,,,,:xxo:,,,,cK0,:MO,;xNWKxc,,,,,,,:.          
        .0l,,,oNMMWl,,,,cMMMW:,,,,,,dXMWNMWXOdc;lxcX:xOxc,,,,,,,,,,,,:          
       ,0;,,,,,,dNMWo,,,cMMMl,,,,;xNMMMMW0kkkkkkddxdddxxxxxxxxxxxxxxxo          
      .Wl,,,,,,,,,dWMo,,cMMx,,,:OWMMW0xc,:c,,:dOkcK:kc:ok0NMMMMMMMMMMd          
      KMMWXOdl;,,,,;xWd,cM0,,l0MW0dc,,,,,,lkWWk:,OW,:XO:,,,;ldOXWMMMM'          
     'MMMMMMMMMN0ko:,;kdcN;o00dc,,,,,,,,,,,0x;,,oMW,,;XWk;,,,,,,,:okk           
     cNKKKKKKKKKKKKKKkoodxxdccccccccccccccco,,,:WMW,,,;XMWk;,,,,,,,l            
     :x,,,,,,,,,,,,,cdkoOldldOKWMMMMMMMMMMMx,,,XMMW,,,,;XMMWx,,,,;c             
     .K,,,,,,,,,cd0WKl,xN,oXo,,,:ok0NMMMMMMc,,OMMMW,,,,,;KMMMNd;l'              
      dl,,,,cx0WMM0c,,lMN,,oMXl,,,,,,;ldOX0',dMMMMW,,,,,,;KMMMK;                
       OoxKWMMMWk:,,,;NMN,,,lWMKc,,,,,,,,ldclWMMMMW,,,,,,:oOl.                  
        OMMMMNx;,,,,,KMMN,,,,lWMM0c,,,,,l. .,cdkO00ccc:;,.                      
         cWXo,,,,,,,kMMMN,,,,,cWMMM0:,c:                                        
          .Kc,,,,,,:MMMMN,,,,,,dMMMMWk'                                         

I am Pepper Minstix, and I'm looking for your help.
Bad guys have us tangled up in pepperminty kelp!
"Password spraying" is to blame for this our grinchly fate.
Should we blame our password policies which users hate?

Here you'll find a web log filled with failure and success.
One successful login there requires your redress.
Can you help us figure out which user was attacked?
Tell us who fell victim, and please handle this with tact...

  Submit the compromised webmail username to 
  runtoanswer to complete this challenge.
elf@dcb7c545f9d3:~$ 
```


### Contents of the python-evtx.py script
```
#!/usr/bin/env python
#    This file is part of python-evtx.
#
#   Copyright 2012, 2013 Willi Ballenthin <william.ballenthin@mandiant.com>
#                    while at Mandiant <http://www.mandiant.com>
#
#   Licensed under the Apache License, Version 2.0 (the "License");
#   you may not use this file except in compliance with the License.
#   You may obtain a copy of the License at
#
#       http://www.apache.org/licenses/LICENSE-2.0
#
#   Unless required by applicable law or agreed to in writing, software
#   distributed under the License is distributed on an "AS IS" BASIS,
#   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#   See the License for the specific language governing permissions and
#   limitations under the License.
#
#   Version v0.1.1
import Evtx.Evtx as evtx
import Evtx.Views as e_views


def main():
    import argparse

    parser = argparse.ArgumentParser(
        description="Dump a binary EVTX file into XML.")
    parser.add_argument("evtx", type=str,
                        help="Path to the Windows EVTX event log file")
    args = parser.parse_args()

    with evtx.Evtx(args.evtx) as log:
        print(e_views.XML_HEADER)
        print("<Events>")
        for record in log.records():
            print(record.xml())
        print("</Events>")


if __name__ == "__main__":
```


### Output of the file search that needs to bee checked.  I'm starting with the users who I know work at the North Pole.

<Data Name="TargetUserName">amy.smith</Data>
<Data Name="TargetUserName">DWM-1</Data>
<Data Name="TargetUserName">LOCAL SERVICE</Data>
<Data Name="TargetUserName">IUSR</Data>
<EventData><Data Name="TargetUserName">WIN-KCON-EXCH16$@EM.KRINGLECON.COM</Data>
<Data Name="TargetUserName">HealthMailboxbab78a6</Data>
WIN-KCON-EXCH16$@EM.KRINGLECON.COM
<Data Name="TargetUserName">HealthMailboxbe58608d4925422d8e4ea458cfedc612@EM.KRINGLECON.COM</Data>
<EventData><Data Name="TargetUserName">sparkle.redberry</Data>
<EventData><Data Name="TargetUserName">sparkle.redberry@EM.KRINGLECON.COM</Data>
<Data Name="TargetUserName">HealthMailboxbe58608</Data>
<EventData><Data Name="TargetUserName">bushy.evergreen</Data>
<EventData><Data Name="TargetUserName">bushy.evergreen@EM.KRINGLECON.COM</Data>
<Data Name="TargetUserName">test.user</Data>
<EventData><Data Name="TargetUserName">shinny.upatree</Data>
<EventData><Data Name="TargetUserName">shinny.upatree@EM.KRINGLECON.COM</Data>
<Data Name="TargetUserName">aaron.smith</Data>
<Data Name="TargetUserName">abhishek.kumar</Data>
<Data Name="TargetUserName">adam.smith</Data>
<Data Name="TargetUserName">ahmed.ali</Data>
<Data Name="TargetUserName">ahmed.hassan</Data>
<Data Name="TargetUserName">ahmed.mohamed</Data>
<Data Name="TargetUserName">ajay.kumar</Data>
<Data Name="TargetUserName">alex.smith</Data>
<Data Name="TargetUserName">ali.khan</Data>
<Data Name="TargetUserName">ali.raza</Data>
<Data Name="TargetUserName">amanda.smith</Data>
<Data Name="TargetUserName">amit.kumar</Data>
<Data Name="TargetUserName">amit.sharma</Data>
<Data Name="TargetUserName">HealthMailboxbe58608</Data>
<Data Name="TargetUserName">amit.singh</Data>
<Data Name="TargetUserName">amy.smith</Data>
<Data Name="TargetUserName">andrew.smith</Data>
<Data Name="TargetUserName">anil.kumar</Data>
<Data Name="TargetUserName">arun.kumar</Data>
<Data Name="TargetUserName">ashley.brown</Data>
<Data Name="TargetUserName">ashley.johnson</Data>
<Data Name="TargetUserName">ashley.jones</Data>
<Data Name="TargetUserName">ashley.smith</Data>
<Data Name="TargetUserName">ashley.williams</Data>
<Data Name="TargetUserName">ashok.kumar</Data>
<Data Name="TargetUserName">ben.smith</Data>
<Data Name="TargetUserName">bob.smith</Data>
<Data Name="TargetUserName">brandon.smith</Data>
<Data Name="TargetUserName">brian.johnson</Data>
<Data Name="TargetUserName">brian.jones</Data>
<Data Name="TargetUserName">brian.smith</Data>
<Data Name="TargetUserName">bushy.evergreen</Data>
<Data Name="TargetUserName">HealthMailboxbab78a6</Data>
<Data Name="TargetUserName">chris.anderson</Data>
<Data Name="TargetUserName">chris.brown</Data>
<Data Name="TargetUserName">chris.davis</Data>
<Data Name="TargetUserName">chris.johnson</Data>
<Data Name="TargetUserName">chris.jones</Data>
<Data Name="TargetUserName">chris.lee</Data>
<Data Name="TargetUserName">chris.martin</Data>
<Data Name="TargetUserName">chris.miller</Data>
<Data Name="TargetUserName">chris.smith</Data>
<Data Name="TargetUserName">chris.taylor</Data>
<Data Name="TargetUserName">chris.williams</Data>
<Data Name="TargetUserName">chris.wilson</Data>
<Data Name="TargetUserName">christopher.smith</Data>
<Data Name="TargetUserName">dan.smith</Data>
<Data Name="TargetUserName">daniel.smith</Data>
<Data Name="TargetUserName">dave.smith</Data>
<Data Name="TargetUserName">david.anderson</Data>
<Data Name="TargetUserName">HealthMailboxbe58608</Data>
<Data Name="TargetUserName">david.brown</Data>
<Data Name="TargetUserName">david.johnson</Data>
<Data Name="TargetUserName">david.jones</Data>
<Data Name="TargetUserName">david.lee</Data>
<Data Name="TargetUserName">david.miller</Data>
<Data Name="TargetUserName">david.smith</Data>
<Data Name="TargetUserName">david.williams</Data>
<Data Name="TargetUserName">david.wilson</Data>
<Data Name="TargetUserName">deepak.kumar</Data>
<Data Name="TargetUserName">deepak.sharma</Data>
<Data Name="TargetUserName">dinesh.kumar</Data>
<Data Name="TargetUserName">eric.johnson</Data>
<Data Name="TargetUserName">eric.smith</Data>
<Data Name="TargetUserName">gaurav.sharma</Data>
<Data Name="TargetUserName">greg.smith</Data>
<Data Name="TargetUserName">gurpreet.singh</Data>
<Data Name="TargetUserName">harpreet.singh</Data>
<Data Name="TargetUserName">heather.smith</Data>
<Data Name="TargetUserName">holly.evergreen</Data>
<Data Name="TargetUserName">imran.khan</Data>
<Data Name="TargetUserName">james.brown</Data>
<Data Name="TargetUserName">james.johnson</Data>
<Data Name="TargetUserName">james.jones</Data>
<Data Name="TargetUserName">james.lee</Data>
<Data Name="TargetUserName">james.smith</Data>
<Data Name="TargetUserName">james.taylor</Data>
<Data Name="TargetUserName">james.williams</Data>
<Data Name="TargetUserName">jamie.smith</Data>
<Data Name="TargetUserName">jane.smith</Data>
<Data Name="TargetUserName">jason.brown</Data>
<Data Name="TargetUserName">jason.jones</Data>
<Data Name="TargetUserName">jason.lee</Data>
<Data Name="TargetUserName">jason.miller</Data>
<Data Name="TargetUserName">HealthMailboxbab78a6</Data>
<Data Name="TargetUserName">jason.smith</Data>
<Data Name="TargetUserName">jason.williams</Data>
<Data Name="TargetUserName">jeff.smith</Data>
<Data Name="TargetUserName">jennifer.johnson</Data>
<Data Name="TargetUserName">jennifer.jones</Data>
<Data Name="TargetUserName">jennifer.smith</Data>
<Data Name="TargetUserName">jessica.brown</Data>
<Data Name="TargetUserName">jessica.johnson</Data>
<Data Name="TargetUserName">jessica.jones</Data>
<Data Name="TargetUserName">jessica.smith</Data>
<Data Name="TargetUserName">HealthMailboxbe58608</Data>
<Data Name="TargetUserName">jessica.williams</Data>
<Data Name="TargetUserName">joe.smith</Data>
<Data Name="TargetUserName">john.anderson</Data>
<Data Name="TargetUserName">john.brown</Data>
<Data Name="TargetUserName">john.davis</Data>
<Data Name="TargetUserName">john.johnson</Data>
<Data Name="TargetUserName">HealthMailboxbe58608</Data>
<Data Name="TargetUserName">john.jones</Data>
<Data Name="TargetUserName">john.lee</Data>
<Data Name="TargetUserName">john.miller</Data>
<Data Name="TargetUserName">john.smith</Data>
<Data Name="TargetUserName">john.taylor</Data>
<Data Name="TargetUserName">john.williams</Data>
<Data Name="TargetUserName">john.wilson</Data>
<Data Name="TargetUserName">jose.garcia</Data>
<Data Name="TargetUserName">jose.rodriguez</Data>
<Data Name="TargetUserName">josh.smith</Data>
<Data Name="TargetUserName">justin.smith</Data>
<Data Name="TargetUserName">karen.smith</Data>
<Data Name="TargetUserName">katie.smith</Data>
<Data Name="TargetUserName">kelly.smith</Data>
<Data Name="TargetUserName">kevin.brown</Data>
<Data Name="TargetUserName">kevin.johnson</Data>
<Data Name="TargetUserName">kevin.jones</Data>
<Data Name="TargetUserName">kevin.smith</Data>
<Data Name="TargetUserName">HealthMailboxbe58608</Data>
<Data Name="TargetUserName">kim.smith</Data>
<Data Name="TargetUserName">kiran.kumar</Data>
<Data Name="TargetUserName">kyle.smith</Data>
<Data Name="TargetUserName">laura.smith</Data>
<Data Name="TargetUserName">lee</Data>
<Data Name="TargetUserName">linda.smith</Data>
<Data Name="TargetUserName">lisa.smith</Data>
<Data Name="TargetUserName">manish.kumar</Data>
<Data Name="TargetUserName">manoj.kumar</Data>
<Data Name="TargetUserName">mark.brown</Data>
<Data Name="TargetUserName">mark.johnson</Data>
<Data Name="TargetUserName">mark.jones</Data>
<Data Name="TargetUserName">mark.smith</Data>
<Data Name="TargetUserName">mark.williams</Data>
<Data Name="TargetUserName">mary.smith</Data>
<Data Name="TargetUserName">matt.johnson</Data>
<Data Name="TargetUserName">matt.smith</Data>
<Data Name="TargetUserName">matthew.smith</Data>
<Data Name="TargetUserName">melissa.smith</Data>
<Data Name="TargetUserName">michael.brown</Data>
<Data Name="TargetUserName">michael.davis</Data>
<Data Name="TargetUserName">michael.johnson</Data>
<Data Name="TargetUserName">michael.jones</Data>
<Data Name="TargetUserName">michael.lee</Data>
<Data Name="TargetUserName">michael.miller</Data>
<Data Name="TargetUserName">michael.smith</Data>
<Data Name="TargetUserName">michael.taylor</Data>
<Data Name="TargetUserName">michael.williams</Data>
<Data Name="TargetUserName">michael.wilson</Data>
<Data Name="TargetUserName">michelle.smith</Data>
<Data Name="TargetUserName">mike.brown</Data>
<Data Name="TargetUserName">mike.johnson</Data>
<Data Name="TargetUserName">mike.jones</Data>
<Data Name="TargetUserName">HealthMailboxbe58608</Data>
<Data Name="TargetUserName">mike.miller</Data>
<Data Name="TargetUserName">mike.smith</Data>
<Data Name="TargetUserName">mike.williams</Data>
<EventData><Data Name="TargetUserName">minty.candycane</Data>
<EventData><Data Name="TargetUserName">minty.candycane@EM.KRINGLECON.COM</Data>
<Data Name="TargetUserName">minty.candycane</Data>
<Data Name="TargetUserName">mohamed.ahmed</Data>
<Data Name="TargetUserName">mohamed.ali</Data>



```
elf@6307ca69e75c:~$ ./runtoanswer 
Loading, please wait..minty....



Whose account was successfully accessed by the attacker's password spray? minty.candycane


MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMNMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMkl0MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMXO0NMxl0MXOONMMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMxlllooldollo0MMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMW0OKWMMNKkollldOKWMMNKOKMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMXollox0NMMMxlOMMMXOdllldWMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMWXOdlllokKxlk0xollox0NMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMNkkXMMMMMMMMMMMWKkollllllldkKWMMMMMMMMMMM0kOWMMMMMMMMMMMM
MMMMMMWKXMMMkllxMMMMMMMMMMMMMMMXOold0NMMMMMMMMMMMMMMMollKMMWKKWMMMMMM
MMMMMMdllKMMkllxMMMMMMMMMMMMN0KNMxl0MN00WMMMMMMMMMMMMollKMMOllkMMMMMM
Mkox0XollKMMkllxMMMMMMMMMMMMxllldoldolllOMMMMMMMMMMMMollKMMkllxXOdl0M
MMN0dllll0MMkllxMMMMMMMMMMMMMN0xolllokKWMMMMMMMMMMMMMollKMMkllllx0NMM
MW0xolllolxOxllxMMNxdOMMMMMWMMMMWxlOMMMMWWMMMMWkdkWMMollOOdlolllokKMM
M0lldkKWMNklllldNMKlloMMMNolok0NMxl0MX0xolxMMMXlllNMXolllo0NMNKkoloXM
MMWWMMWXOdlllokdldxlloWMMXllllllooloollllllWMMXlllxolxxolllx0NMMMNWMM
MMMN0kolllx0NMMW0ollll0NMKlloN0kolllokKKlllWMXklllldKMMWXOdlllokKWMMM
MMOllldOKWMMMMkollox0OdldxlloMMMMxlOMMMNlllxoox0Oxlllo0MMMMWKkolllKMM
MMW0KNMMMMMMMMKkOXWMMMW0olllo0NMMxl0MWXklllldXMMMMWKkkXMMMMMMMMX0KWMM
MMMMMMMMMMMMMMMMMMMW0xollox0Odlokdlxxoox00xlllokKWMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMWollllOWMMMMNklllloOWMMMMNxllllxMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMN0xlllokK0xookdlxxookK0xollokKWMMMMMMMMMMMMMMMMMMM
MMWKKWMMMMMMMMKk0XMMMMW0ollloOXMMxl0MWKklllldKWMMMWXOOXMMMMMMMMNKKMMM
MMkllldOXWMMMMklllok00xoodlloMMMMxlOMMMNlllxook00xollo0MMMMWKkdlllKMM
MMMN0xollox0NMMW0ollllONMKlloNKkollldOKKlllWMXklllldKWMMX0xlllok0NMMM
MMWWMMWKkollldkxlodlloWMMXllllllooloollllllWMMXlllxooxkollldOXMMMWMMM
M0lldOXWMNklllldNMKlloMMMNolox0XMxl0WXOxlldMMMXlllNMXolllo0WMWKkdloXM
MW0xlllodldOxllxMMNxdOMMMMMNMMMMMxlOMMMMWNMMMMWxdxWMMollkkoldlllokKWM
MMN0xllll0MMkllxMMMMMMMMMMMMMNKkolllokKWMMMMMMMMMMMMMollKMMkllllkKWMM
MkldOXollKMMkllxMMMMMMMMMMMMxlllooloolll0MMMMMMMMMMMMollKMMkllxKkol0M
MWWMMMdllKMMkllxMMMMMMMMMMMMXO0XMxl0WXOONMMMMMMMMMMMMollKMMOllkMMMWMM
MMMMMMNKKMMMkllxMMMMMMMMMMMMMMMN0oldKWMMMMMMMMMMMMMMMollKMMWKKWMMMMMM
MMMMMMMMMMMMXkxXMMMMMMMMMMMWKkollllllldOXMMMMMMMMMMMM0xkWMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMX0xlllok0xlk0xollox0NMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMXollldOXMMMxlOMMWXOdllldWMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMW0OKWMMWKkollldOXWMMN0kKMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMklllooloollo0MMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMXOOXMxl0WKOONMMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMkl0MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMWXMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM

Silly Minty Candycane, well this is what she gets.
"Winter2018" isn't for The Internets.
Passwords formed with season-year are on the hackers' list.
Maybe we should look at guidance published by the NIST?

Congratulations!

elf@6307ca69e75c:~$ 
```