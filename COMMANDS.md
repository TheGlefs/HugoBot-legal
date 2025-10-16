## Management Commands

### `/setup`
**Description:** Run the bot setup process   

### `/captcha`
**Description:** Post the captcha verification message   
**Options:**
- `channel` (required, channel): Channel to post the captcha in
- `title` (optional, string): The title of the captcha message
- `description` (optional, string): The description of the captcha message

### `/role`
**Description:** Configure important server roles   
**Subcommands:**
- `verified`: Configure the role that counts as being verified
  - `enable` (optional, boolean): Enable or disable the verified role
  - `role` (optional, role): The role that counts as being verified
- `unverified`: Configure the role that counts as being unverified
  - `enable` (optional, boolean): Enable or disable the unverified role
  - `role` (optional, role): The role that counts as being unverified
- `moderator`: Configure the moderator role
  - `enable` (optional, boolean): Enable or disable the moderator role
  - `role` (optional, role): The role that counts as moderator

### `/logs`
**Description:** Server logging settings   
**Subcommands:**
- `error`: The error log channel where only bot error logs are sent
  - `enable` (optional, boolean): Enable or disable error logging
  - `mention` (optional, boolean): Enable or disable error logging mentions
  - `channel` (optional, channel): The channel to send error logs
- `general`: The general log channel where all logs are sent
  - `enable` (optional, boolean): Enable or disable general logging
  - `mention` (optional, boolean): Enable or disable general logging mentions
  - `channel` (optional, channel): The channel to send general logs
- `chat-only`: The chat-only log channel where only chat logs are sent
  - `enable` (optional, boolean): Enable or disable chat-only logging
  - `mention` (optional, boolean): Enable or disable chat-only logging mentions
  - `channel` (optional, channel): The channel to send chat-only logs

### `/message`
**Description:** Server join/leave/rejoin/ban/unban/kick/timeout/verified announcement message settings   
**Subcommands:**
- `join`: Announce when a user joins the server
  - `enable` (optional, boolean): Enable or disable the announcement when a user joins the server
  - `message` (optional, string): The message to send when a user joins
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{age}`, `{invitertag}`, `{invitername}`, `{inviteruser}`
  - `channel` (optional, channel): The channel to send join messages to
- `leave`: Announce when any user leaves the server
  - `enable` (optional, boolean): Enable or disable the announcement when a user leaves the server
  - `message` (optional, string): The leave message to send when a user leaves
    - **Available replacements:** `{tag}`, `{name}`, `{user}`
  - `channel` (optional, channel): The channel to send leave messages to
- `leave-verified`: Extra announcement when a verified user leaves the server
  - `enable` (optional, boolean): Enable or disable the extra announcement when a verified user leaves the server
  - `message` (optional, string): The message to send when a verified user leaves
    - **Available replacements:** `{tag}`, `{name}`, `{user}`
  - `channel` (optional, channel): The channel to send verified leave messages to
- `rejoin`: Announce when any user rejoins the server
  - `enable` (optional, boolean): Enable or disable the announcement when a user rejoins the server
  - `same-user` (optional, string): The message to send when a user rejoins
    - **Available replacements:** `{tag}`, `{name}`, `{user}`
  - `new-user` (optional, string): The message for users who changed their username
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{oldname}`, `{olduser}`
  - `channel` (optional, channel): The channel to send rejoin messages to
- `rejoin-verified`: Extra announcement when a verified user rejoins the server
  - `enable` (optional, boolean): Enable or disable the extra announcement when a verified user rejoins the server
  - `same-user` (optional, string): The message to send when a verified user rejoins
    - **Available replacements:** `{tag}`, `{name}`, `{user}`
  - `new-user` (optional, string): The message for verified users who changed their username
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{oldname}`, `{olduser}`
  - `channel` (optional, channel): The channel to send verified rejoin messages to
- `ban`: Announce when any user is banned
  - `enable` (optional, boolean): Enable or disable the announcement when a user is banned
  - `message` (optional, string): The message to send when a user is banned
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{modtag}`, `{modname}`, `{moduser}`, `{reason}`
  - `channel` (optional, channel): The channel to send ban messages to
- `ban-verified`: Extra announcement when a verified user is banned
  - `enable` (optional, boolean): Enable or disable the extra announcement when a verified user is banned
  - `message` (optional, string): The message to send when a verified user is banned
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{modtag}`, `{modname}`, `{moduser}`, `{reason}`
  - `channel` (optional, channel): The channel to send verified ban messages to
- `unban`: Announce when any user is unbanned
  - `enable` (optional, boolean): Enable or disable the announcement when a user is unbanned
  - `message` (optional, string): The message to send when a user is unbanned
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{modtag}`, `{modname}`, `{moduser}`, `{reason}`
  - `channel` (optional, channel): The channel to send unban messages to
