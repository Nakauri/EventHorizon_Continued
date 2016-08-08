# Change Log

## [Unreleased](https://github.com/Brusalk/EventHorizon_Continued/tree/HEAD)

[Full Changelog](https://github.com/Brusalk/EventHorizon_Continued/compare/v1.9.11...HEAD)

**Fixed bugs:**

- Error from 1.9.11 [\#6](https://github.com/Brusalk/EventHorizon_Continued/issues/6)

**Merged pull requests:**

- V11 wip [\#5](https://github.com/Brusalk/EventHorizon_Continued/pull/5) ([Brusalk](https://github.com/Brusalk))
- Update config.lua [\#1](https://github.com/Brusalk/EventHorizon_Continued/pull/1) ([Cluuey](https://github.com/Cluuey))

# Historical Changelog:

### v1.9.11
  Brusalk - Sat Jul 23 03:17:26 2016 -0700
      Merge pull request #5 from Brusalk/v11_wip
      
      Added many class configs kindly provided by the users.
      Fixed Green texture display bug. Greatly improved user experience with empty or nearly-empty
      class configs. Fixed all the bugs.
  Brusalk - Sat Jul 23 03:13:21 2016 -0700
      Fix green texture display bug

      Blizzard separated out setting textures from SetTexture into a new SetColorTexture.

  Brusalk - Sat Jul 23 02:40:24 2016 -0700
      Improved user experience with empty class configs

      EH now hides the whole frame when there are no active spellbars or an empty spellconfig is present.

      If there's no spellconfigs a helpful message is displayed to the user outlining why. Once per
      week, the player is shown a message explaining why EH isn't shown if their spell-config happens
      to now allow _any_ bars to show.

      Also changed default appearance to more gracefully handle low-numbers of active bars. (Turned on
      config.staticframes to 4). Slightly widened default icon width.

      Bugs Fixed: Fixed Delayed Load issue with ArtifactLib. Fixed improper display of hidden popups
      if earlier popups were not hidden forever.

  Brusalk - Sat Jul 23 00:36:53 2016 -0700
      Fixed cata talent req for real this time. Now only show DG/Infernal if GoSUP isn't talented.

  Brusalk - Sat Jul 23 00:36:01 2016 -0700
      Enabled staticframes on by default, and widened default icon-width and individual bar
      height.

      This should help EH gracefully scale to low numbers of active spell bars. The numbers are
      turned such that it'll appear that EH grows up to 4 bars, and then begins to shrink each bar to
      stay within the static-height.

  Brusalk - Fri Jul 22 23:50:21 2016 -0700
      Destro Warlock config now properly displays cata only when talented

  Brusalk - Fri Jul 22 01:14:10 2016 -0700
      Added Holy/Disc priest config provided by Sig!

  Brusalk - Fri Jul 22 00:58:09 2016 -0700
      Added Enhance Shammy Config provided By StragaSevera!

  Brusalk - Fri Jul 22 00:55:21 2016 -0700
      Fixed ele shaman config apocalypse

  Brusalk - Fri Jul 22 00:54:51 2016 -0700
      Added Sub Rogue Config kindly provided by Neloangelo13!

  Brusalk - Fri Jul 22 00:45:31 2016 -0700
      Added MM Hunter to display list

  Brusalk - Fri Jul 22 00:44:40 2016 -0700
      Added Hunter config provided by Stilmore!

  Brusalk - Fri Jul 22 00:42:13 2016 -0700
      Updated TOCs to match actual live version number

  Brusalk - Fri Jul 22 00:34:10 2016 -0700
      Added Shadow Priest Class Config provided by Vaelynn

  Brusalk - Fri Jul 22 00:33:35 2016 -0700
      Added Discord/Github Notifications on Login

  Brusalk - Thu Jul 21 23:37:00 2016 -0700
      Added Aff/Demo to Legion Class Config Status

  Brusalk - Thu Jul 21 23:31:20 2016 -0700
      Updated Warlock Class Config with Config provided by BackJauer Warlock Class Config with Config provided by BackJauer

### v1.9.10
##### Core
- Added requiredArtifactTalent requirement with 3 usages:
- 1) requiredArtifactTalent = spellID | Bar has a requirement that the given artifact talent (by passive SpellID) has at least one rank selected
- 2) requiredArtifactTalent = { spellID, rank# } | Bar has a requirement that the given artifact talent (by passive SpellID) has at least 'rank' number of points selected
- 3) requiredArtifactTalent = { { spellID1, rank1 }, { spellID2, rank2 }, ... , { spellIDN, rankN } } | Bar has a requirement that all spells must have at least their associated number of ranks
##### Class Configurations
- Rogue
- - Added Assassination Class Config kindly provided by PessimiStick

### v1.9.9
##### Core:
- Updated core addon functionality for legion beta
##### Class Configurations:
- Warlock
- - Implemented Destro Warlock Spec Class Configs
##### Misc Notes:
- I do not have the time or will to update every class config for every new spec/class redesign for Legion. In the past this has taken me upwards of 80 hours, and I don't have the will anymore.
- If your class/spec has not yet been implemented, please give me a class/spec config for Legion beta, and I will add it to the default for the addon. I just can't proactively do this anymore.
- I love each and every one of you. (I love you more if you give me a class/spec config too! ^.^)

### v1.9.8
##### Class Configurations:
- Hunter
- - Fixed GCD tracking
- - Removed old spell IDs that no longer exist
- Warlock
- - Fixed missing Dark Soul bars for Affliction and Demonology

### v1.9.7
##### Core:
- Removed addon load spam from being on by default.
##### Class Configurations:
- Hunter
- - Fixed Dire Beast to properly display cooldown and playerbuff
- Druid
- - Removed references to spells which no longer exist

### v1.9.6
##### Core:
- Updated opening message
##### Class Configurations:
- All class configs are updated to my best guess, or as supplied by the community (Thanks!)

### v1.9.5-Beta-4
##### Core:
- Fixed GetAddOnInfo bug disabling get via name and enabled returning false for Load on Demand addons always.

### v1.9.5-Beta-3
##### Core:
- Fixed GetTalentInfo and GetSpecialization bug causing talents and abilities to display incorrectly.
- - GetSpecialization was functioning incorrectly for requiredTree = {0, ...} class configs.

### v1.9.5-Beta-2
##### Core:
- Fixed notification error w/ fresh EventHorizonDB variable.

### v1.9.5-Beta-1
##### Core:
- Got core working for WoD. (First rev.)
- Added notification on first load (one time only) about current state of addon and WoD class config status.
- Fixed GetTalentInfo, GetSpellInfo, and GetNumTalents MoP -> WoD incompatibility issues. 

### v1.9.5-15
##### Core:
- Added the "Adding [bar]" debug messages on login/retalent to debug output only.
##### Class Configurations:
- Druid
- - Separated sunfire/moonfire spells into two separate bars
- Hunter
- - Fixed Dire Beast showing for all specs when untalented
- Rogue
- - Applied fix for Shadowblades

### v1.9.5-14
##### Class Configurations:
- Druid
- - Fixed issue in config around dream of cenarius talent. Should work again
- Rogue
- - Updated completely for MoP

### v1.9.5-13
##### Class Configurations:
- Warrior
- - Removed Deadly Calm (No longer in-game)
- Hunter
- - Fixed a typo causing major issues

### v1.9.5-12
##### Class Configurations:
- Shaman
- - Fixed configuration error with level 60/90 talents.

### v1.9.5-11
##### Core:
- Added support for requiredTalent (graciously given to me by Sylna (http://www.curseforge.com/profiles/Sylna/))
##### Class Configurations:
- All
- - Added appropriate talents that weren't there before due to requiredTalent limitations
- Hunter
- - Removed Readiness
- Warlock
- - Added Havoc
- - Added RoF

### v1.9.5-10
##### Core:
- Changed the refreshable config option to be always true unless explicitly set to false. Shouldn't break anything and should fix tick issues when refreshed
##### Class Configurations:
- Warlock
- - Added missing comma
- - Unstable Affliction will now correctly show ticks every 2 seconds unhasted

### v1.9.5-9
##### Core:
 - Removed the spellIDs in tooltips showing by default. If you wish to enable them again, edit the line in EventHorizon.lua that reads local spellIDsEnabled = false to local spellIDsEnabled = true
##### Class Configurations:
 - Paladin:
 - - Prot:
 - - - Removed Inquisition
 - - - Fixed spellIDs
 - - Holy:
 - - - Fixed SpellIDs
 - - All:
 - - - Fixed Judgment SpellID

### v1.9.5-8
##### Core:
 - Fixed playerbuff/debuff not being interpreted correctly.
##### Class Configurations:
 - All Classes
   - Fixed errors in class configs partially causing playerbuffs/debuffs to not be interpreted correctly. All intended debuffs/buffs should show correctly now
 - Rogue:
   - Fixed Sub Hemo bar. Should now correctly show Hemo DoT duration
 - Priest:
   - Added PoM CD to renew bar
 - Paladin:
   - Removed spellIDs which do not exist from class configuration

### v1.9.5-7
##### Core:
 - Identified and probably fixed a bug with SetPoint calls creating Script Ran Too Long errors.
##### Class Configurations:
 - Priest
   - Removed stance reqs for shadow spells
   - All casts are now shown for non-shadowform spriests and healers
   - Renew is also shown for non-shadowform spriests
 - Warlock
   - Commented out Soul Swap for affliction. If you want it back delete the line it says to delete to get it back
   - Fixed error with Shadowflame debuff dot. Should now correctly show the debuff's ticks
   

### v1.9.5-6
##### Core:
 - Identified a bug with playerbuff and debuff for class configurations not being interpreted correctly. Working on a fix but it's taking longer than anticipated
##### Class Configurations:
 - Hunter
   - Added support for all DPS increasing talents in the 60 and 75 talent range. Just have to uncomment the ones you want to show and comment out the ones you don't
   - Fixed a few talents to work as intended
 - Warlock
   - Fixed Agony/Corruption now showing for Affliction (related to bug with multiple debuff definitions per bar)
   - Fixed error with Destruction not showing. (Turns out I added an extra 3 somewhere :P)

### v1.9.5-5
##### Class Configurations:
 - Druid:
   - Fixed issue with an unexpected equals sign on line 34. Turns out I accidentally deleted the self:newSpell({ line. Oopsy :P
 - Shaman:
   - Added back in Lightning Shield stacks as well as keeping the icon on Lightning Shield so stacks are always shown on the icon.

### v1.9.5-4
##### Class Configurations:
 - Mage:
   - Fixed issue with talents for fire mages.
 - Shaman:
   - Slightly Updated Elemental Shaman configuration.

### v1.9.5-3
##### Class Configurations:
 - Fixed errant newSpell() in disc priest config.
 - Vampiric Touch now has a recast line
 - Mind Melt correctly shows on Mind Blast bar.
 - Added Mind Flay/Devouring Plague bar to Shadow

##### Core:
 - Fixed typo in newSpell() which prevent auraunit config option from working as intended

### v1.9.5-2
##### Lots of fixes!

##### Class Configurations:
 - All classes should be working 100% save for Brewmaster Monks
 - Fixed icon/auraunit issues for Fire Mages

##### Core:
 - Fixed requiredGlyphs to have correct functionality in MoP
 - Fixed newSpell() to work 100% correctly for all configurations possible.

### v1.9.5-1:
##### Fixed an error in the config.lua file making it harder to understand


### v1.9.5:
##### Fully and completely working version of EventHorizon for MoP
##### Class Configurations:
 - All are now supported except for Brewmaster Monks
##### Core:
 - Everything should be working 100%. Trinkets may be bugged.

### v1.9.4-3: 
##### Class Configurations:
 - Hunter: Updated for MoP
 - Druid: Updated for MoP. Balance may not be working 100%
 - Monk: Added and updated for MoP. Missing Brewmaster
 - Warlock: Affliction updated for MoP. Demonology and Destruction Missing

### v1.9.4-2:
* Class Config's can now use a table of cooldowns. EH will use the longest CD of the provided spells. cooldown = {spell1, spell2, ...}
* Uncommenting the first line will enable the display of spell IDs in tooltips to assist in identifying the spellIDs of talents.
* Misc fixes
* Hunter: Should now be compatible with MoP abilities.
* Shadow Priest: Now Compatible with MoP abilities inc mindbender/sfiend cd and lvl 90talent cd bar

### v1.9.4-1: MoP Beta (5.0) compatibility. This is NOT compatible with 4.3. ONLY FOR BETA


### v1.9.3-4: WoW 4.1 compatibility. COMBAT_LOG_UNFILTERED events had an extra argument (hideCaster) added after the event arg.
* Little note if you're hacking from an older version, you can search through EventHorizon.lua using a regex of ",\s*event,\s*" and replace with ", event, hideCaster, ". Just watch what you're replacing, there's a couple hits with that which you don't want to replace. Notepad++ handles this very nicely.

### v1.9.3-3:
* Death Knights really do exist.
* Mage: Changed the GCD spellID and haste comparison spell to Polymorph. May work a bit better for some players.

### v1.9.3-2: Kinda.
* Core: See v1.9.3 notes below for most notes.
* Core: Made some changes to the stack indicator code to hopefully work a bit better. May not play nice with glyph-refresh stacks, let me know.
* REMOVAL - Core: Tick detection is once again (mostly) v1.9.2 code. It was accurate for the most part but did NOT play nicely with some spells.
* REMOVAL - nonAffectingHaste removed.
* Warlock: Removed Drain Mana references, as the spell no longer exists.

Note: I don't have an account, so this release is pretty much triage to fix a few 

### v1.9.3: Mmm, ticks. And math. And updates.
* Core: Tick detection has been completely rewritten and is nearly 100% accurate. I'll spare the details here, check beta comments for how it all works.
* Core: Added a NewSpell flag, 'smallCooldown', indended to improve visibility of certain auras without removing their cooldowns. See the Priest config (Devouring Plague bar) for usage.
* Core: Redshift may now be enabled via slash command when disabled via config.lua. (see note)
* Core: Single spell stack numbers (or spells that show a single stack for no reason) are no longer displayed.
* Core: Recast lines were using some incorrect info in certain conditions.
* Core: Buffs cast by other players should no longer cause EH to panic.
* Core: Various module API refinements, little fixes across the board, and probably a lot of stuff I haven't mentioned in the changelog so far.
* Config: Added a new entry for use with the tick-related changes, nonAffectingHaste = {spellID,multiplier} or {{spellID,multiplier},{spellID,multiplier},...}.
 - Warlocks seem to be the only ones needing this at present. If you find other spells affecting cast haste but not tick haste, and your ticks are improperly calculated because of it, by all means let me know.
* Config: Added a new entry to the layout section for the smallCooldown NewSpell flag.
* Druid: Removed Omen of Clarity across all specs. Revive used as haste comparison.
 - Feral/Cat: Bars reorganized to better reflect priorities.
 - Feral/Bear: Added Swipe CD to Pulverize. Enrage removed (commented out if you prefer seeing it).
 - Balance: Shooting Stars added to Starsurge.
 - Resto: Tweaks a'la malsudon.
  + Moved Swiftmend cooldown to the Rejuvenation bar.
  + Added Nature's Swiftness cooldown to the casted heals bar.
  + Added Tree of Life.
* Mage: Conjure Refreshment used as haste comparison.
* Hunter: Steady/Cobra bar now tracks Improved Steady Shot (with recast segment).
 - BM: Usability tweaks.
  + Frenzy bar now tracks Focus Fire cooldown, Focus Fire buff is no longer tracked (same CD as buff time).
  + Killing Streak is now shown on Kill Command as originally intended.
 - Marks: Aimed Shot cast and Master Marksman buffs moved to Chimaera Shot bar.
* Paladin: Redemption used as haste comparison.
* Priest: Resurrection used as haste comparison.
 - All specs: Evangelism and Archangel folded into a single bar.
 - Shadow: Please spend some time on the target dummy to get used to the changes. Most will find the layout more intuitive than it has been in recent releases.
  + Moved Shadowfiend CD to the Devouring Plague bar. Uses the new smallCooldown flag to improve usability.
  + Filler separated into two bars. Cast filler tracks Mind Melt buff, channel filler tracks Shadow Orbs.
  + Moved Shadow Word: Death CD to the channel filler bar.
* Shaman: Ancestral Spirit used as haste comparison.
* Warlock: Create Healthstone used as haste comparison. Eradication defined as not affecting DoT haste.

Redshift note: You may need to repeat the command a couple of times due to an elusive little glitch, but the settings stick between login/reloadui without further issues.
Redshift remembers your last enableRedshift setting from config.lua. If that's changed, Redshift will default to whatever the new setting is.

### v1.9.2: Switched to Git, revision numbers go byebye.
* Core: Added a 'recast' NewSpell flag. 'recast = true,' (or really anything but nil/false) will force the recast segment to show for any aura on the bar.
* Core: Recast lines will try to use the most recent tracked spellcast. (see note)
* Probably some more fixes and changes here and there, but not many. Been focusing on getting things set up with the new repository.

Note: Let's say a bar is tracking a proc and two spells with differing cast times, with the recast flag on. The following situation may happen:
1 - Begin a 1.5 second cast (which procs the aura)
2 - Cast completes and spell's in the air. Begin a 3 second cast (which doesn't proc the aura)
3 - The procced aura appears with a 3 second recast segment, which probably isn't what you wanted to see.
I'll be adding a way to set which casts affect the recast duration in a later release, probably in v1.9.3. For now I don't believe it'll be a huge issue to leave it as is.

### v1.9 r378: Eep again.
* Core: Aura info is no longer indexed by spellID. EH now behaves much better in a raid environment.

### v1.9 r377: Eep.
* Core: Fixed error spam when mouseover units are being actively tracked.
* Core: Increased the period between mouseover aura checks from ~100ms to ~150ms.

### v1.9 r376: Hopefully that's the last time I'll have to fix Redshift.
* Core: Made some huge changes to how aura information is collected and stored. (see note)
* Core: Redshift now has (almost) complete control over frame visibility when enabled.
* Core: Indicators now use the API methods introduced in 4.0.1 to set their drawing order, instead of relying on framelevel hacks. Less CPU usage, more stable ordering.
* Core: Cooldowns are now prioritized over [de]buffs in terms of drawing order.

Note: I haven't had the opportunity to test every variation, but it seems stable enough. Let me know of any issues.

### v1.9 r370: Trinket bars will be disabled by default from this release onward.
* Core: Cast-time debuffs no longer leave a bar segment behind when dispelled or the target dies.
* Core: itemID bars now use the correct GetSpellCooldown syntax.
* Core: Fixed some load order issues that were preventing Redshift from doing its thing at login.
* Core: Added a few API triggers for module usage, fixed some event assignments, and cleaned up a few bits of code.
* Config: Trinket bars are now disabled by default. Look for "config.showTrinketBars" in config.lua if you prefer to see them.
* Class Config: Added an 'icon' NewSpell flag - Sets a static icon for the bar. Can use a spellID, itemID, or texture path. Not usable with equipment slot bars.
* Paladin: Holy Shield has been fixed and folded into the CS/HotR bar, Sacred Duty added to Prot Judgement.
* Warlock: Corruption bar now uses only the Corruption icon. Chaos Bolt's cast is no longer missing from the Destro filler bar.

### v1.9 r362: SavedVariable wipe for people affected by r335 quirks. The new class config system has been delayed for now.
* Core: Talent/glyph checks are now throttled and delayed using the same method as gear checks.
* Core: The recast bar segment should no longer glitch out when recasting or refreshing dots.
* Core: The hideIcons option was broken in a namespace cleanup a while back. This has been corrected.
* Core: Most bar components and some portions of the EventHorizon window may now have their blending mode adjusted. (see note)
* Config: Added config.blendModes to config.lua. See the notes there for usage. (note again)
* Config: The default channel tick color has been changed from class color to castbar color.
* Class Config: Removed 3.3.5 compatibility code.
* DK: Fixed up a couple entries. Trying a new spellID for Unholy Blight, the old one apparently wasn't working (haven't had a chance to check myself).
* Priest/Healer: Greater Heal is now shown on the casted-heals bar.
* Priest/Shadow: Added Shadowfiend CD.
* Rogue: Fixed up an entry or two.
* Warlock: Moved Immolation Aura to the bottom of the list. Corruption now shows for all specs.

Note: Try setting some blend modes to "ADD" if you're curious. This can be very useful for some UIs, and does allow for more visible bars depending on your settings, monitor, and perception of color.
Changelog may be incomplete for this release.

### v1.9 r335:
* TOC: Fixed. Global savedvars weren't being declared due to an old package script.
* r335-2 corrects another global savedvar issue.


### v1.9 r334:
* Core: Killed off some debug code that snuck into r333.

### v1.9 r333: Note - SavedVariables wipe, sorry for any inconvenience. Untested in beta, haven't had an opportunity.
* Core: Trinkets and other gear checks now use savedvariables to avoid constant GetItemInfo calls and at least somewhat remedy the related Beta/PTR issues.
* API: Modules are now loaded before checking talents, allowing modules to use EH's talent checks instead of their own.

Note: Beta/PTR users may notice missing trinkets when logging in for the first time. Entering combat, using a spell/skill with a cooldown, or swapping trinkets should fix that.

### v1.9 r329:
* Core: Fixed stance/form detection.
* Priest (Beta/PTR): Filler bar now tracks Shadow Orbs instead of Mind Spike stacks.

### v1.9 r327: Warlock love inc.
* Core: Bypassed a check in UPDATE_SHAPESHIFT_FORM when playing a Warlock. The Immolation Aura bar now appears as intended.
* Warlock (Beta/PTR): Removed Curse bar.
 - Demonology: Immolation Aura now appears as intended when in metamorphosis. Bar order has been adjusted.
* Warlock (Live): Adjusted Demonology bar order to closer reflect Beta bars. New filler bar, showing Molten Core procs instead of ISB.

### v1.9 r322: SVN messed up EventHorizon.lua in r321, sorry about that.

### v1.9 r321: Bunch of workarounds because Blizzard hates me.
* Core: Bars with both channeled spells and auras (Warlock, Priest, Mage) will no longer lose their channel ticks on aura changes.
* Core: Logging in, reloading your UI, or changing gear sets will no longer trigger multiple layout checks at once. Instead, a 2-second delay is used with a single mass update at the end. (note 1)
* Core: Gear checks have been revamped a bit to reduce errors, oddities, and CPU usage.
* Core: Blank trinket bars at login: Added an extra post-load check for trinket bars, using the glyph redetection workaround. (note 2)
* Core: Leveling up will now trigger a layout check.
* Core: Added a couple new slash commands: "/ehz lock" (toggles the drag-handle), and "/ehz status" (shows a list of modules and shown bars). "/ehz help" has been reformatted a bit. (note 3)
* Config: A new color and layout has been added for channeled ticks.
* Config: Changed the bar layouts a bit. Ticks are a little shorter, bars a little taller.
* Mage (Beta/PTR): Corrected Living Bomb's DoT interval.

Notes:
1) This effectively cuts the number of talent checks and layout updates in half. Yay efficiency.
2) The item cache is pretty screwy. Nothing but the itemID is available at login during the loading process. ReloadUI or logging out and back in fixes it.
+ Using the dissapearing-glyph workaround seems to work decently for now. I'll see about a better solution if people still have blank trinket bars.
3) Using "/ehz lock" when the frame would not normally have a handle does nothing, and will tell you that.
4) I'm still looking for inaccuracies and missing procs in the class config. Let me know if you feel like your bars are missing something that should be there.

