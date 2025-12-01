# Commands
To use a command, you can either press `Slash`, type `/` 1 more time, or press the `Equals`, and you can type the commands. Using the first method requires prefixing with a `/`, i.e. `/commandname`. Arguments (if available) will be displayed as `<argname> <argname2>` where the `argname` is the value you will have to replace.

## General Commands
- `help`: Displays the commands menu. This menu might not update with latest commands.
- `cmds`: Brings up a dialog in which you can view a list of commands. This is often updated.
- `changes`: Displays server changelog.
- `suicide`: Exits from a private, public, or task map.
- `xpstatus`: Check which XP is active, i.e. Master, Giga, Super, Mega.
- `xppotion`: Check whether you have XP potion used, and displays remaining time if applicable.
- `playtime`: Combined play time of all players.
- `status <playername>`: Check the status message of a given player.
- `setstatus <message>`: Sets your status message.
- `clearstatus`: Clears your status message.
- `trust <name>`: Trusts a given player by name. Use `untrust <name>` to untrust.
- `mute <name>`: Mutes a given player by name. Use `unmute <name>` to unmute.
- `trustclear`: Clears your trusted players list.
- `muteclear`: Clears your muted players list.
- `trustlist`: Displays trusted players.
- `otrustlist`: Displays players that have trusted you.
- `mutelist`: Displays muted players.
- `omutelist`: Displays players that have muted you.
- `setonlinemsg <message>`: Sets your online message. Supports message variables.
- `setofflinemsg <message>`: Sets your offline message. Supports message variables.
- `feedback`: open feedback menu where you can create and manage your feedback.

## Team Related Commands
- `jointeam <ID> <password>: Joins a team using its ID.
- `t <message>`: Sends a message to the team.
- `teams`: Displays all available teams.
- `teammembers`: Displays your team members.
- `teampoints`: Displays your team points.
- `teamkills`: Displays your team kills.
- `teamleave`: Leaves the current team (if you are not the owner), or otherwise use below command.
- `teamcancel`: Deletes your team (if you are the owner). This option is irreversible!
- `getteampass`: Retrieves your team's password (if you are the owner).
- `changeteampass <password>`: Changes your team's password (if you are the owner).
- `changeteamleader <name>`: Changes your team's owner to `<name>` (if you are the owner).
- `atmod <name>`: Promotes a team member as a moderator.
- `rtmod <name>`: Demotes a team moderator.
- `tinvite <name>`: Invites a player to your team, if you are a moderator or a leader of the team.
- `ati`: Accepts a pending team invitation.
- `rti`: Rejects a pending team invitation.
- `teamkick <name>`: Removes a member from your team (if you are the owner).
- `teamcreate <ID> <name-optional>: Creates a team with a given ID. The name is optional and can contain spaces, and will be used to display. The ID is used as the name otherwise.
- `team <name>`: Check if a given player has a team, and in which if they have.
