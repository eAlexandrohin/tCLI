# tCLI
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
Simple `tcli` will show live streams from your follows.
### Commands
> Tip: you can see this, in tCLI itself, by using: `tcli help`.
- `help` returns all avaliable commands
  - `[command]` for specified command
- `auth` for repeating auth process
- `follows` returns your follows
  - `[username]` returns follows of that specified username
- `live` default, shows up all live streams, that you follow
  - `[broadcaster]` checks if specified user is live, if yes to returns data about its stream
- `login` returns data about your account
  - `[username]` returns data about specified user
## Credits 
Uses NodeJS and such modules: [`node-fetch`](https://github.com/node-fetch/node-fetch), [`express`](https://expressjs.com/), [`open`](https://www.npmjs.com/package/open), [`twitch-m3u8`](https://github.com/dudik/twitch-m3u8), [`clipboardy`](https://www.npmjs.com/package/clipboardy), [`readline`](https://nodejs.org/api/readline.html), [`path`](https://nodejs.org/api/path.html), [`os`](https://nodejs.org/api/os.html), [`fs`](https://nodejs.org/api/fs.html).
___
##### License: __MIT__