### v1.9 r312: Maintenance release with Cataclysm and PTR compatibility while I break things for Axis. I had this release planned long ago, sorry for the delay.
* NOTE: This release is compatible with live realms, PTRs, and the Cataclysm beta. PTR and Beta players will notice new bar layouts.
* Class Config: Added two new flags to NewSpell:
 - requiredTree = <tree> or {tree, tree, ...} - Adds a dominant talent tree requirement to the bar. This follows the order on your talent sheet (ie, Arms Warrior = 1, Shadow Priest = 3)
 - requiredLevel = <level> - Adds a level requirement to the bar.
* Core: Internal cooldowns have been adjusted to behave a bit better.
* Core: Made some huge changes to EH's internal table structure. (/dump EventHorizon.vars if you're interested)
* Core: config.past and config.future have been sanitized and will no accept both positive and negative numbers with no ill effect.
* Config: The default cooldown color has changed to a mute blue/teal and made a touch more opaque. (0.6, 0.8, 1, 0.3)
* Config: The default cast color has also been changed slightly and made a little less opaque. (0, 1, 0.2, 0.25)

WotLK class config:
* Priest: Vampiric Touch is down to 5 expected ticks. t9 is no longer default. Change it to 7 if you use it.
* Shaman: The Ele bars did feel funky how they were. Sorry about that.
 - Elemental: Lava Burst is back on its own bar. Lightning Bolt and Chain Lightning are shared below it.

