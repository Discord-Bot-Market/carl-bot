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

#### ``rr move <base_id> <target_id>``

- **Example**: !rr move 458641514017587210 445066811097219082	
- **Usage**: Moves the reaction roles from one message to another. This works even if the message was purged (using the message id found in !rr show).

#### ``rr aio <channel> <color> <title | description> <emoji> <role>``

- **Example**: !rr aio #reaction eeaaee "hello there | this is a description" :red: hello :purple: there	
- **Usage**: SEPARATE EACH EMOJI-ROLE PAIR WITH A NEWLINE This is meant for power users who wish to create everything with just one command. The title and description have to be enclosed in double quotes.

#### ``rr aiou <channel> <color> <title | description> <emoji> <role>``

- **Example**: N/A	
- **Usage**: Works like !rr aio but also marks the message as unique

#### ``rr aiov <channel> <color> <title | description> <emoji> <role>``

- **Example**: N/A	
- **Usage**: All in one command to create a verification reaction role.

#### ``rr aioi <channel> <color> <title | description> <emoji> <role>``

- **Example**: N/A	
- **Usage**: All in one command to create an inverse verification reaction role, i.e. one that only removes roles.

#### ``!rr fixforeign <msg_id>``

- **Example**: !rr fixforeign 458641514017587210	
- **Usage**: Super niche command which can be used to have the bot react to emojis the bot doesn't have access to. One reason you might want to use this is because you want to use google's blob emojis. This command isn't required for these emojis to work, it only makes it so that the bot has its reactions added to the message. YOU HAVE TO REACT TO THE MESSAGE WITH THE EMOJIS YOURSELF BEFORE USING THIS COMMAND

#### ``rr maxroles <msg_id> [<role> <number>...]``

- **Example**: !rr maxroles 458641514017587210 DPS 10	
- **Usage**: Want to limit the number of x role? With this, you can. NOTE This checks for how many people have the role, not how many reactions there are.

#### ``rr [colour|color] <msg_id> <color>``

- **Example**: !rr color 458641514017587210 #00ee28	
- **Usage**: Changes the accent color of the specified bot message

