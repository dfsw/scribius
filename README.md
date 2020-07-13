# scribius


0.2.0
- Fixed various kill table bugs, now defaults to sort by level
- Fixed bug with scanning additional log files that may of resulted in miscounts
- Added ranger lasty tracking to More Info tab
- Added each characters Nemesis
- Fixed unexpected results when scanning and indivual characters logs, then scanning the whole log folder right after
- Fixed a bug that would calculate the incorrect start date on certain occassions
- Calculate effective ranks for Swengus, Evus, Eva, and Sprite trainers
- Not yet calculating effective ranks from ,Erthron, Farly Buff, Bangus Anmash, Forvyola, Bodrus, Hardia, Spiritus, Anemia, Stedfustus, Anan Faure, AnDeux Faure, AnTrix Faure, AnQuart Faure, AnSept Faure, Knox, Anglisa, Atkia,Rodnus

0.2.2b
- Fix for poor Forgus
- Veritus was left out in the cold by his brothers, he has been fixed
- Ya'all rangers are crazy with your logs and how you study things, ive built in several protections for cancelled or otherwise log lost studies sticking around.
- Also fixes for studies where you havent gotten a message yet
- Fixes for whatever drunk GM decided to name two different creatures the same name
- Fixes for what I can only assume is the same drunk GM who set two differently named creatures as the same


 0.2.3b
- Yet another fix on lasty calculations
- All screens now force an update after a complete log scan is complete
- Effective rank calculations added for Erthron, Farly Buff, Bangus Anmash, Forvyola, Bodrus, Hardia, Spiritus, Anemia, Stedfustus, Anan Faure, AnDeux Faure, AnTrix Faure, AnQuart Faure, AnSept Faure, Knox, Anglisa, Atkia, Rodnus (this should be all of them).
- Effective ranks are now calculated and displayed in more info
- Fixed a bug when scanning for new kills could overwrite the saved kills
- Hide trainers that you dont have any ranks in either effective, modified, or trained\
- Improved scanning speed by roughly 300%
- Fix for a redacted trainer not being properly counted because his rank message does not conform to normal style

 0.2.4b
- Fixed a bug with only showing your current lasty if you /use /reflect on your goss more than you do on your belt
- Fixed an off by one bug that would count an extra lasty message that sometimes didnt exist (Lasty counts should be mroe accurate now)
- Bulk rank training for 10 ranks is now included in calcualted total
- Bulk rank training for 1-9 ranks is now noted in the new rank notes field, but not added to the totals.
- Still working through scanning for people with unusual file structures and names, you know who you are.

** You will want to do a full rescan to fix issues from previous versions

  0.2.5b
- Scanning non standard log formats should work better now, ie: edited in a text editor, file names changed, ect. Logs must be in a folder titled with the characters name.
- Fixed several possible crashes when scanning data
- Fixed a possible crash for first time users (sorry! I havent been testing your use case a lot).
- Increase scanning speed by about 25% by optimizing how trainer messages are detected
- Fixed a crash for rangers who have actually successfully /judged another potential ranger
- Better lasty detection
- Failing to detect any characters will prompt the user to save a debug log file (on Rescan All only)
- Fixed an issue not showing ranks that you never trained but had effective ranks in

   0.2.6b
- Fixed a crash that would cause people who used time stamps to not be able to add characters
- Fixed several possible crashes while scanning
- Fixed a bug that might(probably would) count bulk ranks twice if you rescan the same log files


   0.2.7b
- Effective Duvin now takes into account Goss training bonuses
- Numerous improvements to log scanning, presentation and functionality
- Darkstone uses have been replaced with Shadow Bell usage and break rates. (please complain if you still find value in knowing your darkstone uses)
- Support for pet rank tracking
- Support for pet coin level detection
- Vala Loack ranks are tracked properly now
- Added levels for a couple of barbershop creatures, more to come
- Updated Bodrus, Mentus, Spiritus with their Master titles, which fixes an issue with bulk ranks not showing up properly

** You will want to do a full rescan to fix issues from previous versions