- `unban-verified`: Extra announcement when a verified user is unbanned
  - `enable` (optional, boolean): Enable or disable the extra announcement when a verified user is unbanned
  - `message` (optional, string): The message to send when a verified user is unbanned
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{modtag}`, `{modname}`, `{moduser}`, `{reason}`
  - `channel` (optional, channel): The channel to send verified unban messages to
- `kick`: Announce when any user is kicked
  - `enable` (optional, boolean): Enable or disable the announcement when a user is kicked
  - `message` (optional, string): The message to send when a user is kicked
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{modtag}`, `{modname}`, `{moduser}`, `{reason}`
  - `channel` (optional, channel): The channel to send kick messages to
- `kick-verified`: Extra announcement when a verified user is kicked
  - `enable` (optional, boolean): Enable or disable the extra announcement when a verified user is kicked
  - `message` (optional, string): The message to send when a verified user is kicked
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{modtag}`, `{modname}`, `{moduser}`, `{reason}`
  - `channel` (optional, channel): The channel to send verified kick messages to
- `timeout`: Announce when any user is timed out
  - `enable` (optional, boolean): Enable or disable the announcement when a user is timed out
  - `applied` (optional, string): The message to send when a user is timed out
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{modtag}`, `{modname}`, `{moduser}`, `{reason}`, `{expiresat}`, `{expiresin}`
  - `removed` (optional, string): The message to send when a user timeout is removed
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{modtag}`, `{modname}`, `{moduser}`, `{reason}`
  - `expired` (optional, string): The message to send when a user timeout expires
    - **Available replacements:** `{tag}`, `{name}`, `{user}`
  - `channel` (optional, channel): The channel to send timeout messages to
- `timeout-verified`: Extra announcement when a verified user is timed out
  - `enable` (optional, boolean): Enable or disable the extra announcement when a verified user is timed out
  - `applied` (optional, string): The message to send when a verified user is timed out
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{modtag}`, `{modname}`, `{moduser}`, `{reason}`, `{expiresat}`, `{expiresin}`
  - `removed` (optional, string): The message to send when a verified user timeout is removed
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{modtag}`, `{modname}`, `{moduser}`, `{reason}`
  - `expired` (optional, string): The message to send when a verified user timeout expires
    - **Available replacements:** `{tag}`, `{name}`, `{user}`
  - `channel` (optional, channel): The channel to send verified timeout messages to
- `verified`: Announce when a user becomes verified
  - `enable` (optional, boolean): Enable or disable verified messages
  - `message` (optional, string): The message to send when a user becomes verified
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{roletag}`, `{rolename}`
  - `channel` (optional, channel): The channel to send verified messages to
