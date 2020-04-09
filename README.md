# Updated & modified ytdl-core-discord

[![dependencies](https://david-dm.org/hardrock13/tirpitz.svg)](https://david-dm.org/hardrock13/tirpitz)

A [ytdl-core](https://github.com/fent/node-ytdl-core/) wrapper focused on efficiency for use in Discord music bots.

Check [ytdl-core-discord](https://github.com/amishshah/ytdl-core-discord) as the original is that one. All thanks go to him.

This is an updated version which contains all the latest updates, mainly:
- @types/node to 13.11.1
- prism-media to 1.2.1
- ytdl-core to 2.0.1
- eslint to 6.8.0

## Additional to that, this one solves the issue of youtube short links (and other non-standard) that threw the error of "No video id found: actual-working-youtube-link".
  I don't think that was exclusive to me, because the module's use was standard. Discord.js tested version 12.1.1.
  I'm sorry if this GitHub repo is a bit rough. It's my first time working with it.

## Usage in Discord.js 12.x

```js
const ytdl = require('ytdl-core-discord');

async function play(connection, url) {
  connection.play(await ytdl(url), { type: 'opus' });
}
```

## Usage in Discord.js 11.4.x

```js
const ytdl = require('ytdl-core-discord');

async function play(connection, url) {
  connection.playOpusStream(await ytdl(url));
}
```
