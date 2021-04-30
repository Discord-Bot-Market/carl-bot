# Role Management

### Table of Contents

Find more in the [Table of Contents](https://github.com/Discord-Bot-Market/carl-bot/blob/main/TOC.md#table-of-contents)


### Info:
These commands are for administrators to manage role assignments in their servers. The bot might mention it or you requiring additional permissions despite having ``manage roles``. To fix this, make sure both you and the bot have roles higher in the role hierarchy than the role you're trying to assign.

## Role Commands

#### ``role <member> <role>``

- **Example**: !role @Carl#0001 fortnite pro	
- **Usage**: Adds/removes a role from the specified member

[![Tutorial](https://img.youtube.com/vi/-Ex0zd0qfj8/2.jpg)](https://www.youtube.com/watch?v=-Ex0zd0qfj8)

#### ``role add <member> <role>``

- **Example**: !role add @Carl#0001 idiot	
- **Usage**: Adds a role to the specified member

#### ``role remove <member> <role>``

- **Example**: !role remove @Carl#0001 idiot	
- **Usage**: Removes a role from the specified member

#### ``role color <role> <color>``

- **Example**: !role color weeb #eeaaee	
- **Usage**: Changes the color of a role

#### ``role [removeall|purge|clear] <@member>``

- **Example**: !role removeall @dumbguy#1337	
- **Usage**: Removes all roles from a member.

#### ``temprole <@member> <time> <role>``

- **Example**: !temprole @coolguy#0001 24h birthday boy	
- **Usage**: Adds a role for some time and removes it after the time is up. Time can be either before or after the role name.

#### ``temprole [custom|c] <@member> <time> <custom_string>``

- **Example**: !temprole @MichaelAus#9999 24h +Role 1 -Role 2	
- **Usage**: Gives the ability to add and remove roles temporarily within a single command, useful for removing roles for a period of time.

#### ``role create <name> [color] [mentionable=False] [hoist=False]``

- **Example**: !role create "cool dude" eeaaee true true	
- **Usage**": Creates a role. Hoist decides if it shows up in the sidebar or not.

#### ``allroles``

- **Example**: !allroles	
- **Usage**: Displays list of roles in the server and member count assigned to the role.

#### ``role info <role>``

- **Example**: !role info fortnite	
- **Usage**: Displays the role's Name, Member Count, Color, and when it was created.

#### ``role [custom|c] <member> <custom_string>``

- **Example**: !role custom @MichaelAus#9999 +Role 1 -Role 2	
- **Usage**: Gives the ability to add and remove roles within a single command, useful for removing a pending role whilst granting a member/joined role.

## Rank Commands

Ranks are roles that have been authorized by a server Admin or Moderator for self-assignment through the use of the ``rank`` command by users. This system is similar to ``iam`` commands in other bots.

#### ``addrank <roles...>``

- **Example**: !addrank fortnite weeb "f1 fanatic" "koishi fanboy" "tomato lover"	
- **Usage**: Adds one or more roles to the list of authorized ranks that members can assign to themselves.

#### ``removerank <roles...>``

- **Example**: !removerank fortnite "f1 fanatic"	
- **Usage**: Removes one or more roles from the list of authorized ranks, so that it can no longer be self assigned.

#### ``ranks``

- **Example**: !ranks	
- **Usage**: Lists all authorized ranks.

#### ``rank <role>``

- **Example**: !rank fortnite	
- **Usage**: Adds/removes the role to the person who used the command. Requires the role to be on the list of authorized ranks.

#### ``rank [custom|c] <custom_string>``

- **Example**: !rank custom +Role 1 -Role 2	
- **Usage**: Adds/removes multiple roles to the person using the command. Requires the role to be on the list of authorized ranks.

## Bulk Role Management

### Warning
Only one bulk assignment can be used at a time. Once started, a bulk role management command will give you an estimated time of completion, and the process cannot be stopped.

#### ``role all <role>``

- **Example**: !role all peon	
- **Usage**: Adds a role to every single member.

#### ``role bots <role>``

- **Example**: !role bots metallic overlord	
- **Usage**: Adds a role to every single bot.

#### ``role humans <role>``

- **Example**: !role humans flesh haver	
- **Usage**: Adds a role to all non-bots

#### ``role in <base_role> <assigned_role>``

- **Example**: !role in "movie fan" game of thrones	
- **Usage**: Adds a role (<assigned_role>) to all members with the <base_role> role. In the previous example, all members with the movie fan role would be assigned the game of thrones role.

#### ``role rall <role>``

- **Example**: !role rall admin	
- **Usage**: Removes a role from all members.

#### ``role rbots <role>``

- **Example**: !role rbots people	
- **Usage**: Removes a role from all bots.

#### ``role rhumans <role>``

- **Example**: !role rhumans metallic	
- **Usage**: Removes a role from all humans.

#### ``role rin <role>``

- **Example**: !role rin weeb cool dude	
- **Usage**: Removes a role from all members with the base_role. Previous example would have removed the "cool dude" role from all weebs.
