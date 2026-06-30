# The GreenZone Changelog

## 0.1.151
- Shows the Crafters window as `The Studium v0.1.151 - Crafters`.
- Changes unavailable FC chest material rows to say `Open FC Chest`.
- Marks fully withdrawn material rows as `Transferred` after FC chest withdrawal.

## 0.1.150
- Adds `/tscrafters` as the direct command for the Studium Crafters module.
- Keeps `/thestudium` focused on the main Studium window, settings, overlay, and clear actions.
- Updates local dev workflow notes to use `/tscrafters`.

## 0.1.149
- Closes the FC chest window after a successful Crafters withdrawal queue completes.
- Keeps Artisan handoff unblocked after materials are withdrawn.
- Keeps the all-or-nothing FC chest material validation from the previous release.

## 0.1.148
- Splits the crafting-list dropdown into DoH, DoL, tank, DPS, and healer categories.
- Updates FC chest withdrawal planning to require all materials to be stocked before withdrawing anything.
- Withdraws full required material amounts, including crystals and clusters up to the player inventory cap.

## 0.1.147
- Adds a visual queue so multiple crafting lists can be planned together.
- Gives each queued list its own Gear, Accessories, and Tools / Weapon controls.
- Aggregates duplicate finished items before material calculation, FC chest withdrawal, and Artisan handoff.

## 0.1.146
- Groups crafting-list choices into DoW/M and Crafting / Gathering sections.
- Makes the expanded hosted gear catalog easier to scan in the plugin.
- Keeps material calculation, FC chest withdrawal, and Artisan handoff behavior unchanged.

## 0.1.145
- Loads predefined crafting sets from the hosted crafter dashboard catalog.
- Adds Miner, Botanist, Fisher, and all crafting job gear sets.
- Adds Gear, Accessories, and Tools filters before material calculation and Artisan handoff.

## 0.1.144
- Adds `/thestudium crafters` with a predefined current mining gear set.
- Calculates direct recipe materials and shows inventory and FC chest availability.
- Adds experimental FC chest withdrawal and Artisan handoff once materials are ready.

## 0.1.143
- Renames the plugin listing and windows to The Studium.
- Adds `/thestudium` as the primary slash command.
- Keeps `/greenzone` as a legacy command alias for compatibility.

## 0.1.142
- Moves the weekly GC seals reset and progress timer to Monday 9am AEST.
- Reorders the daily GC seals activity buckets to run Monday through Sunday.
- Updates Lodestone weekly standings timing to the Monday 6pm AEST publish window.

## 0.1.141
- Ignores initial FC chest tab-load inventory events until the tab has a confirmed baseline.
- Keeps same-character withdrawal debt for remove/re-add protection.
- Requires the corrected contribution detection version for dashboard leaderboard credit.

## 0.1.140
- Uploads verified FC chest add and remove events with retry-safe event IDs.
- Adds same-character withdrawal debt so remove/re-add loops do not create extra credit.
- Allows legitimate restocking after another member uses materials to receive full contribution credit.

## 0.1.139
- Uses verified local inventory change events only for FC chest contributor credit.
- Removes inferred tab-delta contribution credit that could assign another member's additions to the viewer.
- Requires the new contribution detection version for leaderboard credit while preserving normal FC chest stock sync.

## 0.1.138
- Credits GC seals from the game's lower-level LogMessageId 1300 instead of typed chat text.
- Counts only messages sourced from the current local character and home world.
- Blocks `/echo` and player chat from granting seals while keeping real Grand Company hand-ins credited.

## 0.1.137
- Restores the known-good 0.1.134 seal counting behavior so Grand Company hand-ins credit again.
- Removes the broken 0.1.135/0.1.136 chat-channel guards while the integrity fix is reworked.
- Keeps FC chest contributor reliability changes from 0.1.134.

## 0.1.136
- Restores real Grand Company hand-in seal credit from game-generated progress messages.
- Keeps player/local chat channels such as `/echo`, FC chat, party chat, tells, and linkshells blocked.
- Keeps impossible single-message seal values rejected as an additional safeguard.

## 0.1.135
- Counts weekly GC seal gains only from trusted game-generated chat log types.
- Ignores player-typed chat and `/echo` messages that mimic seal gain text.
- Rejects impossible single-message seal values as an additional safeguard.

## 0.1.134
- Detects contributor credit from per-session FC chest stock increases.
- Catches meal and other additions even when the game reports an unusual inventory event shape.
- Keeps existing FC chest stock sync behaviour unchanged.

## 0.1.133
- Credits verified items added into a new empty FC chest slot.
- Fixes food and other separate-stack deposits syncing stock without contributor credit.
- Keeps existing FC chest stock sync behaviour unchanged.

## 0.1.132
- Adds contributor scoring support for FC chest crystal, shard, and cluster deposits.
- Keeps verified local item-move scoring for contributor credit.
- Supports new dashboard categories for tome mats, crystals, and meals.