Notes: This is beta. It's largely untested and things will probably break. I'll update as often as I can.
* GetItemCooldown seems pretty well screwed, let me know if you get errors related to it and which trinkets you're using if you run into problems.
* Several Cataclysm/PTR configs are completely untested.

Release notes:
 v1.9 r274: Minor fixes.
* Trinkets work at login now. Sorry about that. Missed a call at login/reloadui and didn't notice until today.
* Purified Lunar Dust somehow lost its internal cooldown in the shuffle.
* Priest: Mind Sear is now tracked with MB/MF.

### v1.9 r272: Not QUITE Axis, but it's getting there pretty quickly.
* NEW FEATURE! Bars are now able to track multiple casts, and can track both casts and channels on the same bar. The bar icon will change according to the last spell cast. (see note)
* Axis's talent check method has been implemented. Talents are now only checked once per talent, instead of once per config appearance. (see note 2)
* Equipment checks now pay better attention to event arguments and thus no longer require throttling. Say goodbye to missing trinkets.
* Various changes to the cast and channel functions, perhaps a slight performance benefit.
* Death Knight: Simplified the layout a bit. Removed some long cooldowns and unneeded buffs, added Howling Blast + Rime for frost.
* Mage: Folded the various Bolts and Scorch into a single bar. Arcane won't see it. Moved ABar down in priority.
* Priest: Down to four bars for Shadow, yay.
 - Shadow: The Mind Flay and SWD bars have been removed. Mind Flay now shares with Mind Blast, SWD shares with SWP.
