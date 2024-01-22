# 1.2.1
+ **Improvements**
  + Vanilla Boombox interactions through LMB are now smarter
    + If you own the current or last played track, activating the Boombox will now respect the playback modes you have set in DiscJockey (sequential, shuffle, repeat)
    + If you don't own the current or last played track, activating the Boombox will play the first track in your tracklist
+ **Fixes**
  + DiscJockey will now accurately reflect rebound keybinds in the hovertip and controltip for the Boombox when using InputUtils
  + First time downloads of yt-dlp and ffbinaries will no longer fail and abort for users that have double-byte characters (JP/CN/KR characters, some accented characters, etc.) in their path or in their machines hostname
  + You can now open DiscJockey while looking at a Boombox even when holding an item
  + Fixed a rare case in which DiscJockey's audio can desync if a player holding the Boombox activates it through LMB while another player has the DiscJockey UI open
  + DiscJockey will behave significantly better with item interactions now (most notably with ReservedItem mods) (thank you @Rhapsody, @grandteki and @flipf17 !)
    + DiscJockey was originally disabling player Interact input when the panel was open - this appears to break Vanilla interact behaviour in some bizarre, buggy fashion. This has been reworked into a prefix instead.

# 1.2.0
+ **New features**
  + Added a delete button to tracklist buttons - note this won't delete the file, it'll just remove it from your tracklist
  + New config options:
    + Permanently Keep Downloaded Songs - this will make downloaded songs save directly to your Custom Songs folder and bypass all caching mechanisms. False by default.
    + Add Vanilla Boombox Music To Tracklist - added the vanilla Boombox music to your tracklist. False by default.
    + Enemies Hear Music **[SYNCED WITH HOST]** - this was actually a bug that I decided to turn into a config option. True by default, but when False enemies like the blind dog and slime won't hear the Boombox.
+ **Fixes**
  + Players can now interact with DiscJockey by looking at it *even when* it's held by another player.

# 1.1.3
+ **Fixes**
  + Fixed issue preventing youtu.be URLs from being parsed correctly (thanks @Leader!)
  + Fixed issue preventing DiscJockey from progressing to the next track while the Boombox was unmonitored (not held or not looked at) (thanks @Kalem!)

# 1.1.2
+ **Fixes**
  + Fixed folder structure when using r2modman
  + Fixed audio with a sample rate lower than 48khz playing back incorrectly (thanks @NotSoEvilDead!)
    + Audio lower than 48khz is now resample on the fly due to Opus codec requirements
  + Fix tracklist buttons not resetting indicator state when playback stopped
  + Made the download cache less angry about doing its job
  + Added fix to the Netcode patch init method for InputUtils soft dependency
  + Updated config description for Keybind to be explicit that the InputUtils binding takes priority over it

# 1.1.1
+ Lets try uploading the correct README this time...

# 1.1.0
+ **New features**
  + Codebase rewritten to implemented realtime audio streaming
  + Networked config syncing (where applicable)
  + A variety of new config options:
    + Interface colour
    + Interface transparency
    + Disable battery drain **[SYNCED WITH HOST]**
    + Networked volume control **[SYNCED WITH HOST]**
    + Default Boombox volume
  + Direct support for Youtube playlists
  + UI improvements
  + Escape key now closes DiscJockey
  + You can now open DiscJockey while looking at a Boombox
  + Implemented smarter download caching
  + Added track scrolling effect to now playing and buttons on hover
  + Added support for [LethalCompany InputUtils](https://thunderstore.io/c/lethal-company/p/Rune580/LethalCompany_InputUtils/) for in-game rebinds
+ **Fixes**
  + Fixed song duplication issue (GH [#4](https://github.com/Yoshify/DiscJockey/issues/4))
  + Changed OnLoadAllAudioFromDirectory from LogError to LogWarning if empty (GH [#5](https://github.com/Yoshify/DiscJockey/issues/5))
  + Duplicated tooltip bug fixed (GH [#5](https://github.com/Yoshify/DiscJockey/issues/5))
  + Fixed tracklist sorting desync
  + Fixed rare issue causing DiscJockey to shut off when Boombox was pocketed (thanks @broiiler!)
  + Fixed issue causing downloaded content with unicode characters to fail loading
  + Added timeout to YT-DLP so that if it *does* get stuck, it'll bail out after 30 seconds
  + Mading playing/stopping tracks from outside the UI with left-click more reliable
  + A plethora of other community reported bugs
+ **Removed**
  + **Track scrubbing** - might make a return, the tradeoff of making it work with real-time streaming wasn't worth the effort in my opinion. If the community wants it badly enough, I'll revisit.
  + **Chat alerts**
+ **Dependencies**
  + Added `Concentus`, `UniTask` and `NAudio`

# 1.0.1
+ Added MD5 Checksum verification to FFBinaries downloads

# 1.0.0
+ Initial release