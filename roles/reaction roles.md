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