- `verified-secondary`: Extra announcement when a user becomes verified
  - `enable` (optional, boolean): Enable or disable the extra announcement when a user becomes verified
  - `message` (optional, string): The secondary message to send when a user becomes verified
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{roletag}`, `{rolename}`
  - `channel` (optional, channel): The channel to send secondary verified messages to

### `/color`
**Description:** Manage color roles   
**Subcommands:**
- `add`: Add a color to the color list, automatically sorted by hue before saving
  - `name` (required, string): The name of the color role
  - `color` (required, string): The color of the color role
- `remove`: Remove a color from the color list
  - `name` (required, string): The name of the color role to remove
- `list`: List all available color roles
- `edit`: Edit an existing color role
  - `name` (required, string): The name of the color role to edit
  - `new-name` (optional, string): The new name for the color role
  - `new-color` (optional, string): The new color for the color role
- `default`: Configure default color role settings
  - `enable` (optional, boolean): Enable or disable default color roles
  - `name` (optional, string): The name of the default color role
- `create`: Create color roles on the server
  - `target` (required, user): The user to create color roles for
  - `prefix` (optional, string): Prefix for color role names
  - `suffix` (optional, string): Suffix for color role names
- `post`: Post color role selection message
  - `channel` (required, channel): The channel to post the color selection message
- `reset`: Reset all color role configurations

### `/group`
**Description:** Manage user groups that automatically grant channel permissions   
**Subcommands:**
- `create`: Create a user group that automatically grant channel permissions
  - `group` (required, string): The name of the user group
- `delete`: Delete a user group
  - `group` (required, string): The name of the user group
  - `revoke` (optional, boolean): Revoke access to all the channels in the group for all members?
- `list`: List all users and channels in a user group
  - `group` (optional, string): The name of the user group. Leave blank to list all groups.
- `restore`: Should group membership be restored when a user rejoins?
  - `group` (optional, string): The name of the user group
  - `enable` (optional, boolean): Enable or disable restoring group membership
- `add-member`: Add a member to a user group
  - `group` (required, string): The name of the user group
  - `member` (required, user): The member to add to the user group
- `add-channel`: Add a channel to a user group all members will get permissions for
  - `group` (required, string): The name of the user group
  - `channel` (required, channel): The channel that all group members will get permissions for
- `add-channel-viewers`: Add all users who can view a channel to a user group
  - `group` (required, string): The name of the user group
  - `channel` (required, channel): The channel to add all users who can view it to user group
- `add-role`: Add all users with a role to a user group
  - `group` (required, string): The name of the user group
  - `role` (required, role): The role to add all users with to the user group
- `remove-member`: Remove a member from a user group
  - `group` (required, string): The name of the user group
  - `member` (required, string): The member to remove from the user group
  - `revoke` (optional, boolean): Revoke access to all the channels in the group?
  - `inform` (optional, boolean): Inform the member that they have been removed from the group?
- `remove-channel`: Remove a channel from a user group
  - `group` (required, string): The name of the user group
  - `channel` (required, channel): The channel to remove from the user group
  - `revoke` (optional, boolean): Revoke access to the channel from all group members?
- `remove-role`: Remove a role from user a group
  - `group` (required, string): The name of the user group
  - `role` (required, role): The role to remove from the user group
- `edit-permissions`: Edit the automatic channel permissions for a user group
  - `group` (required, string): The name of the user group
  - `permission` (required, string): The permission to edit
  - `enable` (required, boolean): Enable or disable the permission
  - `mod` (optional, boolean): Is this a permission for mods only?
- `list-permissions`: List the automatic channel permissions for a user group
  - `group` (required, string): The name of the user group
- `refresh-permissions`: Refresh channel permissions for all members of a user group
  - `group` (required, string): The name of the user group
- `copy-permissions`: Copy channel permissions from one user group to another
  - `source` (required, string): The name of the user group to copy permissions from
  - `recipient` (required, string): The name of the user group to copy permissions to

### `/rolekick`
**Description:** Roles that automatically get kicked/banned from the server   
**Subcommands:**
- `settings`: Enable roles that get instantly kicked/banned from the server and edit ban/kick mode and reason
  - `enable` (optional, boolean): Enable or disable the rolekick/ban feature
  - `ban` (optional, boolean): Ban instead of kick? (default is kick)
  - `reason` (optional, string): Reason for kicking/banning members with forbidden roles (max 512 characters)
    - **Available replacements:** `{roletag}`, `{rolename}`
- `add`: Add a role that get instantly kicked/banned from the server, with optional retroactive application
  - `role` (required, role): The role to add to the list of roles that get instantly kicked/banned from the server
  - `retroactive` (optional, boolean): Apply this rule to existing members with this role
- `remove`: Remove a role from the kick/ban list
  - `role` (required, role): The role to remove from the list
- `list`: List all roles that get instantly kicked/banned

### `/autothread`
**Description:** Channels that automatically create threads on new messages   
**Subcommands:**
- `settings`: Enable automatically creating threads on new messages and edit their title and response
  - `enable` (optional, boolean): Whether automatic thread creation on new messages in autothread channels is enabled
  - `title` (optional, string): The title of the autothread threads
    - **Available replacements:** `{name}`, `{user}`, `{date}`, `{time}`
  - `message` (optional, string): The message to send when a thread is created
- `add`: Add a channel to create threads automatically
- `remove`: Remove a channel from automatic thread creation
- `list`: List all autothread channels

### `/agekick`
**Description:** Automatically kick/ban joining users based on account age   
**Subcommands:**
- `enable`: Enable or disable the auto-kick/ban feature
- `days`: The minimum account age in days
- `reason`: The reason for auto-kicking/banning users
- `ban`: Ban users instead of kicking them?

### `/autorole`
**Description:** Automatically assign roles to users joining the server   
**Subcommands:**
- `enable`: Enable automatic role assignment to users joining the server
  - `enable` (optional, boolean): Whether automatic role assignment to users joining the server is enabled
- `add`: Add a role that get assigned to users joining the server, with optional retroactive application
  - `role` (required, role): The role to add
- `remove`: Remove a role from automatic assignment
- `list`: List all autoroles

### `/starboard`
**Description:** Starboard channel which features messages reacted to with stars   
**Options:**
- `enable` (optional, boolean): Enable or disable the starboard feature
- `channel` (optional, channel): The channel to set as the starboard channel
- `stars` (optional, integer): The amount of stars a message needs to be featured
- `mod-stars` (optional, integer): The amount of stars a message needs to be featured when reacted by a moderator (optional)
- `thread-enable` (optional, boolean): Enable threads on starboard messages
- `thread-title` (optional, string): The title for starboard threads
  - **Available replacements:** `{name}`, `{user}`, `{date}`, `{time}`
- `thread-message` (optional, string): The message to send in starboard threads
- `thread-message-enable` (optional, boolean): Enable custom messages in starboard threads

### `/bump`
**Description:** Automatic bump reminder for the disboard bot   
**Options:**
- `enable` (optional, boolean): Enable or disable the automatic bump reminder
- `bumped` (optional, string): The message to send when a user bumps the server
  - **Note:** Simple text message, no replacement variables available
- `reminder` (optional, string): The reminder message to send when it's time to bump again
  - **Note:** Simple text message, no replacement variables available

### `/emulate`
**Description:** Emulate various user actions for testing   
**Subcommands:**
- `all`: Emulate all user actions
- `join`: Emulate a new user joining the server
- `leave`: Emulate a user leaving the server
- `leave-verified`: Emulate a verified user leaving the server
- `rejoin`: Emulate a user rejoining the server
- `rejoin-verified`: Emulate a verified user rejoin the server
- `kick`: Emulate a user being kicked from the server
- `kick-verified`: Emulate a verified user being kicked from the server
- `ban`: Emulate a user being banned from the server
- `ban-verified`: Emulate a verified user being banned from the server
- `unban`: Emulate a user being unbanned from the server
- `unban-verified`: Emulate a verified user being unbanned from the server
- `timeout`: Emulate a user being timed out
- `timeout-verified`: Emulate a verified user being timed out
- `verified`: Emulate a new user becoming verified
- `verified-secondary`: Emulate a user getting a secondary verification

## Leveling Commands

### `/xp`
**Description:** Chat XP/level system configuration   
**Subcommands:**
- `settings`: Enable the chat XP/level system and edit cooldown, min/max XP and channel
  - `xp-enable` (optional, boolean): Enable or disable XP gain from messages
  - `xp-cooldown` (optional, integer): Cooldown period for XP gain in ms (1000ms = 1s)
  - `xp-min` (optional, integer): Minimum XP per message based on message length
  - `xp-max` (optional, integer): Maximum XP per message based on message length
  - `role-enable` (optional, boolean): Enable role rewards for leveling up
  - `channel` (optional, channel): The channel to send level up messages to
  - `channel-enable` (optional, boolean): Enable level up message in channel
- `level-up`: Configure level up messages
  - `enable` (optional, boolean): Enable or disable level up messages
  - `message` (optional, string): The message to send when a user levels up
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{level}`, `{xp}`, `{xpneed}`, `{xpmiss}`
- `level-cmd`: Configure level command messages
  - `enable` (optional, boolean): Enable or disable the level command
  - `message` (optional, string): The message format for level command responses
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{level}`, `{xp}`, `{xpneed}`, `{xpmiss}`
- `rank-up`: Configure rank up messages
  - `enable` (optional, boolean): Enable or disable rank up messages
  - `message` (optional, string): The message to send when a user ranks up
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{level}`, `{xp}`, `{xpneed}`, `{xpmiss}`, `{roletag}`, `{rolename}`
- `rank-cmd`: Configure rank command messages
  - `enable` (optional, boolean): Enable or disable the rank command
  - `message` (optional, string): The message format for rank command responses
    - **Available replacements:** `{tag}`, `{name}`, `{user}`, `{level}`, `{xp}`, `{xpneed}`, `{xpmiss}`, `{rank}`, `{members}`