* Shaman: Hey look, I play one these days. Nice little batch of updates.
 - Flame Shock is properly tagged as hasted.
 - Elemental: Added Thunderstorm, changed EM's requiredTalent to EM (was Lightning Mastery for some reason). Folded Lava Burst and its cooldown into Lightning Bolt.
 - Enhancement: Stormstrike debuff is now tracked. Maelstrom Weapon has been folded into Lava Lash's bar. 
 - Resto: Folded Earthliving Weapon and Lesser Healing Wave into Healing Wave's bar.
* Warlock: Could use feedback on the bar placement.
 - The former Shadow Bolt bar now tracks the following casts: Shadow Bolt, Incinerate, Soul Fire, Chaos Bolt (plus cooldown), Drain Life/Mana/Soul (with tick info).

Notes:
1) The spell config remains compatible with previous versions, however a new syntax has been added for the NewSpell cast and channeled flags.
 - cast = {spellID1, spellID2, spellID3, ...}
 - channeled = { {spellID1,numhits}, {spellID2,numhits}, {spellID3,numhits} } - Note that numhits is not required and will fall back to the NewSpell numhits setting or nothing, if not present.
 - See the Warlock, Priest, or Mage config for usage.
 - The existing 'keepIcon' flag will prevent the bar icon from changing (casting times already prevent icon changes for buffs/debuffs).
2) Priests went from around 10 talent checks to 4. I'm pretty sure Shammies went from 16 to something like 5 or 6 checks. Pretty awesome stuff.

### v1.9 r249: I lied. Got a little tired of random cooldown-induced issues.
* Core: The spell config cooldown flag may now be set to a spellID, to track an alternate spell for cooldown info. See the Warlock config.
* Core: If a buff's duration is longer than its internal cooldown, the cooldown bar will be overlaid like a normal cd. (see note)
* Death Knight: Revamped the config. No more long cooldown option, talent checks are a bit more intelligent to compensate.
* Priest: Penance will keep its own icon.
* Warlock: Adjusted the config a bit to better account for tree-specific procs. The curse bar now tracks Curse of Doom's cooldown.
* Warrior: Taste for Blood now properly displays its internal cooldown (see above).

