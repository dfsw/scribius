# Scribius

Scribius is a log scanner for the MMORPG [Clan Lord](https://www.deltatao.com/clanlord/). Point it at your text log folder and it will chew through years of logs and tell you pretty much everything there is to know about your exiles: ranks trained, things killed, coins earned, lasties studied, and a bunch of other fun stats.

**Download:** [Scribius.dmg](https://raw.githubusercontent.com/dfsw/scribius/master/Scribius.dmg)

Version 2.0 requires macOS 14 Sonoma or newer. If you're stuck on something older, the 0.4.x versions still work fine. The app checks for updates on its own so you don't have to watch Discord for new versions.

## Features

### Ranks

Every trainer you've trained, sortable by trained or effective ranks, plus the date you last trained them. Trainers you have no ranks in can be hidden. Effective ranks are calculated for all the combo trainers too (Duvin knows about your Goss training, Histia counts ranks earned through Rodnus, the "Master" trainers behave, etc).

### Rank Progress

A chart of your training over time. Watch your total ranks climb, or break it out per trainer, stacked or overlaid, and turn individual trainers on and off. Hover anywhere to see exact numbers for that date.

![Rank Progress](https://raw.githubusercontent.com/dfsw/scribius/master/wiki%20images/scribius1.png)

### Creatures

Everything you've killed, sortable by level, with vanquish/dispatch/slaughter/kill counts, how many times it's dropped you, and when you got your first real kill on it. There's a filter box, and an option to group Fane bosses and ravens together instead of listing each one by name.

![Creatures](https://raw.githubusercontent.com/dfsw/scribius/master/wiki%20images/scribius3.png)

### Info

The character summary sheet: start date, logins, falls, departs, chain usage and break rates, karma, kills per login, ranks per login, your nemesis, environmental deaths, your most common mistake, ethereal portals, shieldstone break rate, casino profit, lifetime coin earnings, and more. Rangers also get their lasty study progress here: befriended creatures (Q/NQ for morph), lastys remaining, and kills since your last study message.

![Info](https://raw.githubusercontent.com/dfsw/scribius/master/wiki%20images/scribius4.png)

### More

- **Coins**: coin earnings and casino wins/losses over time.
- **Modifiers**: adjust any trainer's ranks by hand (for ranks that aren't in your logs). Modified ranks count toward effective totals. The Notes field in the ranks table is editable too, double-click it to add your own.
- **Search**: full-text search across all your logs, with extra context lines if you want them, an option to include player/NPC speech, and a button to reveal the log file a result came from.
- **Pets**: tracks "grows stronger" / "grows much stronger" messages, pet kills, and pet coin level. Pet data can be merged or deleted from the healer More Info area.
- **All Data / Last Scan**: flip the Ranks and Creatures tables between your full history and just what the latest scan found.

![More Info](https://raw.githubusercontent.com/dfsw/scribius/master/wiki%20images/scribius2.png)

## Notes

- First launch: pick your Clan Lord log folder and hit **Scan Logs…**. A full scan of thousands of files takes a few seconds.
- After that, scanning just your new logs updates everything without a full rescan.
- Logs need to be in a folder named after the character. Weird formats are handled (files edited in a text editor, renamed files, timestamps, logs going back to 2002).

## Changelog

### 2.0.2

- Fixed modified ranks showing up in the Ranks table when viewing Last Scan results

### 2.0.1

- Fixed a bug that could mark players as the wrong class

### 2.0

- Major rewrite to move to SwiftData, which will make things faster and more stable but does have the drawback of requiring macOS 14 or newer (2022), you can continue to use an older version if you do not have macOS 14 or newer. You will need to do a full rescan of your logs when moving to this version but your modified ranks should be preserved. SwiftData gives me a lot more flexibility to do a lot of things that I have been wanting to do forever.
- Slightly updated design and layout to be a bit more modern
- Pet data can now be merged and/or deleted from the healer more info area.
- We now track and display the first time you move from a vanq to a kill in the creatures table (helpful for them rangers)
- Lastys now show you how many kills you assisted in since the last message, while not perfect it can clue you into where you are.
- Fixed some bugs that would make lastys that were cancelled not being detected as cancelled and just hang out forever.
- Updated creature database to include all the new stuff added in the last 2 years.
- You can now filter your view by all data or just your last scan data.
- Notes field in ranks is now editable by users, double click on it to add your own rank notes.
- Added some fun new stuff to More Info through the power of SwiftData such as kills per login, ranks per login, lifetime coin earnings, net casino winnings, and a bunch of other fun stuff.
- Log search has been rethought and is much more useful, even allowing you to reveal the log file the search result was found in.
- Further backwards compatibility, now with full support for logs going back to 2002! If you have older logs that aren't scanning send them my way and we will go even further back into compatibility.
- In theory should handle Windows log files (though requires a Mac to run), could use some more test files from Windows machines for debugging though.
- The app now tries to correctly sync up unknown An* trainers to proper ones assuming you set them both in modified ranks.
- Added a really neat rank progression chart to show you how your training has trended over time.
- Bunch of other stuff, totally not abandonware ;p

### 0.4.3b

- Fix for a crash on first launch for people upgrading from an older version

### 0.4.2b

- Hotfix for Core Data Crash

### 0.4.1b

- Woodworking trainer and support added
- Fix for sandboxing issue that was messing up some data
- Fixed a bug that could prevent lastys from being shown
- Easier editing of modifier ranks (select in table)

### 0.4.0b

- Completely rewrote and refactored how data is stored and processed, which will open the door for a bunch of really awesome new features down the road
- Updated monster coin values (Shadowplane, Orionwood, and Bookfort areas)
- Fixed an issue that would improperly count deaths to unique boss names
- Provided an option to group Fane Bosses and Ravens in the kill list instead of breaking them out by name
- Better filtering out of illogical monster names
- Better profession detection for exiles who have not chosen a profession
- Detection of older pet grows much stronger message (that uses Kennel)
- Fixed typo with Loovma and Angilsa that prevented you from modifying those ranks
- Rank modifier menus are now alphabetical
- Added support for Darktur
- Fixed a bug where a modified rank may not appear if you have never trained it (Also added a new preference for this)
- Finally have an icon
- Trainer table now shows the date it was most recently trained
- Effective ranks are now calculated for combo trainers, effective ranks is also now more accurate
- With log searching you can now display X additional lines after your search result
- Integrated automatic update checking so you dont have to watch Discord for new update messages anymore

(A full Scan All is required for continued use)

### 0.3.2b

- Fixed a bug that was preventing certain bulk training to be counted properly
- Loovma Geer now knows his own name, same with Skea Brightfur and Dentir Longtooth
- Updated formulas for Hardia (spoiler it sucks more)
- Radium was missing from our trainer list so that has been added.
- Fixed a bug that would incorrectly add bulk training ranks to traditional training ranks
- Added assorted new monsters to the directory
- Stability enhancements
- Fixed a bug that was preventing casino winnings (and losing) from showing

### 0.3.1b

- Users with multicore machines should see massive speed improvements in the area for 2-8x faster scanning
- Log searching now includes an option to search through player and NPC speech (or ignore speech as the default)
- Fixed a bug that would confuse players /actions Grows Much Stronger! as a pet rank
- Better support for monsters with a "The" in their name
- Filter functionality added to kill table
- Fixed a bug that could make some ranks disappear on scan new logs if you have a modified rank associated with it
- Fixed a bug that didnt understand trying to over bulk train with pathfinding books. (You have completed what you can without consulting)
- Fixed a bug that would miscalculate the number of lastys remaining on low number of a lot messages.
- Trainer info added for Master Janis' Mental Mysteries
- Fixed a bug that was preventing Loomva ranks from scanning properly

### 0.3.0b

- Major code refactor to make things more stable and faster
- We know understand and properly handle raven kills.
- We no longer let exiles fake being pets by using certain key words in /actions, take that Shaky's pet Arod.
- Rodnus ranks now count towards effective rank totals
- Fixed an internal bug dealing with coin level that no one would of ever noticed but it doesnt happen anymore
- Cleaned up monsters and coin level things, should hopefully see less unknown levels on things
- Lastys during befriend counting now show a Q if you are qualified for Morph or NQ if you are not qualifed for morph
- Characters are now listed in alphabetical order
- Trainers are now listed in alphabetical order

### 0.2.8b

- Should crash less if we find something unexpected.
- Fixed an issue that prevented shadow bell breaking percentage from showing up
- Fixed a bug that would show the incorrect effective ranks total when entering a new modified rank
- Fixed another bug that would show incorrect effective ranks when scanning new logs
- Effective histia now takes into account histia earned through Rodnus
- Should now better detect young blood mages
- Added ability to save debug logs when a recoverable error occurs
- Fix for modified ranks using the three "Master" trainers.
- Fix for some very old logs having missing ranks in them because the format on those rank messages has changed over time
- Various pet tracking fixes
- Monsters with a ' in the name should be happier
- Some improvements to the reliability of lasty detection
- Captured creatures (circle test) now behave as they should

### 0.2.7b

- Effective Duvin now takes into account Goss training bonuses
- Numerous improvements to log scanning, presentation and functionality
- Darkstone uses have been replaced with Shadow Bell usage and break rates. (please complain if you still find value in knowing your darkstone uses)
- Support for pet rank tracking
- Support for pet coin level detection
- Vala Loack ranks are tracked properly now
- Added levels for a couple of barbershop creatures, more to come
- Updated Bodrus, Mentus, Spiritus with their Master titles, which fixes an issue with bulk ranks not showing up properly

**You will want to do a full rescan to support pets and fix issues with Master trainers and Vala Loack**

### 0.2.6b

- Fixed a crash that would cause people who used time stamps to not be able to add characters
- Fixed several possible crashes while scanning
- Fixed a bug that might(probably would) count bulk ranks twice if you rescan the same log files

### 0.2.5b

- Scanning non standard log formats should work better now, ie: edited in a text editor, file names changed, ect. Logs must be in a folder titled with the characters name.
- Fixed several possible crashes when scanning data
- Fixed a possible crash for first time users (sorry! I havent been testing your use case a lot).
- Increase scanning speed by about 25% by optimizing how trainer messages are detected
- Fixed a crash for rangers who have actually successfully /judged another potential ranger
- Better lasty detection
- Failing to detect any characters will prompt the user to save a debug log file (on Rescan All only)
- Fixed an issue not showing ranks that you never trained but had effective ranks in

### 0.2.4b

- Fixed a bug with only showing your current lasty if you /use /reflect on your goss more than you do on your belt
- Fixed an off by one bug that would count an extra lasty message that sometimes didnt exist (Lasty counts should be mroe accurate now)
- Bulk rank training for 10 ranks is now included in calcualted total
- Bulk rank training for 1-9 ranks is now noted in the new rank notes field, but not added to the totals.
- Still working through scanning for people with unusual file structures and names, you know who you are.

**You will want to do a full rescan to fix issues from previous versions**

### 0.2.3b

- Yet another fix on lasty calculations
- All screens now force an update after a complete log scan is complete
- Effective rank calculations added for Erthron, Farly Buff, Bangus Anmash, Forvyola, Bodrus, Hardia, Spiritus, Anemia, Stedfustus, Anan Faure, AnDeux Faure, AnTrix Faure, AnQuart Faure, AnSept Faure, Knox, Anglisa, Atkia, Rodnus (this should be all of them).
- Effective ranks are now calculated and displayed in more info
- Fixed a bug when scanning for new kills could overwrite the saved kills
- Hide trainers that you dont have any ranks in either effective, modified, or trained
- Improved scanning speed by roughly 300%
- Fix for a redacted trainer not being properly counted because his rank message does not conform to normal style

### 0.2.2b

- Fix for poor Forgus
- Veritus was left out in the cold by his brothers, he has been fixed
- Ya'all rangers are crazy with your logs and how you study things, ive built in several protections for cancelled or otherwise log lost studies sticking around.
- Also fixes for studies where you havent gotten a message yet
- Fixes for whatever drunk GM decided to name two different creatures the same name
- Fixes for what I can only assume is the same drunk GM who set two differently named creatures as the same

### 0.2.0

- Fixed various kill table bugs, now defaults to sort by level
- Fixed bug with scanning additional log files that may of resulted in miscounts
- Added ranger lasty tracking to More Info tab
- Added each characters Nemesis
- Fixed unexpected results when scanning and indivual characters logs, then scanning the whole log folder right after
- Fixed a bug that would calculate the incorrect start date on certain occassions
- Calculate effective ranks for Swengus, Evus, Eva, and Sprite trainers
- Not yet calculating effective ranks from ,Erthron, Farly Buff, Bangus Anmash, Forvyola, Bodrus, Hardia, Spiritus, Anemia, Stedfustus, Anan Faure, AnDeux Faure, AnTrix Faure, AnQuart Faure, AnSept Faure, Knox, Anglisa, Atkia,Rodnus
