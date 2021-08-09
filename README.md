# tCLI
![tCLI2_final](https://user-images.githubusercontent.com/46440248/128658059-9ddeecfb-f60a-4cfa-8392-e33c19f63fe5.png)<br>
Little, very simple [CLI](https://en.wikipedia.org/wiki/Command-line_interface) of twitch for Windows.<br>
Pronounce like that: "tickly", as in "tickle".
## Installation
[Download](https://github.com/eAlexandrohin/tCLI/releases), install it and you good to go.
## Auth
Firstly, you need to authenticate.
Just type in cmd:
```
tcli
```

It will automaticly start authentication.
- You will get asked for your twitch login, like this, type it and press "Enter":
```
login: [your login here]
```
- After it, tCLI will open your default browser and you will need to authorize in the TwitchAPI.
- You will get sent to the "localhost" with your auth token. 
- Copy it and paste it, back in cmd, here:
```
token: [your token]
```
- After it, you will probably see this, if you did all right:
```
Successful!
```
You're done!
### Expiring auth tokens
Somewhen your token will be expired, but dont worry you're safe.<br>
You will get message about it and you will proceeded to reauth:
```
Your token has been expired or incorrect.
You will be proceeded to authentication.
```
After that, you will again be able to use tCLI!
### Switching accounts
If you need to logout from your account, and login in different, just type and repeate auth process:
```
tcli auth
```
#### _You need to switch your account on twitch in default browser, before you go to switching in tCLI._<br>
### Deleting your auth data
It stored in your documents folder:
```
C:/Users/[Username]/Documents/tCLI
```
- Delete ".cfg" file.

## Usage
```
tcli [command] [username] [...arguments]
```
Simple `tcli` will show live streams your followings.
### Commands
> Tip: you can see basic version of this, in tCLI itself, by using: `tcli help`.
- `f` sets titles to full
- `auth` for repeating auth process
- `following [from] [to]` returns boolean of check if "from" user is following "to" user
- `follows` returns your follows
  - `[username]` returns follows of that specified username
- `help` returns all avaliable commands
  - `[command]` for specified command
- `link [username]` copies link to the stream of specified streamer, default quality is source
  - `[quality]` you can specify the quality, as in twitch player: 1080p60, 720p60, 720p and etc 
- `live` default, shows up all live streams, that you following
  - `[username]` checks if specified user is live, if yes to returns data about its stream
- `login` returns data about your account
  - `[username]` returns data about specified user
- `vods` returns vods by the time, from your follows
  - `[username]` returns vods of the specified username
  - `f` sets titles to full
# Community
Feel free to post errors, contact me and stuff. You're welcome!
## Credits 
Uses NodeJS and such modules: [`node-fetch`](https://github.com/node-fetch/node-fetch), [`express`](https://expressjs.com/), [`open`](https://www.npmjs.com/package/open), [`twitch-m3u8`](https://github.com/dudik/twitch-m3u8), [`readline`](https://nodejs.org/api/readline.html), [`moment`](https://momentjs.com/), [`copy-paste`](https://github.com/xavi-/node-copy-paste), [`path`](https://nodejs.org/api/path.html), [`os`](https://nodejs.org/api/os.html), [`fs`](https://nodejs.org/api/fs.html).
___
##### License: __MIT__
