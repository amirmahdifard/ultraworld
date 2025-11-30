## Changes in 2.49 (Pieces of the Broken Clock)
- Removed vehicles.
- Redesigned player menus that open with `F5` and `Shift+F5` keys. In the menu that opens with `Shift+F5`, you can now press `Enter`, which will bring up yet another menu with contextual and possible options you can perform at the focused player. This means you do not necessarily need to remember the shortcuts. Due to this change, shortcuts within this menu are also reorganized.
- Added elevator and floor.
- Fixed a bug where connecting back to the server upon it is restarted while you are in a menu would block, which makes you unable to open other menus.
- You can now receive player events that are performed yourself if the player events buffer is muted. Thanks "Rishi".
- All server menus are now using the new and more responsive menu system. Also, most menus in client will now use the new menu system to make them more responsive.
- Added options menu in the game. To open it, press `Alt+O` key. Currently, option menu contains manage your account.
- Players can now change password! Available in manage account section of the options menu.

## Changes in 2.48 (The Hearth of a New Generation)
- Added 3 new commands. `/tinvite <name>` will invite a player into your team. `/ati` will accept the invitation, and `/rti` will refuse the invitation. Each player can only hold 1 invite. Thus, if the player has already been invited by someone, other players cannot invite that player until they have accepted or refused. If you accept an invitation but you are already in a team and are not the leader, you will leave the team.
- Managers can now merge 2 teams if requested. Only do this when it is necessary.
- Modified the house system.
- Added a new house called Apartment, anyone with a house or not, anyone, married or not, can buy it. The residencial building is currently in the Lindow Town.
- Added tents, now players can place there tents like how you place other houses, there is no specific map for tents, just some maps restrict them. you can also pick up your tents when you dont need them out in the open with enter.
- skillets no longer work with ID's. yay.
- You can now open your house / apartment doors with `Alt+Enter` while standing on the door from inside or outside your house for 8 seconds. While the door is open, anyone can enter your house without the code. Be careful! Only use this when people you dont trust arent around your house!
- Assistants can now review to admintells and respond to them.
- Assistants can now edit, add or otherwise remove item descriptions.
- Added `/teammods` command to list moderators of the team.
- Store items now provide description.
- Team moderators can no longer kick the team leader off the team. Oops? Hopefully no leaders have been kicked previously.
- The `/teams` command now sorts teams by the best rank. The sorting system uses the team's total kills and points in order to determine the rank. This means that, even if your team has higher kills, this does not mean your team is the best. Sorting system will always determine based on the points and kills total.
- Sonar has now been removed completely.
- Zones will no longer go to buffer, and the zones buffer has been removed.
- The bug where the inventory could be obtained upon login if the player is in jail has been resolved.
- The notifications when a staff member comes online have been removed, you can view who is staff in the `/staff` command anyway. Thanks "Fifi" and "Rishi".
- Added 1 new buffer called "Player Events" which receives all player related activities, including away messages, AFK messages, so on and so forth. This means if you do not want to receive them, you can mute the entire "Player Events" buffer. Thanks "Fifi".
- AI will no longer go out of their designated coordinate range.
- Jail system has been polished. The system can now jail a player for a given time. Note. The jail time means the player's actual online time.
- Inventory will no longer send amounts to the server when sorting items. This would hopefully disable the cheat engine.
- Spam character kill system has now gotten a lot more sophisticated.
- Added a command called `/otrustlist` to view who has trusted you.

## Changes in 2.47 (The Taking Chances)
- Fixed buffer playing sounds while muted.
- Admins can now destroy houses easily should it be necessary.
- Added assistant rank.
- Modified some weapons.
- You can now press `Shift+' (Apostrophe)` to chat to your team.
- All staff ranks have now a new system called SCP (Sophisticated Control Panel, or Staff Control Panel).
- Added private message history system. Press `Alt+P`, and it will display the last 100 messages sent and received. Press `Enter` on one of them, and it will directly bring you to reply field!
- Added a new command for team leaders: `/teaminfo` allows you to check your team info.
- Changed zone tracking key to `O` key. Thanks "Rishi".

## Changes in 2.46 (The Hearth of Ultra World!
- Finally, finally, the houses are enabled for building in the residencial area! The names of the house items are also changed and have their prices increased. The Conex (the single house) is now named as `golden_gate_house`, and the partner house is now named as `rosehaven_house`.
- Buffer now has actual muting system. This means that when you mute a buffer, the speech and sound will not play, but the items will be there. If you want to even disable items from coming, you can deactivate the buffer.
- You can now copy buffer item by pressing `Shift+C`.
- Language channel managers can now press `Shift+Alt+L` to set the message of the day of their channel rather than using the `/newlmotd` command. The command is still available though.
- Language channel managers can now press `Shift+D` to chat between language channel managers of all languages, i.e. for communication purposes.
- Fixed TTS.
- Removed restart option.
- The `/channelusers` command now displays if they are channel managers.
- Added the `/lcms` command to display all language channel managers of all languages.
- Fixed stream volume.
- Hopefully fixed the bug where your contributed maps do not appear until you log off, thanks "Nyx".

