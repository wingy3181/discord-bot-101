Overview
========

There should be a `config.json` file with the following contents:

```json
{
  "token": "<token of bot from discord>",
  "prefix": "+"
}
```

References
==========

Discord Application + Bot Setup
-------------------------------    
-   [x] [Creating a discord bot & getting a token](https://github.com/reactiflux/discord-irc/wiki/Creating-a-discord-bot-&-getting-a-token)
-   [x] [Official Discord Developer Apps Documentation](https://discordapp.com/developers/docs/intro)

Discord `npm` packages
----------------------
-   [x] [NPM Registry - Query 'discord' npm packages](https://www.npmjs.com/search?q=discord)

Discord.io
----------
-   [x] [Tutorial: Creating a simple Discord Bot](https://medium.com/@renesansz/tutorial-creating-a-simple-discord-bot-9465a2764dc0)
    -   **Uses:**
        -   **[winston](https://github.com/winstonjs/winston) for logging**
    -   [x] <https://discordapp.com/api/oauth2/authorize?client_id=402719089329700864&permissions=0&scope=bot>
    -   [x] [[EDIT: I FIXED IT] when I run node bot.js, nothing happening..](https://github.com/renesansz/discord-greeter-bot/issues/44)
    -   [x] [node bot.js won't work](https://github.com/renesansz/discord-greeter-bot/issues/30)

Discord.js
----------
-   [x] [Discord.js official documentation](https://discord.js.org/#/docs/main/stable/general/welcome)
-   [x] [The Perfect Lil' Bot - Example discord bot with discord.js](https://gist.github.com/eslachance/3349734a98d30011bb202f47342601d3)
-   [x] [A powerful JavaScript library for interacting with the Discord API](https://github.com/hydrabolt/discord.js)
-   [x] [Discord.js Bot Guide](https://anidiotsguide.gitbooks.io/discord-js-bot-guide/) 👍
    -   **NOTE:**
        -   Best practices
            -   Return if author is bot or if no prefix
            -   reload using require.cache and require.resolve
        -   How to separate commands and events into their own folder (command handlers)
        -   How to use embed
            -   <https://leovoel.github.io/embed-visualizer/>
        -   Persisting data to a JSON file, SQLite or Enmap
        -   Cleverbot integration, self bots and use of emojis
        -   Examples of remember data, using an array to avoid too much conditional logic, "eval"
        -   Hosting bots on [Glitch.com](https://glitch.com/) for free
        -   [ShareX](https://getsharex.com/) and integration with webhook (Screenshot tool)
-   [x] [Discord.js Bot Guide - Youtube Videos Playlist](https://www.youtube.com/playlist?list=PLR2_rarYLHfg6ZJqq0WTMmI9uLcd7_GRO)
    -   x ] [Github - An-Idiots-Guide/Tutorial-Bot](https://github.com/An-Idiots-Guide/Tutorial-Bot)
        -   Use `nodemon`
        -   Episode 02: Multiple cmmands
            -   User Settings - Developer mode on to get menu items to easily copy id's of channels, users, messages, etc
            -   Sending message to another channel
            -   Set status
            -   Set game
        -   Episode 03: Guild events
            -   [`return-deep-diff`](https://www.npmjs.com/package/return-deep-diff) npm module for comparing collections
        -   Episode 04: Client events
            -   Use regex to remove any tokens or hidden info when using events: debug, warn, error
            -   Handle `disconnect` and `reconnecting` events and log them so can find out when and why bots sometimes keep disconnecting/reconnecting
            -   [`chalk`](https://www.npmjs.com/package/chalk) npm module for colorizing logs
        -   Episode 05: Roles
            -   Put backslash infront of a mention to get the ID
            -   Role events and how to programmatically update/add/delete/set roles
        -   Episode 06: Handlers - Part I
            -   Converting into separate files for events and commands with an eventHandler and commandHandler respectively
            -   Deleting node require.cache to reload a command
        -   Episode 06: Handlers - Part II
            -   Converting into using Evie.selfbot/York-Dev discord bot framework
                -   Restriction of commands via a permission level dependent on roles
                -   Useful `help` commands and configuration per command for documentation, aliases, etc
        -   Episode 07: Warning, Mute & Lockdown
            -   Use of [`ms` npm module](https://www.npmjs.com/package/ms) to convert human readable time to ms and vice versa
            -   Example of adding validation to commands and checking inputs are valid
            -   Warn users with mentions and log to a mod channel (doesn't warn users in videos implementation)
            -   Mute/Unmute users with mentions by adding/removing a mute role to them
            -   Lockdown a channel for set period of time (can unlock, uses `setTimeout`, `clearInterval` for only locking for set times)
        -   Episode 08: Kick, Ban & Unban
        -   Episode 09: Embeds
            -   Looking at discord.js release notes and modifying deprecated methods
            -   Using embed description instead of addField (seems to support Markdown syntax)
        -   Episode 10: Case logs and fixes - Part I
            -   Removal of `deep-diff` due to circular references causing out of memory errors
            -   Use embed footer to create "cases", and update reason for cases later
            -   Sanitise embed of any circular references before editing
            -   Generate new case numbers via a utility function method that is in its own module, grabs previous case number and increases by 1s
        -   Episode 10: Finishing up - Part II
            -   Added logic to only run moderation commands on users with lower role levels
-   [x] [Discord.js Bot Guide - Youtube Videos Playlist - Viewer's Requests](https://www.youtube.com/playlist?list=PLR2_rarYLHfiiGobZwWFLtZteu6pd_nRy)
    -   [x] Glitch.com hosting
    -   [x] Guidebot dashboard 👍
        -   <https://github.com/An-Idiots-Guide/guidebot-class>
-   [x] [Github - YorkAARGH/York-Dev - Reference app](https://github.com/YorkAARGH/York-Dev) 👍
-   [x] [Github - Hyvnoic/guidebot - Reference app](https://github.com/Hyvonic/guidebot)
-   [x] [Github - An-Idiots-Guide/guidebot - Reference app](https://github.com/An-Idiots-Guide/guidebot) 👍
-   [x] [Github - Evie.Selfbot - Reference app](https://github.com/eslachance/evie.selfbot)
-   [x] [List of bots](https://botlist.co/)
-   [x] [discord-coinmarketcap-bot](https://github.com/EricCrosson/discord-coinmarketcap-bot)
    -   **Uses:**
        -   **[coinmarketcap-api](https://github.com/ericcrosson/coinmarketcap-api) for access data from coinmarketcap.com**
        -   **[cryptocurrencies](https://github.com/crypti/cryptocurrencies) for a JSON list of all the cryptocurrency symbols and names**
        -   **[imgur](https://github.com/kaimallea/node-imgur) for uploading images to imgur**
        -   **[webshot](https://github.com/brenden/node-webshot) for taking webpage screenshots with PhantomJSx**
-   [x] [Crypton - a Discord bot for fetching and displaying prices of cryptocurrencies from exchanges through their public APIs and more crypto-related stuff](https://github.com/Trophonix/Crypton)
    -   **NOTES:**
        -   commands are separated out
        -   express REST API endpoints
        -   'help' usage commands
        -   Examples of using discord.js RichEmbed
        -   Calling binance API every interval and caching this in memory (see index.js)


Akairo (Discord.js bot framework)
---------------------------------
-   [ ] [A bot framework for Discord.js](https://github.com/1Computer1/discord-akairo)
-   [x] [Discord-Akairo Tutorials](https://1computer1.gitbooks.io/akairo-tutorials/content/)
