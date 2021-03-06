# Frequently Asked Questions

### Table of Contents

Find more in the [Table of Contents](https://github.com/Discord-Bot-Market/carl-bot/blob/main/TOC.md#table-of-contents)

## How do I create reaction roles?

Most people are probably best off using ``!rr make`` simply because it guides you through the process and tries to tell you what went wrong if any. Other ways of doing it includes using ``!rr aio`` which results in the same result as ``!rr make`` but with just a single command, it uses some weird syntax if you are unfamiliar, so I would recommend sticking to !rr make until you are familiar with the bot.

![image](https://user-images.githubusercontent.com/70546159/116555454-a6747c00-a8b9-11eb-924c-7e557ad019ba.png)

## What's the drama channel?
It's a premium feature that aims to streamline your server's moderation. Automod is nice, but it's not perfect, false positives happen. The drama channel was made for that exact reason. You need to:

1. Set up the drama channel. Either on the dashboard or with the command

``!am drama <channel>``

2. Set the automod punishment to 'Post to drama channel (premium only)' on the dashboard

![image](https://user-images.githubusercontent.com/70546159/116555748-f6534300-a8b9-11eb-9638-eac33da90cad.png)

## Why does the bot complain about requiring more permissions? I've given it manage roles already!

The way discord decides if you can add a role or not is based on two things:

1. Does the member adding the role have 'manage roles'

2. Is the member trying to add the role higher in the role hierarchy than the role they're trying to add?

Just assign the bot a role that is higher than highest role it has to assign, the role being hoisted does not have to have any special permissions.

## How do I get a message ID?

Discord settings -> Appearance -> Developer mode

![image](https://user-images.githubusercontent.com/70546159/116556088-53e78f80-a8ba-11eb-93ad-a2ec40a79bde.png)

For reaction roles already set up you can also use ``!rr show``

## How do I get the bot to announce new members joining?

Use the dashboard! https://carl.gg Just make sure to set a welcome channel in the top left box. You find the settings under 'welcome'.

## I don't want normal users creating tags, but I obviously can't disable tag, what do I do?

``!tag modonly`` will make it so that only mods can manage tags, while anyone can still use them

## I set up a highlight word but it's not working
Yes it is. The bot tries to detect when you're reading the chat and not spam you with unnecessary pings. If you wish to see if a message would have triggered any of your words, use ``!hl match <sentence>``

## Another bot has the same command and they both respond, what do I do?
Depends on what you're after. If you need to use both, you're pretty much forced to change the prefix of either bot. If you're after just the non-carlbot command, you can disable it with ``!disable <command>``. If you just want carlbot's command, I suppose you could create an alias using tags and ``{cmd:cmdname {args}}`` see the "Advanced tag usage" section for more information.