## Changes in 2.45
- Fixed the bug where you are unable to move the inventory items faster. Thanks "Charry".
- Fixed test speakers.
- Removed some titles, as they are not that useful at all.
- Added language channel manager. Each channel can now have different message of the day. As such, you must now press `Alt+F4` and `Alt+Shift+F4` respectively to get the server English message, and the normal `F4` and `Shift+F4` for per-channel message.

## Changes in 2.44
This is a small patch update mainly to fix the buffer muting bug.
- Added automatic update extraction script.
- Fixed buffer muting, thanks "Aleesya" for the immediate report.
- Fixed some bugs of vehicles, thanks to several players.
- Fixed the bug where using teleporter freezes everyone. Thanks "Aiden".
- Added 2 new keys for inventory menu. Press `Ctrl+C` to copy the item name, and `Ctrl+Shift+C` to copy the item amount to the clipboard.
- Added positional indication when you move items in the inventory.

# Changes in 2.43
- Hopefully fixed the network problem, including double sound.
- Buffer menu that opens with `Shift+B` is back as it is seriously requested!
- Hopefully fixed the error of the inventory. Unfortunately this only affects 1 player, and this change has yet to be confirmed.
- Player menus now support multiletter navigation.

## Changes in 2.40
Welcome to the first version of NVGT engine. Therefore, bugs might arrive. This version contains bug fixes, redesigned systems, improvements, and removals and is thus recommended that you read the change log before you play. Since this is the first start on NVGT engine, future bugs might be found, and we suggest that you report bugs to us as well as give suggestions and ideas that you think might be considerable enough for such suggestions and/or ideas to be implemented. This version also includes changes to sound system, UI controls and responsive menus, as well as security implementations.
- Ultra World now supports actual 3D sound environment!
- Fixed most of the runtime errors.
- The `/teamcreate` now takes a new argument. `/teamcreate <id> <team name>`. The ID is the normal, small, identifier, while the team name is your display name and thus can contain spaces. Players must always use the ID when the team ID is needed to be set, such as in `/jointeam` command. Thus, ID can never change once created.
- Added a new command called `/teamnickname <team name>` that changes your team's display name.
- Fixed the bug where you spawn in the jail after you die in a task map.
- Map error handle is now improved. It will tell you what went wrong, on which line, rather than otherwise causing the runtime error and causes the game to crash.
- Removed voice chat. We have already considered the possibility that this system might be reimplemented in future version after we review that the new NVGT's sound system is working properly to change to it.
- Removed visual mode and some other options from the settings.
- You can now hear others wall bumping sounds.
- Added reverb.
- Redesigned buffer system.
- Redesigned inventory system. Now you can switch order of items using the Alt key alongside normal navigation keys. Note, switching order only works if you have the category set to all.
- The inventory search and cycle / navigation systems have been redesigned. The `Shift+S` inside the inventory has been changed to `CTRL+F`. Multi letter navigation is now possible. The `Alt+V` key outside of inventory also gets replaced by a new search dialog.
- Rewritten ban system.
- Redesigned staff system.
- Rewritten how network is handled on the server. The server should now response better.
- Redesigned moving system.
- Added per-coordinate based death message system.
- Redesigned input system. As the result, you can now type in your language, provided that it is in UTF8 encoding. Multi line is now supported in chat.
- Removed entertainment games.
- Added DVS (Dynamic Variable System). Fully documented in README.
- Redesigned map variables to support dynamic variables. The `%n` was no longer available.
- Redesigned online and offline message system which now has the addition of the ability to use dynamic variables, mainly gender codes.
- Added updater.
- Redesigned the `/me` command to add the ability to use dynamic variables.
- AI now has gender. Usually, this depends on the staff who would set it, but under its default, the gender will be randomized.
- Fixed PVP and jail title when turning off PVP or when unjailed.
- Fixed automatic falling bug when you enter or exit from a map.
- Some text fields, such as changelog and rules, will now be displayed as form input boxes instead of the menu.
- Fixed the bug where the required XP is not being correctly evaluated upon login.
- You can no longer create characters that are not allowed, i.e. comma and slash characters.
- Removed Turrets.
- Redesigned map system. It now supports having its own automatic updated date.
- Redesigned account login and creation systems.
- Fixed a bug where the hand did not clear the drawn item after the item was no longer present in the inventory.
- Completely redesigned the auction system.
- Age will now automatically calculate.
- Fixed map level and reinforcement maximum values.
- Added nutrition machines. These machines can make foods and drinks such as coffee. The recipes are documented on the website.
- When using items mode, you must now press `Shift+Space` to jump, not `Alt+Space`.
- Dropping with `Shift+Delete` has been fixed, especially on fire.
- You can now press `Ctrl+Delete` in the inventory to drop the entire quantity of the focused item.