The fastest and most reliable unique reaction roles of any bot.
![image](https://user-images.githubusercontent.com/70546159/116631727-cc7a3a80-a912-11eb-8422-ce947e38d973.png)


# Reaction Roles

To remove a bot message, simply delete the message like you would delete any other message, it's handled by the bot automatically.

| Name | Example | Usage |
| :--- | :--- | :--- |
| **rr \[setup\|make\]** | -- | Starts the interactive setup to get you started with reaction roles |
| rr \[list\|show\] \[msg\_id\] | -- | Shows the emoji-role pairs and their associated message id, useful for rr add. If a message id is specified, it will show additional information about that particular reaction role. |
| **rr edit &lt;msg\_id&gt; &lt;title \| description&gt;** | !rr edit 23094823094823490 Games \| Click on the games you want to be notified by | Edits the title and description, works like it does in the make command |
| **rr remove &lt;msg\_id&gt; &lt;role&gt;** | !rr remove 493018654405951488  fortnite | Removes an emoji-reaction pair from the specified bot message. |
| **rr move &lt;base\_id&gt; &lt;target\_id&gt;** | !rr move 493018654405951488 351050906189692938 | Moves the reaction roles from one message to another. This works even if the message was purged \(using the message id found in !rr show\). |
| **rr clear \[msg\_id\]** | !rr clear 12343323615155 | If you specify a message id, it removes all the roles from the message, if you don't, it will remove **all** reaction roles from the server. |
| **rr add \[channel\] &lt;msg\_id&gt; &lt;emoji&gt; &lt;role&gt;** | !rr add 1238901239812 :angel: pure | Adds the emoji-role pair to the message and the database. **NOTE:** This message id can belong to other people than carlbot, and the same emoji can be used for different messages for different roles \(useful for regional roles\) |
| **rr \[colour\|color\] &lt;msg\_id&gt; &lt;color&gt;** | !rr color 507068806800211969 \#00ee28 | Changes the accent color of the specified  bot message |
| **rr addmany \[channel\] &lt;msg\_id&gt; &lt;emoji role...&gt;** | !rr addmany 1238901239812 :angel: pure :poop: fortnite :grin: league of legends | **SEPARATE EACH EMOJI-ROLE PAIR WITH A NEWLINE** Works like **!rr add** except it adds more than one role at a time |
| **rr unique &lt;msg\_id&gt;** | !rr unique 123817349589 | Marks a message as 'unique' meaning a member can only claim one role from this message at a time, this works per message. Automatically removes the old reactions for you |
| **rr binding &lt;msg\_id&gt;** | !rr binding 123817349589 | A combination of rr verify and rr unique. Allowing for members to limit people to one choice ever. |
| **rr link &lt;base\_id&gt; &lt;target\_id&gt;** | !rr link 2389742349827 1239179273791283 | By linking two or more messages together, only one role from either message can be self-assigned. If you have 30 color roles for instance, linking the two messages together \(since the limit is 20/message\) allows a smooth, user-friendly experience when picking up roles. |
| **rr unlink &lt;msg\_id&gt;** | !rr unlink 2389742349827 | This breaks apart the entire group created by `!rr link` This means if you had three messages linked together, none of them will be after using this command. |
| **rr verify &lt;msg\_id&gt;** | !rr verify 123123123123 | With this enabled, reactions can only assign roles, not take them away. Additionally the bot automatically removes the reaction after the user reacts. This is useful for servers that want a verification reaction |
| **rr drop &lt;msg\_id&gt;** | !rr drop 123123123123 | Works sort of like rr verify, except it can only remove roles \(and roles are removed when the emoji is added\). This can be used for servers that automatically assign a role that you wish to remove. |
| **rr normal &lt;msg\_id&gt;** | !rr normal 123123123123 | This returns the reaction role message back to a normal reaction role message. Meaning any commands applied to it such as verify or unique will be removed. |
| **rr temp &lt;msg\_id&gt;  &lt;time&gt;** | !rr temp 2389742349827 24h | [Patreon only](https://www.patreon.com/carlbot): This allows for roles to be temporarily be assigned to a member and then removed after the designated amount of time. |
| **rr reversed &lt;msg\_id&gt;** | !rr reversed 2389742349827 | Reacting removes roles, unreacting adds roles. |
| **rr lock &lt;msg\_id&gt;** | !rr lock 2389742349827 | Locks the message preventing any roles from being handed out. |
| **rr limit &lt;msg\_id&gt; &lt;limit&gt;**  | !rr limit 2389742349827 5 | Limits members to picking up x amount of roles from a message. |
| **rr bl &lt;msg\_id&gt; &lt;roles...&gt;** | !rr bl 2389742349827 Staff | Prevents members with this role from picking up roles from the message.  |
| **rr wl &lt;msg\_id&gt; &lt;roles...&gt;** | !rr wl 2389742349827 Staff | Only members with one of these roles can pick up roles from the message. |
| **rr unbl &lt;msg\_id&gt;&lt;roles...&gt;** | !rr unbl 2389742349827 Staff | Removes a blacklisted role from the indicated reaction role message allowing for the role to pick up new roles from the message. |
| **rr unwl &lt;msg\_id&gt;&lt;roles...&gt;** | !rr unwl 2389742349827 Staff | Removes a whitelisted role from the indicated reaction role message preventing the role from picking up new roles from the message. |
| **rr clearbl &lt;msg\_id&gt;** | !rr clearbl 2389742349827  | Removes all roles from your blacklist for that set of reaction roles. |
| **rr clearwl &lt;msg\_id&gt;** | !rr clearwl 2389742349827  | Removes all roles from your whitelist for that set of reaction roles. |
| **rr maxroles &lt;msg\_id&gt; \[&lt;role&gt; &lt;number&gt;...\]** | !rr maxroles 2389742349827 DPS 10 | Want to limit the number of x role? With this, you can. **NOTE** This checks for how many people have the role, not how many reactions there are. |
| **rr selfdestruct &lt;msg\_id&gt; &lt;time&gt;** | !rr selfdestruct 2389742349827 7d | Deletes the message and all of its reaction roles after the time is up. |
| **rr aio &lt;channel&gt; &lt;color&gt; &lt;title \| description&gt; &lt;emoji&gt; &lt;role&gt;** | !rr aio \#reaction eeaaee "hello there \| this is a description" :red: hello :purple: there | **SEPARATE EACH EMOJI-ROLE PAIR WITH A NEWLINE** This is meant for power users who wish to create everything with just one command. The title and description have to be enclosed in double quotes. |
| **rr aiou &lt;channel&gt; &lt;color&gt; &lt;title \| description&gt; &lt;emoji&gt; &lt;role&gt;** | -- | Works like **!rr aio** but also marks the message as unique |
| **rr aiov &lt;channel&gt; &lt;color&gt; &lt;title \| description&gt; &lt;emoji&gt; &lt;role&gt;** | -- | All in one command to create a verification reaction role. |
| **rr aioi &lt;channel&gt; &lt;color&gt; &lt;title \| description&gt; &lt;emoji&gt; &lt;role&gt;** | -- | All in one command to create an inverse verification reaction role, i.e. one that only removes roles. |
| **!rr fixforeign &lt;msg\_id&gt;** | !rr fixforeign 351050906189692938 | Super niche command which can be used to have the bot react to emojis the bot doesn't have access to. One reason you might want to use this is because you want to use google's blob emojis. This command isn't required for these emojis to work, it only makes it so that the bot has its reactions added to the message. **YOU HAVE TO REACT TO THE MESSAGE WITH THE EMOJIS YOURSELF BEFORE USING THIS COMMAND** |
| **!embed &lt;channel&gt; &lt;color&gt; &lt;title \| description&gt;** | Pick up a role in \#get-roles to get pinged here | Creates an embed. |

[The fastest and most reliable unique reaction roles of any bot.](https://i.imgur.com/A7ShLfZ.mp4)

![Me setting up reaction roles in my support server.](../.gitbook/assets/w2kaapa-1.png)