- `add-role`: Add a role reward for leveling up
  - `role` (required, role): The role to reward
  - `level` (required, integer): The level required to get this role
- `remove-role`: Remove a role reward
  - `role` (required, role): The role to remove from rewards
- `edit-role`: Edit a role reward level requirement
  - `role` (required, role): The role to edit
  - `level` (required, integer): The new level requirement
- `list-roles`: List all role rewards

### `/set`
**Description:** Set a user's XP or level   
**Subcommands:**
- `xp`: Set a user's XP
  - `target` (required, user): The user to set XP for
  - `xp` (required, integer): The XP to change to (minimum: 0)
- `level`: Set a user's level
  - `target` (required, user): The user to set level for
  - `level` (required, integer): The level to change to (minimum: 0)

### `/delete`
**Description:** Deletes a user's XP/level data from the server   
**Options:**
- `user` (required, string): The user to delete

### `/leaderboard`
**Description:** Shows the server XP/level leaderboard  

### `/rank`
**Description:** Shows your chat XP/level and rank on the server leaderboard  
**Options:**
- `user` (optional, string): The user to check

### `/level`
**Description:** Shows your chat XP/level on the server  
**Options:**
- `user` (optional, string): The user to check

### `/measure`
**Description:** Measure how much XP a message would give  
**Options:**
- `message` (required, string): The message to measure
