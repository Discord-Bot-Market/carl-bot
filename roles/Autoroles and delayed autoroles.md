# Autoroles and delayed autoroles

### Table of Contents

Find more in the [Table of Contents](https://github.com/Discord-Bot-Market/carl-bot/blob/main/TOC.md#table-of-contents)

### Info:
If you have autoroles and reassigned roles, the returning member will receive the union of both.

## Automatic Roles

#### ``[autorole|autoroles]``

- **Example**: !autoroles	
- **Usage**: Shows which roles will be added upon joining and if the bot will readd roles when someone leaves and rejoins the server

#### ``autorole [readd|reassign]``

- **Example**: !autorole readd	
- **Usage**: Turns reassigning roles on/off

#### ``autorole add <role>``

- **Example**: !autorole add peon	
- **Usage**: Autoroles are roles that are given to the user upon joining the server.

#### ``autorole remove <role>``

- **Example**: !autorole remove admin	
- **Usage**: Removes a role from being auto assigned

#### ``autorole [bl|blacklist] <roles...>``

- **Example**: !autorole bl admin newbie	
- **Usage**: Prevents the mentioned roles from being reassigned

#### ``autorole unblacklist <roles...>``

- **Example**: !autorole unblacklist "fortnite expert" admin	
- **Usage**: Undoes what !autorole bl does

## Delayed Autoroles

#### ``[tr|timedrole]

- **Example**: !timedrole	
- **Usage**: Shows the roles being assigned with their delay

#### ``timedrole [add|+] <time> <role>``

- **Example**: !timedrole add 42h19m22s fortnite expert	
- **Usage**: Adds a role to be added with a delay

#### ``timedrole remove <role>``

- **Example**: !tr remove newbie	
- **Usage**: Removes the role from being automatically assigned and also cancels any pending roles (Note: all pending delayed roles with the same delay as the removed role will be removed, sorry!)
