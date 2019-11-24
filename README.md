Sentinel+ Import Tool

This is a backup tool for CIty of Heroes

You'll need to run this from the command line, but hopefully it shouldn't be too difficult for non-tech savvy users.

Usage

As always back up your XML files before doing anything! This tool does not modify them, but it's strongly recommended to always have a good backup in case of accidental foot-shooting like switching the order of the input and output files.

xml2db [authid] [authname] [bin.pigg] [xmlfile] [txtfile]

authid: The ID number for the game account the character will go on. You can get this in-game by turning on self-info with the GM commands.
authname: The name of the game account - same thing you type in on the login screen.
bin.pigg: Path to your bin.pigg file.
xmlfile: Sentinel+ XML file to be converted.
txtfile: Output file to create.

Example:
xml2db 150 myaccount C:\CoX\piggs\bin.pigg CoolGuy.xml CoolGuy.txt

Once you have the output file, you can open the file with your browser/editor (try Notepad++) to look at the file. If you have your own private CoX server, you can use mapserver in dbquery mode to import it.

bin\dbquery.exe -putcharacter CoolGuy.txt

Download



Source

https://github.com/Hal47/xml2db

Notes & Caveats

Sentinel+ only exported information that the client had access to, which means a lot of stuff is missing, especially state related to mission/contact completion. This tool attempts to correct some of the bigger issues related to accolade powers and inventory sizes, but it is far from comprehensive and there may be some slight irregularities, especially related to having badges for arcs that the game doesn't think you've completed yet.

All characters processed by this tool are granted the Passport badge.

Based on the original Sentinel+ made by Codewalker.