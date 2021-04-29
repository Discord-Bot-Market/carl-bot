# Reaction Roles

### Table of Contents

Find more in the [Table of Contents](https://github.com/Discord-Bot-Market/carl-bot/blob/main/TOC.md#table-of-contents)

### Tip:
Deleted messages are also cleared from the database. Pin the reaction role message to make it immune to purging.

## RR Management

### Info:
``reactrole``, ``reactionrole``, and ``rr`` are all aliases for the same base command.

#### ``rr [make|setup]``

- **Example**: !rr make 
- **Usage**: Starts the interactive setup to get you started with reaction roles


#### ``rr [list|show] [msg_id]``

- **Example**: !rr show
- **Usage**: Shows the emoji-role pairs and their associated message id, useful for rr add. If a message id is specified, it will show additional information about that particular reaction role.

#### ``rr add [channel] <msg_id> <emoji> <role>``	

- **Example**: !rr add 458641514017587210 👼 @pure
- **Usage**: Adds the emoji-role pair to the message and the database. NOTE: This message id can belong to authors other than Carl-bot, and the same emoji can be used for different messages for different roles (useful for regional roles)

#### ``rr addmany [channel] <msg_id> <emoji role...>``

- **Example**: !rr addmany 458641514017587210 👼 @pure 💩 @fortnite 😁 @league of legends	
- **Usage**: Works like !rr add except it adds more than one role at a time. SEPARATE EACH EMOJI-ROLE PAIR WITH A NEW LINE USING: Shift+Enter

#### ``rr remove <msg_id> <role>``
  
- **Example**: !rr remove 458641514017587210 @fortnite	
- **Usage**: Removes an emoji-reaction pair from the specified bot message.

#### ``rr clear [msg_id]``	

- **Example**: !rr clear 458641514017587210	
- **Usage**: If you specify a message id, it removes all the roles from the message, if you don't, it will remove all reaction roles from the server.

#### ``rr bl <msg_id> <roles...>``

- **Example**: !rr bl 458641514017587210 Staff	
- **Usage**: Prevents members with this role from picking up roles from the message.

#### ``rr wl <msg_id> <roles...>``

- **Example**: !rr wl 458641514017587210 Staff	
- **Usage**: Only members with one of these roles can pick up roles from the message.

#### ``rr unbl <msg_id> <roles...>``

- **Example**: !rr unbl 458641514017587210 Staff	
- **Usage**: Removes a blacklisted role from the indicated reaction role message allowing for the role to pick up new roles from the message.

#### ``rr unwl <msg_id> <roles...>``

- **Example**: !rr unwl 458641514017587210 Staff	
- **Usage**: Removes a whitelisted role from the indicated reaction role message preventing the role from picking up new roles from the message.

#### ``rr clearbl <msg_id>``

- **Example**: !rr clearbl 458641514017587210	
- **Usage**: Removes all roles from your blacklist for that set of reaction roles.

#### ``rr clearwl <msg_id>``

- **Example**: !rr clearwl 458641514017587210	
- **Usage**: Removes all roles from your whitelist for that set of reaction roles.

#### ``rr selfdestruct <msg_id> <time>``
  
- **Example**: !rr selfdestruct 458641514017587210 7d	
- **Usage**: Deletes the message and all of its reaction roles after the time is up.

#### ``rr edit <msg_id> <title | description>``

- **Example**: !rr edit 458641514017587210 Games | Click on the games you want to be notified by	
- **Usage**: Edits the title and description, works like it does in the make command

#### ``rr [channel|cc] [name=get-roles]``

- **Example**: !rr cc color-roles	
- **Usage**: Creates a channel with the sort of permissions you most likely want for a reaction role channel (yes, add reactions is off, this is intentional)

#### ``rr fix``

- **Example**: !rr fix	
- **Usage**: Accidentally (or intentionally) cleared all reactions? Use this command to have the bot add the reactions missing

## RR Types

### Info:
Types are per message and change their behavior. Every message has a type which defaults to normal.

#### ``rr unique <msg_id>``

- **Example**: !rr unique 458641514017587210	
- **Usage**: Marks a message as 'unique' meaning a member can only claim one role from this message at a time, this works per message. Automatically removes the old reactions for you

#### ``rr binding <msg_id>``

- **Example**: !rr binding 458641514017587210	
- **Usage**: A combination of rr verify and rr unique. Allowing for members to limit people to one choice ever.

#### ``rr link <base_id> <target_id>``

- **Example**: !rr link 458641514017587210 445066811097219082	
- **Usage**: By linking two or more messages together, only one role from either message can be self-assigned. If you have 30 color roles for instance, linking the two messages together (since the limit is 20/message) allows a smooth, user-friendly experience when picking up roles.

#### ``rr unlink <msg_id>``

- **Example**: !rr unlink 458641514017587210	
- **Usage**: This breaks apart the entire group created by ``!rr link`` This means if you had three messages linked together, none of them will be after using this command.

#### ``rr verify <msg_id>``

- **Example**: !rr verify 458641514017587210	
- **Usage**: With this enabled, reactions can only assign roles, not take them away. Additionally the bot automatically removes the reaction after the user reacts. This is useful for servers that want a verification reaction

#### ``rr drop <msg_id>``

- **Example**: !rr drop 458641514017587210	
- **Usage**: Works sort of like rr verify, except it can only remove roles (and roles are removed when the emoji is added). This can be used for servers that automatically assign a role that you wish to remove.

#### ``rr normal <msg_id>``

- **Example**: !rr normal 458641514017587210	
- **Usage**: This returns the reaction role message back to a normal reaction role message. Meaning any commands applied to it such as verify or unique will be removed.

#### ``rr temp <msg_id> <time>``

- **Example**: !rr temp 458641514017587210 24h	
- **Usage**: Patreon only: This allows for roles to be temporarily be assigned to a member and then removed after the designated amount of time.

#### ``rr reversed <msg_id>``

- **Example**: !rr reversed 458641514017587210	
- **Usage**: Reacting removes roles, unreacting adds roles.

#### ``rr lock <msg_id>``

- **Example**: !rr lock 458641514017587210	
- **Usage**: Locks the message preventing any roles from being handed out.

#### ``rr limit <msg_id> <limit>``

- **Example**: !rr limit 458641514017587210 5	
- **Usage**: Limits members to picking up x amount of roles from a message.

## Advanced/niche

### Warning
These commands come in very handy in certain situations, but may cause confusion to people unfamiliar with how Carl-bot's reaction roles work.

