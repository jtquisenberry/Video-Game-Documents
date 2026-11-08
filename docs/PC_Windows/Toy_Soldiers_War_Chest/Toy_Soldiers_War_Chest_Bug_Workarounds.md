---
title: "Toy Soldiers: War Chest Bug Workarounds FAQ"
game: "Toy Soldiers: War Chest"
platform: "PC (Windows, PlayStation 4, Xbox One)"
alternate_titles:
  - "Toy Soldiers: War Chest"
developer: "Signal Studios"
publisher: "Ubisoft"
release_year: 2015
document_type: "Strategy Guide"
author: "Jacob Quisenberry"
version: "1.01"
date: "2026-11-07"
last_updated: "2026-11-07"
language: "en"
tags:
  - toy-soldiers-war-chest
  - bug-workarounds
  - pc-windows
  - playstation-4
  - xbox-one
  - preservation

summary: "Version 1.01 FAQ documenting reported workarounds for the frozen main menu, lost DLC entitlement, a PC black screen, and unavailable trophy/achievement completion. This source is a troubleshooting note, not a unit-stat or hero-tactics guide; platform-specific steps and source caveats are retained."
---

# Toy Soldiers: War Chest Bug Workarounds FAQ

This archive preserves the supplied version 1.01 troubleshooting FAQ. It covers the PC, PS4, and Xbox One workarounds reported by the author and users; these historical steps are not independently verified for current game or system updates. The DLC section describes restoring access for users who already purchased or redeemed the content, not obtaining an entitlement that was never acquired. No screenshots were copied into this document.

## Complete source text

The original text is retained below in a fixed-width block for its tables and codes. Email contact addresses have been omitted.

````text
Toy Soldiers War Chest
Bug Workarounds
v. 1.01


01. TABLE OF CONTENTS

02. INTRODUCTION
03. MAIN MENU FROZEN
  PC
  PS4
  XBOX ONE
04. LOSS OF DLC
  PC
  PS4
05. BLACK SCREEN
  PC
06. BROKEN TROPHY / ACHIEVEMENT
  PS4 - NO SOLUTION
  XBOX ONE - NO SOLUTION


02. INTRODUCTION

Some time around October 2015, the game received an update that rendered it
unplayable. There are workarounds that make the game playable, but there are
other major bugs.


03. MAIN MENU FROZEN

It is not possible to make a selection from the main menu. Therefore, it is not
possible to play anything other than the tutorial mission. 

PC - SOLUTION

Set the system clock to a date/time before October 1, 2015. This date has been
tested to work: August 2, 2015 12:00:00 AM. Changing the system clock can cause
issues with other applications, so I recommend staring the game using NirSoft's
RunAsDate https://www.nirsoft.net/utils/run_as_date.html. 

To set the system date without using RunAsDate, do the following: 

(1) Disable the option to set the date and time from the network.

    Change the date and time -> Set time automatically = Off

(2) Set the date and time.

    Change the date and time -> Set the date and time manually


PS4 - SOLUTION

I have not observed the issue when running update version 1.02. Users who have
encountered the issue work around it by setting the PS4 clock to August 1, 2015.
It is necessary to disconnect the PS4 from Internet, either physically or
through system settings. 

Reference:
https://www.amazon.com/gp/customer-reviews/R9H5AKSFLDNHH/ref=cm_cr_dp_d_rvw_ttl?
ie=UTF8&ASIN=B00YO2PRPS


XBOX ONE - SOLUTION

Users who have encounter the issue work around it by setting the system clock to
January 1, 2015.

(1) Disconnect from the Internet.

    Settings -> General -> Network Settings -> Go Offline

(2) Restart the console.
(3) Change the date to January 1, 2015.

    Settings -> System -> Time -> Date

(4) Load the game.
(5) Connect to the Internet.

    Settings -> General -> Network Settings -> Go Offline
    

Reference:
https://forums.ubisoft.com/showthread.php/1885710-Menu-Screen-Frozen?p=14845763&
viewfull=1#post14845763


It may also be necessary to delete the game's saved options (not the saved
game). When deleting anything, it is best to back it up to USB first.

Reference:
https://forums.ubisoft.com/showthread.php/1885710-Menu-Screen-Frozen?p=13625667&
viewfull=1#post13625667



04. LOSS OF DLC

DLC is available in the Hall of Fame edition of the game. It consists of four
character packs. Users who have purchased the DLC or redeemed it with a code may
lose access to the DLC. It appears that this is a server-level issue. 


PC - SOLUTION

The game includes a development console. 
(1) Rename the game's main executable Game.exe to Game.exe.bak
(2) Copy and rename GameD.exe to Game.exe

    Some users report that they have to use GameP.exe, instead.

(3) Run Game.exe.
(4) Advance to the main menu.
(5) On the gamepad, click both the left and right analog sticks. The development
console will open.
(6) Scroll to "Heroes".
(7) Select it and change option "UnlockAll" from false to true.
(8) Close the development console. 

Steps 4-8 must be performed each time the game is played. The option is not
saved. However, the last character used will continue to be available without
repeating the steps. 


PS4 - SOLUTION

If the user did not redeem the DLC at a time when the online store was
available, it may never be possible to play with the DLC. It seems unlikely that
Signal Studios or Ubisoft will fix the store. 

If the user did redeem the DLC successfully, then some players report that the
DLC becomes available after setting the system date to August 30, 2015. It is
necessary to disconnect the PS4 from Internet, either physically or through
system settings. 

Reference:
https://www.amazon.com/gp/customer-reviews/R9H5AKSFLDNHH/ref=cm_cr_dp_d_rvw_ttl?
ie=UTF8&ASIN=B00YO2PRPS


05. BLACK SCREEN

The PC version of the game may display a solid black screen. It is meant to run
in full-screen mode, but there are graphical display issues. 


PC - SOLUTION

The solution is to run the game in windowed mode. Alt + Enter does not switch
the game to windowed mode; so do the following: 

1. Set the resolution of the monitor to 1366 x 768. 
 
   This will provide enough screen space to accommodate the 1280 x 720 play
area, plus the title bar, plus the Windows task bar (if it is docked on the left
or right).

2. Start the game.

   Wait until the monitor displays a solid black screen. 

3. Start a second instance of the game.

   The second instance of the game will run in a window. If you are running a
single monitor, you may need to Alt + Tab to access the Desktop and start the
second instance.

4. Close the first instance of the game. 

   The remaining instance will continue to run in windowed mode. 


06. BROKEN TROPHY / ACHIEVEMENT

This section is a warning that it is not possible to obtain the platinum trophy
for this game. 

It is believed to be impossible to obtain the Challenger trophy / achievement.
It is not possible to complete the challenges in the GI Joe Survival mission. 

PS4 - NO SOLUTION

Reference:
https://www.playstationtrophies.org/game/toy-soldiers-war-chest/trophy/118069-Ch
allenger.html

XBOX ONE - NO SOLUTION

Reference: https://www.trueachievements.com/a205085/challenger-achievement





CONTACT

Jacob Quisenberry
````
