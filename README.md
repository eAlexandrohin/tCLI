# tCLI
tCLI - Twitch Command-Line Interface, very simple CLI for the Twitch.
Pronounce like that: "ticly", similar to "tickly" or "tickle".
## Installation
[Download](https://github.com/eAlexandrohin/tCLI/releases), install it and you good to go.
## Auth
Firstly, you need to authenticate.
Just type in cmd:
```
tcli
```

It will automaticly start auth.
- You will get asked for your twitch login, like this, type it and press "Enter":
```
login: [your login here]
```
- After it, tCLI will be opened your default browser and you will need to authorize in the TwitchAPI.
- You will get sent to the "localhost" with your auth token. 
- Copy it and paste it, back in cmd, here:
```
token: [your token]
```
- After it, you will probably see, if you did all right:
```
Successful!
```
You're done!
### Switching accounts
If you need to logout from your account, and login in different, just type and repeate auth process:
```
tcli auth
```
### Deleting your auth data
It stores in program folder:
```
C:/Program Files (x86)/tCLI
```
- Delete ".cfg" file.

## Usage
Simple 
```
tcli
```
will show live streams from your follows.
### Commands
Usage: `tcli [command] [argument]`.
- `help` returns all avaliable commands.
  - `[command]` for specialized command.
- `auth` for repeating auth process.
- `follows` returns your follows.
  - `[username]` returns follows of that username.
- `live` default, shows up all live streams, that you follow.
  - `[broadcaster]` checks if specialized user is live, if yes to returns data about its stream.
- `login` returns data about your account.
  - `[username]` returns data about specialized user.
##### License: MIT