Note: Some items (Deathbringer's Will in particular) seem to prefer placing a full cooldown bar for whatever reason.

### v1.9 r241: EventHorizon is officially feature-frozen barring the discovery of major bugs. Stay tuned for the next betas.
* Core: A few API changes for external config support have been made, nothing affecting normal usage.
* Warlock: Corruption's amount of expected ticks has been corrected.

### v1.9 r233:
* Core: The frame update function now obeys config.texturedbars if the option is disabled.
* Core: Removed some debug code that snuck in the release.

### v1.9: Next up, Axis!
- NOTE: EventHorizon_Lines and EventHorizon_Redshift will be marked as disabled when you log in. This won't take effect until your next login or reloadui.
- NOTE: EH's savedvariables will be reset with this release, to ensure compatibility with older versions.
- NOTE: If you're an EventHorizon_Vitals user, please update Vitals to the latest version.
* Core: Integrated EH_Redshift and EH_Lines. No more trying not to break 4 addons at once. (notes 1 and 2)
* Core: EH will reset savedvariables when updating to incompatible versions. I'll try not to make use of that, but it helps to have the functionality.
* Core: Hopefully resolved crashes at login. Please let me know what you experience with this release if EH has been crashing your game.
* Core: Lots of optimization and streamlining. There should be an all-around performance increase with v1.9 over previous versions.
* Core: All known bar positioning issues have been fixed.
* Core: The end-of-cast line now appears for all casts by default.
* Core: Bar icons will now change according to the currently shown buff or debuff, if the bar does not track a cast time or equipment slot. Use the 'keepIcon' spell config flag to prevent this (see below).
* Core: Added a workaround for Lua errors caused by a bar trying to create itself without an associated type. Still not sure what causes it.
* Trinkets: Phylactery of the Nameless Lich and Whipsering Fanged Skull now have correct internal cooldowns.
* Trinkets: Spark of Hope is now on the ignore list.
* Config: config.lua has been redocumented. Should be a lot easier to read now.
* Config: config.castLine now accepts a number, defining the minimum cast time needed to show the end-of-cast line. Example: 'config.castLine = 1.5' will produce the old behavior. Default = true (0).
* Config: The end-of-cast line now has an entry in the color table (c.castLine) and is now the same color as the cast bar by default.
* Config: Trinkets should actually be shown by default now. Pretty sure I lied in the v1.8 notes, sorry.
* Config: Removed config.iconborder (no difference if you were using the defaults before).
* Config: config.staticheight (disabled by default) will have EH resize the bars instead of the frame. Credit to Brusalk for the idea. (notes 3, 4, and 5)
* Config: config.hideIcons will hide the bar icons. Usage: config.hideIcons = true
* Config: config.stackFont will change the font of the stack indicators. Usage: config.stackFont = "FontPath" (see note 6)
* Config: config.stackFontColor will change the color of the stack indicators. Usage = config.stackFontColor = {Red,Green,Blue,(Alpha)} (default = {1,1,1}, alpha is optional, does not need config.stackFont to work)
* Config: config.stackOnRight can move the stack indicators to the other side of the frame. Usage: config.stackOnRight = true (default = false)
* Config: Added support for individual bar coloring and textures. Three new options are available in the class config. Also, an extra flag has been added for bar icons.
- bartexture: Sets a custom texture for this bar. Applies to buffs, debuffs, and cooldowns. (example: bartexture = "Interface\\Addons\\EventHorizon\\Smooth")
- barcolor: Sets a custom color for active buffs and debuffs for this bar. Does not support class coloring. (example: barcolor = {Red,Green,Blue,Alpha}, ie {1,0,0,0.6} )
- barcolorunique: Sets a custom color for 'unique' spells for this bar. If barcolor is set and this is not, unique spells will show with barcolor's setting instead. Same format as barcolor.
- keepIcon: Will force the bar icon to stay the same if it would normally change itself when a different spell is being shown. See the Warrior config for usage.
* Warrior: Added keepIcon flag to Revenge and Shield Slam bars.

(1): Redshift and Lines are DISABLED by default. They can be turned on in config.lua, via the options config.enableRedshift and config.Lines.
(2): You can use the slash commands (/eventhorizon or /ehz) to disable Redshift and Lines per character if they are enabled in config.lua, as well.
(3): For example, 'config.staticheight = 150' will make EH 150 pixels tall. With 5 shown bars, each bar will be 30 pixels tall. Spacing is still used in this mode and will act the same as it does otherwise.
(4): Please be aware that this is an 'all or nothing' option. It's made for people with a specific area to place EH who do not want the frame to ever be resized.
(5): When using the staticheight option, icons will be cropped to always show 100% of at least one dimension. If an icon is wider than it is tall, the full width is always shown. Otherwise, the full height is shown.
(6): When config.stackFont is used, a few new options open up:
- config.stackFontSize changes the size of the font. Usage: config.stackFontSize = <number> (default = 12, no effect if stackFont is not used)
- config.stackFontOutline adds an outline or other effect to the font. Valid options are "OUTLINE", "THICKOUTLINE", or "MONOCHROME". Usage: config.stackFontOutline = "FLAG" (default = nothing)
- config.stackFontShadow adds a shadow effect to the stack indicators. Usage: config.stackFontShadow = {Red,Green,Blue,(Alpha)} (default = {0,0,0,0.5} if true, alpha is optional but recommended)
- config.stackFontShadowOffset changes the offset of the font shadow. Usage: config.stackFontShadowOffset = {x,y} (default = {1,-1} if invalid or not specified)
Note: config.stackFontColor doesn't support class coloring directly (though you can work out something if you really want it). Possibly in the future.

r232-specific notes: Fixes for staticheight, plus some much-requested spell config stuff.
* Core: Changing stance/form with staticheight enabled now resizes any active bars and indicators.
* Config: Added support for individual bar coloring and textures. Three new options are available in the class config.
- bartexture: Sets a custom texture for this bar. Applies to buffs, debuffs, and cooldowns. (example: bartexture = "Interface\\Addons\\EventHorizon\\Smooth")
- barcolor: Sets a custom color for active buffs and debuffs for this bar. Does not support class coloring. (example: barcolor = {Red,Green,Blue,Alpha}, ie {1,0,0,0.6} )
- barcolorunique: Sets a custom color for 'unique' spells for this bar. If barcolor is set and this is not, unique spells will show with barcolor's setting instead. Same format as barcolor.

### v1.8: Big trinket update. Huge. Long. I have a headache.
* Config: Added a new option, config.showTrinketBars (default = true) - Set this to anything but true or remove it entirely to disable.
* Core: Trinket bars will be automatically added to the frame. Disable config.showTrinketBars if you don't like this. (See notes 1-5)
* Core: Massively improved the trinket detection. (See notes A-D)
* Spent about five hours (I wish I were exaggerating) adding trinkets to the database in trinkets.lua. Pretty much everything with an effect that can be tracked is in there now. Some things with hard-to-find spellIDs or complex effects aren't in. You're welcome, and I hope to never touch that file again.
* Druid/Balance: Added Starfall. Thanks for the reminder, Everdreamer.

* Addenum: EventHorizon now handles the initialization for EventHorizon_Vitals, if loaded. EH_V does next to nothing (as of v2.0 beta) before EH completely finishes loading.

(1): For those that haven't used EventHorizon's trinket support, this adds duration and cooldown info for just about any trinket automatically. This includes internal cooldowns, and does NOT include effects which are not buffs on yourself.
(2): If your trinket is not in trinkets.lua and it has a USE effect, its cooldown will still be tracked. The purpose of trinkets.lua is to assign spellIDs and internal cooldown information for the buffs that trinkets provide. Let me know if you have a trinket that you would like added to the list.
(3): I know this question will come up - TRINKETS.LUA IS NOT AND WILL NEVER BE LOCALIZED. If you are in a locale using a language other than English, EH will ONLY be able to track the cooldowns of trinkets with USE: effects.
(4): Deathbringer's Will should work for everyone now. Thanks for the spellIDs, Kogasu.
(5): I did add DMC:Greatness and Death's Choice/Verdict, let me know if you have any issues with either. It's easy enough to fix if need be.

(A): Empty trinket slots are removed from the display, no more empty bars.
(B): A blacklist contained within trinkets.lua (bottom of the file), EventHorizon.trinkets.blacklist, will tell EH to act as if certain trinkets are not equipped. Only the Argent Dawn trinkets are in for now. Give me names and more will be added, I'm not screwing with it anymore.
(C): Swapping trinkets or other cooldown slots will no longer result in multiple cooldown bars. This was a little tougher to fix than it sounds, let me know of any issues. (I tried to test as thoroughly as possible).
(D): The PLAYER_EQUIPMENT_CHANGED function that is used by trinket/equipment bars has been throttled to reduce framerate spiked caused by changing equipment sets, and perhaps at login.

### v1.7c:
* Core: Overhauled the pre-init code. It's a little more intelligent now, resulting in less of a hitch at login/reload and hopefully resolving an issue with random freezes/crashes at login/reload.
* Config: Added Deathbringer's Will to the trinket module. I have no way to see whether or not it actually works, though.
* Shaman: Adjusted a couple talent requirements. Flame Shock and Fire Nova will now be visible to Shamans without Concussion. The spells now check for the absence of Restorative Totems.
 - Enhance: Flame Shock is now tracked instead of Earth Shock.

### v1.7b:
* Core: Fixed a non-fatal Lua error.

### v1.7a:
* Core: Fixed a minor error caused by a variable that got renamed last release.

### v1.7: Two major releases in how many days? I MUST HAVE GONE MAD. Don't worry, I didn't break too much (I hope).
* WARNING: Healers might be a bit confused on this release. The default behavior of the healing bars has received some love. Read on for the gory details.
* Core: EventHorizon's layout has changed for the better! The clunky old layout code has been completely rewritten in favor of something much more appealing to the eye.
* Core: Improved spell config flag: auraunit = 'mouseover' - Now works like a [@mouseover,exists][@target] macro (by default) rather than just horribly breaking things.
* Core: New spell config flag: baseunit = 'focus'/'targettarget'/'whateverYouWant' - Adjusts the [@target] portion above to whatever feels more appropriate for you.
* Random: TOC now has a ## Title field, sorry bout that Minion users.
* HEALING CLASSES: Added 'local usemouseover = true' to the top of EventHorizon_CLASSNAME\config.lua. Set this to nil, false, or delete the line entirely to make everything normal again.
 - Druid/Resto: All bars involving a targeted buff now watch mouseover units as well.
 - Paladin/Holy: All bars involving a targeted buff now watch mouseover units as well.
 - Priest/Healing: All bars involving a targeted buff now watch mouseover units as well.
 - Shaman/Resto: All bars involving a targeted buff now watch mouseover units as well.

### v1.6: Obligatory disclaimer - MANY Saronite Bombs and Target Dummies were harmed in the making of this release. Seriously though, while this has had some fairly in-depth testing, treat this release as beta quality.
* NOTE: YOU MAY NEED TO ADJUST YOUR MYCONFIG.LUA. A few things have been moved to different tables, and there has been an added line in the colors section. Nothing should error unless you're overwriting the color table at once instead of per value. Adjust accordingly.
* Core: Added support for equipped items (trinkets, anyone?) and Engineering tinkers via 'slotID = <slotnumber>' in the class config. Items are refreshed every time you swap gear (no hitching noticed when using the equipment manager, though performance could likely be improved). Please see trinkets.lua before adding anything to your class config.
* Core: Added support for inventory items via 'itemID = <ID>' in the class config. Again, please see trinkets.lua.
* Config: EH's background and border may now be class colored. To make this easier to implement, config.bgcolor and config.bordercolor have been moved to the EventHorizon.colors. Move your myconfig vars around accordingly.
* Config: The 'Now' line has been made less opaque by default, and its color may now be adjusted (including class coloring) via colors.nowLine. See config.lua.
* Config: Indicators without a texture (sent/tick/nowLine, etc) no longer have their opacity multiplied by config.texturealphamultiplier. If you were having issues with this you know what I'm talking about. Otherwise, don't worry about it.
* Class changes: Lots. If you see something different about your class setup, I likely forgot about it when writing this log.
* Hunter: Shuffled the bars around a bit to better reflect shot priorities. Removed Mend Pet from all specs. BM may have a screwy shot list as a result of all this.
* Priest: Lots of changes for playability.
 - Shadow: Shuffled the bars a little. They feel a tiny bit more natural now, though they could likely use further changes.
 - Holy/Disc: The bars should work a little better for healers using Clique or similar addons/macros for healing, showing more information when you're not actually targeting what you're healing, and more relevant info when you are. Be sure to spam yourself a bit to get the hang of things before using this release in a raid environment. More adjustments will be made over time. (If you play another healing class and would like this same treatment, by all means let me know what I can do for you.)
* Paladin: Added Art of War to Exorcism. Changed one of the Judgement bars yet again. Let me know if I broke anything (again).
* Warrior/Prot: Removed Concussion Blow.
* Misc: ...lots. I probably missed quite a few changes on this log. Have fun finding them!

### v1.5c: No core changes. If you're completely happy with your class layouts, feel free to skip this release.
* Warrior: Arms rehaul, etc.
 - Arms: Reordered the bars. They feel less clunky now, IMHO.
 - Prot: Revenge bar now tracks Sword and Board instead of Improved Revenge's stun.
* Druid: Minor tweaks.
 - Feral: Reordered bear bars a bit. I haven't had an opportunity to test these changes, so please send feedback. Frenzied Regeneration isn't tracked on purpose, a dedicated cooldown monitor does a much better job for it.
 - Balance: The Typhoon bar now tracks pretty much every worthwhile idol proc.
* Mage: Fixed up +crit debuff tracking and made it consistent across specs.
* Rogue: The inactive/optional Expose Armor bar has been updated to track Sunder Armor as well.

### v1.5b:
* Core: Cooldown bars have had their opacity lowered a bit.
* Warrior: Fixed an old typo that was messing up the bars a little for Arms and Fury.
* Priest: Vampiric Touch now uses on-the-fly tick recalculation until I can figure out a way to get its expected ticks working properly with 2t9.

### v1.5a:
* Core: Reworked the stance code a bit and added a new spell config flag. See the Warrior module for the new stuff.
 - Multiple allowed stances for a spell may be set via the flag "stance = {x, y, ...}". Any number of stances may be specified.
 - Disallowed stances may be set via the flag "notstance", using the same format as "stance".
 - Cleaned up the stance code a little.
* Core: Cooldowns are now lower on the strata priority. Should make buffs and debuffs a little more visible.
* Druid: Feral abilities now have Ferocity as a required talent. Trees and boomkins, no more pointless bars when running around as a kitty.
 - Balance: Added a couple idol procs to Typhoon's bar.
* Paladin: Reordered bars a bit to better reflect the 969 tanking rotation and Ret changes. Let me know if I can further improve it.
* Warrior: Shockwave and Concussive Blow are now tracked. Added some extra talent requirements to trim unnecessary bars.

### v1.5:
* Core: Glyph detection has been rewritten a bit and uses less CPU while being less of a pain to work with on my end.
* Core: Glyph-based periodic haste (Corruption/Rejuvenation) should work better now. It's still not 100%, though, due to oddities on Blizzard's end.
* Core: Converted textureID to uniqueID in core and class config. uniqueID tracks a single specific spellID for things like Eclipse and Sacred Shield.
* Core: Some general fixes and API updates that I've likely forgotten by now.
* Druid: Converted Eclipse tracking from textureID to uniqueID. Removed Faerie Fire and reordered Balance bars a bit.
* Paladin: Converted Sacred Shield tracking from textureID to uniqueID.
* Shaman: Thunderstorm removed. Fire Nova and Elemental Mastery added.
* Mage: Updated Frost and Arcane. Arcane now tracks AP and PoM. Frost now tracks most freeze effects, Deep Freeze, and Fingers of Frost (TLDR: EH is now much more usable for Frost).

### v1.4: Patch 3.3 compatibility
* Core: Hasted periodic spells now calculate their interval once per cast rather than per tick. This may cause issues with target swapping and variable haste, please let me know if any issues pop up. (See the changed modules for how this works - To use the old per-tick behavior, remove or comment out the expectedTicks flag)
 - Note that the new code may cause issues when target switching with variable haste. Let me know if anything pops up.
 - Due to the new handling, a check has been added for Mage Armor on the hasted spell's target.
 - For hasted effects using the old handling, some extra logic has been added to make sure target swaps don't really screw things up. Future releases may remove the old handling completely. This is untested but should work fine.
* Core: Removed PTR check code. This release should still work in patch 3.2 if anyone is somehow still playing it, but v1.3c is preferred in that case.
* Warlock: Updated for the new haste handling.
* Priest: Updated for the new haste handling.
* Druid: Updated for the new haste handling.
* TOC: Updated for WoW 3.3.

### v1.3c:
* Core: Fixed a minor Lua error resulting from delaying (and possibly cancelling) a tracked spellcast under 1.5 seconds. Once again, copypasta kills.

### v1.3b:
* Core: Fixed errors related to the casting line. Not sure how they got there, to be honest.
* Warlock: Corruption is once more spec-specific, recovering from its status as a debug spell.

### v1.3a:
* Core: Fixed a minor non-fatal typo in UnitBuffUnique (the function used to check status of multiple buffs at once) that caused buffs tagged as unique (Inspiration/AF, Grace) to not track other players' versions. Thanks, hungtar.

### v1.3: Patch 3.3 update with some extra goodies.
* Core: Hasted periodic (DoT/HoT) spells are now fully supported. A new spell config var has been added: haste = glyphID or {talentTab,talentIndex}. This piggybacks on tick recalculation and is heavily affected by lag, but is as accurate as WoW's API allows. Ticks may seem a little jumpy depending on your latency. Hasted tick recalculation is only enabled when playing Patch 3.3.
* Core: When a bar has multiple spells assigned to it, spells cast by others should no longer interfere with the showing of your own buffs/debuffs. Warlock curses were affected most by this.
* Core: A vertical line, extending the full height of EH's frame, has been added to signify the end of any cast longer than 1.5 seconds. This uses the 'sent' coloring for those wishing to change it, and config.castLine for those wishing to remove it.
* Core: Bars watching multiple buffs/debuffs now have the ability to track periodic ticks on the bar's initial spell (spellID field) without bugging out. This allows the Warlock curse bar to provide tick info for CoA without messing up other curses, and has potential for a few other classes as well.
* Config: config.castLine has been added. Any value other than 'true' will disable full-frame casting lines if you dislike them.
* Config: config.recalculate is now mandatory and the option to disable it has been removed (as with its config entry).
* Warlock: Corruption is now considered a hasted DoT when using a Glyph of Rapid Decay.
 - The Warlock curse bar should now work properly in the presence of other Warlocks.
 - Curse of Agony is now able to show its ticks.
* Priest: Vampiric Touch and Devouring Plague are now considered as hasted DoTs as long as Shadowform is talented.
* Druid: Rejuvenation is now considered a hasted HoT when using a Glyph of Rapid Rejuvenation.
* Warrior: You may now use myconfig.lua with the Warrior module without needing to modify EventHorizon_Warrior.toc. No other class needed changing.

### v1.2.4c: All Warlocks should now see the curse bar. In addition, the curse bar's icon has been changed to CoA.

### v1.2.4b: Made a few changes to the frame reloading code to keep CPU usage down and prevent the frame from randomly reappearing if EH is hidden.

### v1.2.4a: Corrected an event call that was being overwritten, preventing EventHorizon from initializing until reloadui. Sorry about that.

### v1.2.4:
* Core: DoT/HoT recalculation was throwing errors if a spell ticked between the time a unit hit zero health and actually died (the timing differs between players and most mobs). A workaround has been added.
* Core: The frame is now reloaded when entering/exiting combat, changing zones and areas within zones, and at a few other points. This should hopefully resolve disappearing spells. A better fix is in the works.
* Paladin: Reworked the module a bit. Judgements will now show for all specs (including untalented). Judgement of Justice is tracked by default.
 - Holy: If Judgements of the Pure is talented, the Judgement bar will change to JoW + JotP.
 - Prot/Ret: Changed talentIDs a bit to handle lower levels and cross-speccing a bit better.
* Shaman: Changed the talentID for Earth Shock to Dual Wield.

### v1.2.3:
* Shaman: Updates and fixes to the module. Talents got messed up a bit when I was working with the Resto config.
 - All specs: Flame Shock now requires Concussion. Earth Shock now requires Shamanistic Focus. This is for Resto's sake, and there are other ways to handle it if anyone has issues due to the change.
 - Elemental: Thunderstorm is now only shown when it's actually talented.
 - Enhance: Maelstrom Weapon is now tracked on its own bar.
 - Resto: Talent requirements have been fixed. Sorry about that. Also, corrected the spellID for Ancestral Fortitude.
* Priest/Heal: Corrected the spellID for Shaman's Ancestral Fortitude (unique tracking alongside Inspiration).

### v1.2.2: Minor fixes and updates while we get ready for partial recoding in v1.3.
* Core: Zoning should no longer break spells that use the requiredGlyph setting. The fix had a 100% success rate in tests on two computers with a friend involved, but your mileage may vary.
* Shaman: Config has been revamped for personal sanity reasons.
 - Elemental: Swapped Lightning Bolt and Chain Lightning. Thunderstorm is now tracked.
* Warlock: Haunt once again has a cast time.
* Warrior:
 - Protection: Shield Slam will now only appear when Shield Mastery is talented, appears in all stances, and now tracks Glyph of Blocking.
 - Arms: Unrelenting Assault's talent index has been fixed.

### v1.2.1:
* Core: Fixed a typo that was causing glyph checks to fail. Please let me know if the issues continue.
 - v1.2.1a: Added all Warlock curses to the display under a single bar. Be aware that Curse of Agony has no DoT tick display.

### v1.2: The long-promised Special-Cases update!
 - NOTE: This release marks the official re-release of EventHorizon's continued branch as its own addon. Please update your bookmarks and favorites accordingly. I'll get in touch with Tifi to have him update the original EH page with the new link once it's up.
* Core: Added "textureID" to spell config, allowing a user-specified texture to be used as a filter for any aura. See the Druid config for usage.
* Core: Buffs/debuffs with casting time have had their logic altered. The small recast line (Vampiric Touch, Immolate, etc) is now only displayed if the aura being tracked is the same as the spell being cast. This fixes undesired behavior with many spells, while leaving the spells it was intended for intact.
* Core: Auras using the "playerbuff" spell flag now accept tables as valid entries. This allows multiple buffs to be tracked on the same bar, same as debuffs.
* Core: All auras may now use the "unique" flag, rather than just debuffs.
* Config: Bar backgrounds are now hidden by default.
* Shaman: Updated module, Resto spec now included. Tracked in order: Earthliving Weapon, Riptide, Lesser Healing Wave (includes Ancestral Healing/Inspiration), Healing Wave, Chain Heal (includes Tidal Waves), Earth Shield.
* Paladin: Updated module, Holy spec now included. Tracked in order: Beacon of Light (on Focus), Sacred Shield (on target), Holy Shock, Holy Light (including Light's Grace), Flash of Light (including Sacred Shield HoT effect).
* Rogue: All ranks of Deadly Poison are now tracked. Leveling Rogues no longer have a bar that does absolutely nothing. Note: Due to limitations in combat log filtering, DP ranks lower than max level will have limited functionality. They will not recalculate, nor will ticks appear in the 'past' section of the bar. There is no way to fix this at the moment without massively increasing EventHorizon's cpu usage.
* Priest: Updated module, spell flags should all be correct now. Inspiration tracking now includes unique buff tracking for Ancestral Healing and other priests' Inspiration.
* Druid: Eclipse tracking is now done via Wrath and Starfire, with procs tracked independently.

### v1.1.6:
* Core: Fixed timeless spells refreshing to timed breaking bars (Overkill is the only spell that comes to mind here, but should work for everything)
* Rogue: Added Overkill to the display if specced for it.
 - v1.1.6a: Minor update. Auras flagged as "refreshable" with an auraunit other than target will no longer glitch on target changes.

### v1.1.5: More glyph support.
* Core: Added requiredGlyph = <glyphID> to the spell config. See the Warlock module for reference. Note that if looking for the glyph on WowHead, you need to search for the glyph name and go to the uncategorized spells tab. The actual glyphID is the one with the gear icon, NOT the spell icon.
* Warlock: Warlock module has been updated. Thanks, Warlocomotif.
* Etc: TOC updates across the board. Sorry for being lazy with those, modules should no longer read as out of date.
 - v1.1.5a corrects the glyph detection logic. There is a much more efficient way of doing this, which will make it in next release.

### v1.1.4:
* Core: Fixed a very old (possibly ancient) bug involving spellcast delays.

### v1.1.3: Glyph support!
 - This release is somewhere between beta and release quality. I've ironed out as many bugs as I could find, but some may remain. Please let me know if you run into any issues.
* Class modules: A new variable has been added - glyphrefresh = {Stacks, GlyphID, "Trigger Spell"}
* Core: Glyphs are now detected on frame load/reload. Some extra glyph-related events have been added to make sure glyph changes aren't missed. Module hackers: Print EventHorizon.glyphs ingame if you need a list of currently equipped GlyphIDs.
* Core: When casting a spell that uses the glyphrefresh var, and currently using the appropriate glyph, the number of remaining glyph-based refreshes is displayed as a stack count on the spell's icon. This is much more complicated than it sounds and may result in unexpected bugs, but should be safe for all intents and purposes.
* Core: Gnomish fanatics have found their way to the CLEU filtering mechanisms. Let's hope they didn't break too much on their way out.
* Druid: Glyphs of Starfire and Shred have been added to Moonfire and Rip respectively.
* Rogue: Rupture somehow lost its refreshable tag, which has been corrected. Glyph of Backstab has been added to Rupture.

### v1.1.2:
* Core: DoT tick recalculation was trying to calculate channeled spells, producing an error.

### v1.1.1:
* Config: Reverted the cooldown layout change for now.
* Priest: Missing stance flags added. Sorry about that, Shadow Priests.
* Mage/Arcane: Updated Arcane Blast for 3.2.2.

### v1.1: Look, Feel, and Quirks update of d00m.
Major changes:
* Core: Class coloring has been implemented. Usage and examples are in config.lua.
* Core: Tick indicators may now recalculate based on the last tick to fire. This fixes all known cases of incorrect tick displays. This [b]IS[/b] affected by your latency, and will take a tick once a spell is refreshed to update. A 200ms grace period is allowed after a spell ends for the last tick to show. If you have any issues with this, by all means let me know.
* Config: The following indicators/bars will now be class colored by default: 'sent', 'tick', 'debuffmine', 'debuff' (darkened). The background has been made slightly more opaque for visibility. Priests will find that their class color is automatically darkened a little 

Minor changes:
* Core: The 'auraunit' class config setting should play nicely with target changes now.
* Core: Cooldown lines have had their placement adjusted slightly due to visibility issues. This change may not be final, expect tweaks over the next few releases.
* Config: Changed config.future from 9 to 12.
* Config: Class locals have been added to config.lua. This is mainly for copypaste over to myconfig.lua to make adjustments per class a little easier to type out.
* Config: The coloring section is now commented much more thoroughly.
* Config: Removed color.default from the color section, as it should never need to be changed anyway.
* Config: config.recalculate has been added, allowing the option to enable/disable the new tick checks. Enabled by default.
* Druid: HoT ticks have been added (copypaste is bad, mkay?).
* Priest: Renew now tracks target, not player (again with the copypaste).
* Etc: Changelog updated and hopefully easier to read.

### v1.0 (v0.2 again?): Healer support!
- Major version bump. Postrelease note: This should've been a beta.
- Didn't get to the coloring portion this time around, expect it in the next update. Buffs and casts for healer specs may be a little hard to tell apart for now.
* Core: Heal-over-time spells are now fully supported. Consult the Priest and Druid modules for usage.
* Core: Many changes to the UNIT_AURA code. Hopefully there will be no more cases of bars acting oddly.
* Core: Tidied up CLEU filtering a bit. There may be a performance improvement with this build (one table check versus a LOT of comparitive statements).
* Core: Fixed many issues involving buffs tied to spells with casting times.
* Core: Added an alias for the spell config flag 'cleu'. You may now use 'event' instead. Consult the Priest module for usage. Warning: Only use the flag when you can't get ticks to show in the past section of the bar in any other way. Doing otherwise will provoke a nil error which I haven't been able to track down.
* Priest: Holy and Disc are now fully supported. Lesser Heal tracks Serendipity, Greater Heal tracks Inspiration (self-casted only for the moment), Penance tracks Grace. Can't track PW:S alongside Weakened Soul quite yet. Bars will show when not in shadowform.
* Druid: Resto is now fully supported. Nourish also tracks Nature's Grace, for the curious. Requires Swiftmend talented to see the bars.

### v1.0 (v0.12) Beta 5:
* Core: Buffs may now use the 'dot' flag to signify a heal-over-time spell. SPELL_PERIODIC_HEAL is automatically tracked. Heal-over-time spells will now be able to track ticks with no additional config required. Refer to the Hunter module for an example.
* Hunter: Added Mend Pet with a working tick display. Should be fully accurate.

### v1.0 (v0.12) Beta 4:
* Core: Drycode fix, can't use SetFrameLevel on the nowIndicator. Addon is usable again, sorry about that.

### v1.0 (v0.12) Beta 3:
* Core: Talents are now updated when using /ehz to unhide the addon.
* Etc: Added class modules to the beta release. The original EH files are no longer required.
* Warrior: Added EventHorizon_Warrior to the release.
* Deathknight: Added Tyno's excellent EventHorizon_Deathknight to the release, with some minor changes.

### v1.0 (v0.12) Beta 2:
* Config: Color settings are now included in config.lua. The provided defaults are not final. (Taroven)
* Core: Handle is now clamped to the screen, preventing loss of the frame outside of the screen edges. (Tifi)

### v1.0 (v0.12) Beta 1:
* Class modules: Added NewSpell config "auraunit = 'unitID'" to playerbuff settings. (Taroven)
* Core: Moved "interesting event" application to a new function. Users will see no difference, module developers may find some use. Documentation will come when modules have finer access to EventHorizon's bars. (Taroven)
* Bar config: Buffs are now correctly colored. (Taroven)

### v0.11:
* Class modules: The file myconfig.lua is now loaded if present, e.g. EventHorizon_Druid/myconfig.lua
* Shaman: Added spells Lava Lash, Stormstrike, and Earth Shock when specced Enhancement.
* Bugfix: Disabling the GCD indicator with config.gcdStyle=nil won't cause any more errors.

### v0.10b:
* Druid: Cleaned up comments. Added simple Eclipse tracking (duration and cooldown, no proc info). Rip set to refreshable to fix tick timing with Glyph of Shred.
* Hunter: Arcane Shot not tracked when Explosive Shot is talented. Moved Steady Shot to above Kill Shot. Cleaned up some oddities with the comments. 
* Rogue: Moved ShS nearer to the bottom.
* Warlock: Added Glyph of Life Tap for all specs. Added Drain Soul when specced Death's Embrace.

### v0.10a:
* Mage: Added Winter's Chill tracking to the Frostbolt bar. Also added Blizzard, but it's commented out by default.
* Paladin: Added Protection spells, required talent Hammer of the Righteous.
* Paladin: Changed required talent for shared Prot/Ret spells to Divine Strength.
* Paladin: Reordered all spells to reflect current prioritization.
* Warlock: Show Immolate only if Unstable Affliction isn't talented.

### v0.10:
* Warlock fixed: The spell ID of Conflagrate changed.
* Hunter: Added Black Arrow.
* Removed stuff for 3.09.

### v0.9c
* Fixed: Using the slash command will now completely disable the addon. The state is saved in the SavedVar.
* Fixed: Indicators are now hidden when their bar is hidden.

### v0.9b
* Fixed: Ticks from channeled spells were not properly unregistered. This could sometimes lead to disappearing ticks in other spells bars.

### v0.9a
* Fixed: Overlapping segments won't flicker anymore.
* Added config.auraunit field for spell configs to specify a non-default unit (e.g. 'player' for debuffs).
* Paladin: Set Divine Storm as required talent for all spells to make the module Retribution-only.
* Mage: Added Arcane and (some) Frost spells. Added talent requirements for Fire spells. Added Fireball.
* Getting ready for 3.1: Druids' Berserk and Paladins' Divine Storm talent index changes, Warlocks' Siphon Life gets removed. These also should work now on the PTR.

### v0.9
* The spell bars that depend on talents are now created/shown/hidden when the talents change. Reloading the UI is no longer necessary. Should be working in both 3.0 and 3.1.
* Added Paladin module from Psychosomatic. Retribution only, still needs talent dependencies.
* Priest: Added talent dependencies.

### v0.8
* Bar segments are optionally textured now instead of using a solid color.
* Added slash commands /eventhorizon and /ehz to toggle the visibility of the main frame.
* Added the ability to track debuffs which are unique per mob. The debuff bars get a slightly different color when they were not applied by you.
* Druid: The Mangle bars now track Mangle and Trauma debuffs. Added cooldown for Mangle - Bear. Added DoT ticks for Insect Swarm and Moonfire.
* Mage: The Scorch bar now tracks both Imp Scorch and Winter's Chill.
* Tweaked the default texture a bit.

### v0.7b
* Removed some settings in the class files that were overwriting settings in the master config.

### v0.7a
* Warlock: Show Incinerate if Emberstorm is talented, otherwise show Shadow Bolt. Removed Molten Core bar and Backdraft tracking from the default config, as they have no influence on the rotation.
* Bugfix: The default anchoring of the handle wasn't working.

### v0.7
* Added config.spacing = <number> to set the space between two bars.
* Added config.iconborder = <boolean> option to toggle the default Blizzard icon border.
* Added config.scale = <number> option to scale the main frame.
* Added GCD indicator: 
 config.gcdStyle = 'line' displays the end of the GCD as a thin line.
 config.gcdStyle = 'bar' displays the GCD as a bar from now to the end.
 config.gcdStyle = nil disables the GCD indicator.
 config.gcdColor = {r,g,b,a} sets the color.
* The handle and the background frame are now parented to the main frame. If you use Goose to show/hide EventHorizon, you only need to specify conditions for EventHorizonFrame.

### v0.6a
* Added minstacks=<number> syntax. The Imp. Scorch debuff bar is shown only when five stacks are applied.
* Fixed Rogue Hunger for Blood talent index.
* Major bug fixed: In some cases the main frame was created multiple times.

### v0.5
* Added modules for Druids, Hunters, [FFB-]Mages, Rogues and Warlocks.
* Most of the settings were moved to the config.lua files. When you want to change something, look there first.
* Spell frames can now be shown/hidden depending on stance. Look at the Druid config for an example.
* Spell frames can now be created depending on talents. When changing the spec, you may need to reload the interface. Again, look at the Druid config.
* Added an (optional) backdrop frame. Enabled by default.

### v0.4
* Bugfix: When the target dies, predicted ticks are now removed.
* Bugfix: Textures of 1 pixel width should now be visible even when the UI scale is low.

### v0.3
* Minor bug fix.

### v0.2
* Predicted DoT/MF ticks lying in the past are now replaced by actual ticks taken from the combat log.
* If SWP is refreshed after the last tick occured, it's treated like it was recast.

### v0.1a
* Forgot to add the background texture. -.-

### v0.1
* Initial beta release.


\* *This Change Log was automatically generated by [github_changelog_generator](https://github.com/skywinder/Github-Changelog-Generator)*