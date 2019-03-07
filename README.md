# OpenPatch-NDSGameList

I made this repo because the most updated GameList for nds AP-Patches was dated, very dated. Not all games have patches working and some would need an updated patch. Most patches are only made to patch a certain dump, and given how I saw at least 3 different groups releasing clean nds roms....  I'll focus most of the time on patching No-Intro roms. Usually the patch was done for the first clean rom dumped.

# Usage
Drag the nds rom to [OpenPatch.exe](https://github.com/Intervencion/OpenPatch-NDSGameList/releases). [GameList.txt](https://github.com/Intervencion/OpenPatch-NDSGameList/blob/master/GameList.txt) must be on the same folder than the binaries. If a patch is found, it will patch it and ask whether you want to backup your rom or not. Left button is Yes, right button is No. If it displays error starting with TEXT, your game wasn't found on the txt.

If you wish to add a game to the GameList, be sure to check its other versions (USA/EUR/JPN/German/Italian/etc) to see if they have a patch. If so, you can compare with [HxD](https://mh-nexus.de/en/hxd/) the hexadecimals in the marked offsets and see if they're the same (most likely they will not).

For example, to add Pokémon HeartGold in Spanish from No-Intro I checked both EUR and Germany patches. Found out the offsets of all but the last line were the same, so I could safely patch it knowing I just needed to transcribe the hexadecimals from the Spanish rom to the txt. The last one was a bit trickier, because Germany had 000DF41A whilst Europe had 000DF41B. Hexadecimal was D1 on both so I could patch it with offset 000DF41B in the Spanish rom since that exact offset had an hexadecimal value of D1.

If all of this seems too complicated to you, feel free to add an issue with the rom you wish to patch (just give me the game name and the group's name, and the rom's [CRC](http://rapidcrc.sourceforge.net/) and I'll check what I can do. I don't know coding, I didn't made any actual patch. I just try to re-use what is already done.

Some games have XDelta patches. Those are esentially the same, just using a different software. Make sure to backup the source rom and compare the hexadecimals between pre and post XDelta patch. You'll be able to see there the patch and be able to transcribe it to the txt file.

With [DS-Scene Rom Tool](https://gbatemp.net/threads/repack-ds-scene-rom-tool-v1-0-build-1215-includes-cmp-and-ap-database.477193/) you can AP-Patch games, listed on an AP Database. Always try this first because it's actually more User friendly.

# Disclaimer
I did not make OpenPatch. I'm not a programmer. Huge credits to its author(s) I'm just adding it on releases to make it easier for users to find it.
