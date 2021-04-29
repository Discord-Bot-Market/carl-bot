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
