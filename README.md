# `pug-bot`
A bot for managing pick-up games (aka scrims) on Discord.

The bot is programmed entirely in Python 3, and it makes use of the [discord.py (rewrite)](https://github.com/Rapptz/discord.py) package.

## Introduction
The creation of this bot was inspired by the daily League of Legends 10-mans in my guild.

The bot helps you keep track of teams and players, and it can also randomize teams for you. Another nice feature is that each team can pick a voice channel, and the bot will automatically move teams to their picked channels. After completing a round of games (i.e., when you run `..stop`), the lobby creator has the option to move all players to one voice channel automatically.

![example of usage](https://imgur.com/qv5WTkJ.png)

## Usage
The main flow for this bot is as follows:

1. Create a PUG
2. Have players join the PUG
3. Pick teams and channels
4. Start the PUG
5. Stop the PUG
6. Repeat or close it

Here's the list of commands:

| Command | Action
| :---- | :----
| `..help` | `pug-bot` will private message you a list of commands and their usage (i.e., basically everything in here)
| `..create [name] [size]` | Create a PUG with the given name and size
| `..join [name]` | Join the PUG with the given name
| `..leave` | Leave the PUG you're currently in
| `..cancel` | Delete the PUG you created
| `..start` | Starts your PUG and moves teams to their channels
| `..stop` | Stops the PUG and move players to a channel
| `..close` | Close a PUG, i.e., you can't interact with the PUG anymore
| `..reset` | Remove all teams in your PUG
| `..refresh` | Refresh the message with the PUG status
| `..remove [number]` | Remove a player from your PUG
| `..random [teams]` | Randomly create teams in your PUG, if there're enough people
| `..random captains [teams]` | Randomly assign captains in your PUG, if there're enough people
| `..team [team name]` | Create a team with the listed name and captain it
| `..rename [team name]` | Rename the team you're the captain of
| `..pick [number]` | Pick teammates from the player list
| `..kick [number]` | Kick teammates from your team
| `..channel` | Select your team's voice channel