## 0.1.131
- Scores contributor credit only from verified local item moves into the FC chest.
- Stops using passive FC chest stock increases as individual contribution proof.
- Keeps normal FC chest stock sync behaviour unchanged.

## 0.1.130
- Nets FC chest contribution credit within the current chest session so remove/re-add loops do not create duplicate pending credit.
- Keeps contribution tracking in memory only while the chest is open.
- Keeps normal FC chest stock sync behaviour unchanged.

## 0.1.129
- Tightens FC chest contribution detection so existing stock loaded late is not credited as a new contribution.
- Marks new contribution uploads with a safer detection version for the dashboard contributor ledger.
- Keeps normal FC chest stock sync behaviour unchanged.

## 0.1.128
- Repairs malformed saved config data during startup instead of letting it stop GreenZone from loading.
- Cleans bad saved profile, FC point, ranking, FC chest sync, and community status entries defensively.

## 0.1.127
- Prevents a bad saved FC point sample from stopping GreenZone from loading.
- Keeps the FC chest sync reliability and settings status improvements from 0.1.126.

## 0.1.126
- Detects loaded FC chest tab content changes even if the normal inventory-change event is missed.
- Adds a read-only FC chest sync status section to settings for easier troubleshooting.
- Keeps existing seals and tier tracking behavior unchanged.

## 0.1.125
- Uploads Materia rank alongside Ravana rank for personal best seals records.
- Keeps existing seals and tier tracking behavior unchanged.

## 0.1.124
- Retries pending FC chest contribution entries until a sync upload succeeds.
- Tracks positive FC chest additions for top contributor leaderboards.

## 0.1.123
- Tracks positive FC chest additions during a GreenZone chest session for top contributor leaderboards.
- Adds item category metadata so Minion contributions can be identified correctly.

## 0.1.122
- Sends Studium Community presence updates to `community.thestudium.com.au`.

## 0.1.121
- Adds a default-on Studium Community setting.
- Lists opted-in The Studium characters on the community page with character name, GreenZone version, and personal best weekly GC seals.
- Sends a remove request when the setting is turned off.

## 0.1.120
- Uploads The Studium FC chest gil balance with FC chest sync snapshots.
- Updates settings wording to distinguish FC chest gil from personal gil.

## 0.1.119
- Detects FC chest pages from loaded inventory data as well as selected tab UI.
- Allows opened Tabs 2-5 to sync even when the game UI does not report tab selection reliably.

## 0.1.118
- Confirms selected FC chest tabs only after their actual item data is loaded.
- Allows Tabs 2-5 to upload after clicking through them instead of stopping at Tab 1.

## 0.1.117
- Syncs Tab 1 after the FC chest opens when Tab 1 actual inventory data is loaded.
- Keeps the unsafe blind Tab 1 guess disabled so weak reads do not publish false tab data.

## 0.1.116
- Uploads full FC chest section snapshots for opened tabs and crystals, including item IDs, names, quantities and slots.
- Stops guessing Tab 1 when the selected FC chest tab cannot be read confidently.
- Updates FC chest sync wording for the broader full-chest dashboard model.

## 0.1.115
- Only uploads FC chest data while the current character is in The Studium FC tag.
- Sends the FC tag with chest sync uploads so the dashboard endpoint can reject non-Studium chest data.
- Updates the settings wording to explain that FC tag is included in sync uploads.

## 0.1.114
- Detects FC chest tab changes from explicit inventory event page data.
- Trusts tabs with confirmed item changes so Tab 2 can repair stuck dashboard values.
- Narrows selected-tab UI detection to the real 1-5 chest tab row.

## 0.1.113
- Detects the selected FC chest tab from the visible chest window.
- Fixes later visits showing only Tab 1 when the game reuses cached chest page data.
- Rejects unsafe empty or partial material-tab reads before they can zero dashboard quantities.

## 0.1.112
- Keeps syncing while the FC chest remains open.
- Uploads again after later tab loads or item changes.
- Fixes Tab 2 items such as Double Duracoat staying on an old quantity after the first Tab 1 sync.

## 0.1.111
- Adds `/greenzone settings` with FC Chest Sync enabled by default for The Studium.
- Uploads tracked FC chest item counts when members open the FC chest.
- Reports only the FC chest tabs viewed during the current chest session.

## 0.1.110
- Changes the main command to `/greenzone`.
- Changes the overlay command to `/greenzone overlay`.

## 0.1.109
- Waits for the correct Lodestone tallying period before caching weekly seal rankings.
- Assigns published rankings to the completed challenge week.

## 0.1.108
- Adds a gold weekly reset pace marker to the FC Credits Target ring.

## 0.1.107
- Renames the daily activity title to Daily GC Seals.

