# tCLI
![tCLI_icon_v2](https://user-images.githubusercontent.com/46440248/142761121-ea1c9825-bec4-419b-8f29-5f6388a9411b.png)<br>
<!-- ![tCLI2_final](https://user-images.githubusercontent.com/46440248/128658059-9ddeecfb-f60a-4cfa-8392-e33c19f63fe5.png)<br> -->
Little, very simple [CLI](https://en.wikipedia.org/wiki/Command-line_interface) of twitch for Windows.<br>
Pronounce like that: "tickly", as in "tickle".
## Installation
[Download](https://github.com/eAlexandrohin/tCLI/releases/latest), install it and you good to go.
## Auth
Firstly, you need to authenticate.
Just type in cmd:
```
tcli
```

It will automaticly start authentication by opening your default browser.
```
Authenticating: opening browser...
```
 - You should authorize in the TwitchAPI.  
 - Then, you will  get sent  to the "localhost" with your auth token.
 - You should copy-paste it back in your cmd:
```
authToken: [your token]
```
And there you go - you've did it!
Here's your little reward!
```
Successful!
```
### Expiring auth tokens
Somewhen your token will be expired, but dont worry you're safe.<br>
You will get message about it and you will proceeded to reauth:
```
Your token has been expired or incorrect.
You will be proceeded to authentication.
```
After that, you will again be able to use tCLI!
### Switching accounts
Your account based on which you've been signup in twitch itself.<br>
So, just switch to different account in your default browser and run auth process again:
```
tcli auth
```
### Files
All data, information and content used, gathered and downloaded are stored in app folder in your Documents:
```
C:/Users/[Username]/Documents/tCLI
```
### Updates
tCLI will notify you about a new update, like this:
```
Update avaliable: v2.3.2.
You can update by running: "tcli update"
See: https://github.com/eAlexandrohin/tCLI/releases/latest
```
It checks every launch.
To update, simply use:
```
tcli update
```
 - It will download setup file.
 - And open it.
 - You should give admin rigths, if it asked, otherwise it will cancelled.
 - After you saw setup window you must close your original cmd. It will tell it to you.
 - Install it.
 - Done!
Now, you can run it again.
---
Last version setup installed always stored in update folder at app:
```
.../tCLI/update/
```
### Your auth data
It stored in app folder:
```
C:/Users/[Username]/Documents/tCLI
```
- Delete "auth.json" file.
 > DO NOT OPEN FILE ON STREAM

## Usage
```
tcli [command] [username] [...arguments]
```
Simple `tcli` will show live streams of your follows.
### Commands
> Tip: you can see basic version of this, in tCLI itself, by using: `tcli help`.
- `-f` sets titles to full
- `-v` returns current version of tCLI
- `auth` for repeating auth process
- `clips [username]` gets 100 clips from specified streamer sorted by views for week
  - `-dl [username]` downloads clips from specified user for specified time
  > location: `C:/Users/[Username]/Documents/tCLI/clips`
    - `-n` downloads one exact cilp, that you need
    - `-a/-y/-m/-w/-d` timestamps
  - `-id [clipID]` returns data about specified clip
    - `-c [clipID]` copies link to the clip
  - `-a/-y/-m/-w/-d` returns clips top of clips for `all time/year/month/week/day`
- `directory [gameName]/all` returns streamers from specified directory or from all
> If you want to select Just Chatting category or anything more than one word, use quotation marks:<br>`tcli directory "just chatting"`.
- `download [URL]` downloads .mp4 file
> Must be through HTTPS-protocol.
- `following [from] [to]` returns boolean of check if "from" user is following "to" user
- `follows` returns your follows with timestamps
  - `[username]` returns follows of that specified username with timestamps
- `help` returns all avaliable commands
  - `[command]` for specified command
- `link [username]` copies link to the stream of specified streamer, for using in VLC, for example, default quality is source
  - `[quality]` you can specify the quality, as in twitch player: 1080p60, 720p60, 720p and etc 
  - `-v [username]` you can choose vod, that you want to watch and it will copy its link, default quality is source
    - `[quality]` specifying quality, as in twitch player
- `live` default, shows up all live streams, that you following
  - `[username]` checks if specified user is live, if yes to returns data about its stream
- `login` returns data about your account
  - `[username]` returns data about specified user
- `teams` returns all teams that you had joined
  - `[teamName]` returns all members of the specified team
  - `-a [username]` returns all teams that specified streamer had joined
- `update` updates tCLI 
- `version` same as `-v`, see above
- `vods` returns vods by the time, from your follows
  - `[username]` returns vods of the specified username
  - `-f` sets titles to full
## Known bugs
1. If you paste link of clip to cmd and in your link have "**_&_**" character, cmd thinks that string after it is a command, so tries to exec it, but its not.<br>Please, remove it from link, if possible for more stability.
# Community
Feel free to post errors, contact me and stuff.<br>You're welcome!
> Hey, I know about [`Semantic Versioning`](https://semver.org/) - but, let me do my own little thing down here)<br>
> And about [`yargs`](https://github.com/yargs/yargs) too, and bout it's predecessor [`optimist`](https://www.npmjs.com/package/optimist) and bout his replacement by his own creator - [`minimist`](https://www.npmjs.com/package/minimist). <br>:)
# Legal
If you are a member of a Twitch Staff or working at Twitch and have questions, claims or anything - I will cooperate as much as I can. Or anyone who has something, email me at:<br>contact@ean.slmail.me
## Credits 
Uses NodeJS and such modules:<br>[`node-fetch`](https://github.com/node-fetch/node-fetch), [`express`](https://expressjs.com/), [`open`](https://www.npmjs.com/package/open), [`twitch-m3u8`](https://github.com/dudik/twitch-m3u8),<br>[`readline`](https://nodejs.org/api/readline.html), [`moment`](https://momentjs.com/), [`copy-paste`](https://github.com/xavi-/node-copy-paste), [`path`](https://nodejs.org/api/path.html),<br>[`os`](https://nodejs.org/api/os.html), [`fs`](https://nodejs.org/api/fs.html), [`https`](https://nodejs.org/api/https.html), [`nodejs-file-downloader`](https://www.npmjs.com/package/nodejs-file-downloader),<br>[`cli-progress`](https://www.npmjs.com/package/cli-progress), [`ansi-colors`](https://www.npmjs.com/package/ansi-colors), [`child_process`](https://nodejs.org/api/child_process.html).
___
##### License: __MIT__
