# Anki Quake 3

This project is a fork of IOQuake3 (http://ioquake3.org) designed for learning gamification
in conjunction with the Anki flashcard software package (https://apps.ankiweb.net/).

## Basics
* You can start single player games with bots using this special build of IOQuake3
* You will not be able to pick up any weapons, ammo or powerups off the ground. You will have to earn those by doing Anki reviews. Bots will pick up items/weapons and shoot you with them though.
* You start the game with a Railgun and Rocket Launcher, with no ammo. You can request ammo for them at the cost of 5 anki reviews for each ammo pack (this is configurable). 
* Similarly, you can request Health or Armor.
* When you request items, the bots become paused and will not attack you.
* You can then alt-tab into Anki, which has been notified of your target review count.
* Perform all your reviews in Anki. You will hear audio feedback from Quake3 as you perform your reviews and earn items. You will also hear a sound when all your reviews are done. You can then alt-tab into Quake3 and resume playing.

![Anki Quake 3 screenshot](https://raw.githubusercontent.com/lucwastiaux/anki-quake3/master/screenshots/anki_quake3.jpg)

## Limitations
* You must own a copy of Quake 3 Arena (http://store.steampowered.com/app/2200/Quake_III_Arena/)
* The only items/weapons supported currently are:
   * Railgun (damage changed to 200 instead of default 100)
   * Rocket Launcher
   * Armor
   * Health
* Only windows is supported.


## Setup
* Download current release https://github.com/lucwastiaux/anki-quake3/blob/master/releases/anki-quake3-2018-04-08.zip (Windows 64bit)
* Unzip
* copy all *.pk3 files from your Steam install (C:\Program Files (x86)\Steam\steamapps\common\Quake 3 Arena\baseq3) into anki-quake3/baseq3
* Launch the game once so that it'll create a user profile (start ioquake3.x86_64.exe), but exit right away as we need to do some more setup
* After exiting, open windows explorer and paste this path: 
* Open *q3config.cfg* in a text editor, and add the following lines at the bottom
   * **bind e "toggle bot_pause"**
   * **bind r "request_rail"**
   * **bind t "request_rockets"**
   * **bind f "request_health"**
   * **bind g "request_armor"**
   * **bind q "anki_decrement"**

# Optional setup
seta cl_ankiHostPort "127.0.0.1:27975"