## 0.1.106
- Shows the personal best week, GC Seals, and Ravana rank on one line.
- Uses standard white text with only the numbers highlighted in gold.

## 0.1.105
- Records weekly Lodestone seal results after the Monday publish window.
- Shows the active character's best recorded weekly GC Seals and Ravana rank.

## 0.1.104
- Shows the daily GC Seals total inside each activity box.

## 0.1.103
- Assigns seal hand-ins to daily boxes using the 8am reset boundary.

## 0.1.102
- Smoothly animates seal progress from the current displayed percentage when seals are added.

## 0.1.101
- Moved the overlay toggle into the weekly reset bar as plain text.

## 0.1.100
- Tracks personal seals earned for each day of the week.
- Fills the daily activity boxes in blue relative to the highest personal day.

## 0.1.99
- Left-aligned the daily activity title.
- Added more space below the daily activity title.

## 0.1.98
- Renamed the top seal earners heading.
- Added the daily activity title and weekday labels.
- Doubled the daily activity box height.

## 0.1.97
- Added seven translucent boxes to the bottom tile.
- Moved the overlay toggle beneath the bottom tile.

## 0.1.96
- Reduced the two main column heights by another 10px.

## 0.1.95
- Reduced the two main column heights a little more.

## 0.1.94
- Renamed the header start point label.
- Moved the overlay toggle into a new full-width tile.
- Reduced the two main column heights.

## 0.1.93
- Nudged the third top seal earner row up one more pixel.

## 0.1.92
- Nudged the third top seal earner row up a little more.

## 0.1.91
- Moved the third top seal earner row up slightly.

## 0.1.90
- Moved the divider below the second top seal earner up slightly.

## 0.1.89
- Nudged the second top seal earner row up a little more.

## 0.1.88
- Moved the second top seal earner row up slightly.

## 0.1.87
- Moved the top seal earner rows up slightly.

## 0.1.85
- Centered the overlay button group.

## 0.1.84
- Reduced the Open button width slightly.

## 0.1.83
- Adjusted overlay panel and button corner rounding.

## 0.1.82
- Increased the overlay width and rounded the panel corners.

## 0.1.81
- Restored the pre-tab overlay behavior.

## 0.1.80
- Added a left-edge tab that collapses and restores the overlay.

## 0.1.79
- Fixed the overlay close image loading so the plugin loads safely.

## 0.1.78
- Added a top-left image button for closing the overlay.

## 0.1.77
- Moved the first top seal earner divider down slightly.

## 0.1.76
- Moved the top seal earners title up slightly.

## 0.1.75
- Centered the top seal earners title and tightened the leaderboard spacing.

## 0.1.74
- Moved the top seal earners title up slightly in the FC Credits panel.

## 0.1.73
- Moved the top seal earners into the FC Credits panel with a cleaner list layout.

## 0.1.72
- Added the top 3 weekly Grand Company Seals earners from The Studium.

## 0.1.71
- Fixed the shared week base so it appears in the window header bar.

## 0.1.70
- Moved the shared week base into the window header bar.

## 0.1.69
- Moved the rotating FC information panel down slightly.

## 0.1.68
- Added a subtle blue border around the rotating FC information panel.

## 0.1.67
- Contained the rotating FC information text in a dark blue rounded panel.
- Extended each rotating item hold to 7 seconds.
- Highlighted numeric values in gold inside the rotating panel.

## 0.1.66
- Added a rotating information panel beneath the FC Credits target graph.
- Total FC Credits, weekly target progress, and personal estimated FC Credits now share one fade-in/fade-out space.
- Moved the shared week base beneath the rotating information panel.

## 0.1.65
- Removed obsolete local FC target, correction, and manual start-week controls.
- Updated the source and live repository documentation for the shared weekly baseline workflow.
- Added a short member guide explaining how to use The GreenZone and why it helps the FC.
- Kept local storage compact by removing unused legacy tracking fields from new saves.

## 0.1.64
- Shows the current Gil reward only for the latest completed tier.
- Keeps earlier completed tiers visibly complete without implying multiple rewards are paid.

## 0.1.63
- Added a helper bubble for the current reward message on the overlay.
- Shows that rewards are posted on Monday night and reminds members to have Gwen in their friends list.
- Completed tier bars now turn green, and the latest completed tier displays the current reward.

## 0.1.60 - 0.1.62
- Refined the main window layout around the FC target panel and personal tier panel.
- Renamed the FC target labels to use shorter, clearer FC Credits language.
- Added hover behavior that reveals the Gil reward for each tier.

## 0.1.50 - 0.1.59
- Added shared FC week support through `fc-week.json`.
- Moved FC target progress to a shared baseline so all members see the same weekly FC progress.
- Added support for Priority Seal Allowance `(+15%)` seal messages.
- Updated the GreenZone status and helper bubbles for active and inactive states.
