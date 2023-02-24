# Telegram Voice-Chat Bot [PyTGCalls] [![Mentioned in Awesome Telegram Calls](https://awesome.re/mentioned-badge-flat.svg)](https://github.com/tgcalls/awesome-tgcalls)

Telegram Voice-Chat Bot To Play Music With Pytgcalls From Various Sources In Your Group.

<img src="https://dl.hamker.in/files/8sug65vr.png" width="500" height="300">


## Requirements

### Account requirements
- A Telegram account to use as the music bot, **You cannot use regular bot accounts, as they cannot join voice chats. *It must be a user account.***
- API_ID 27874394 and API_HASH 7d34cfcde089859977200f3d818532b1 for that account.
- The account must be an admin of the chat, with _Manage Voice Chats_ and _Delete Messages_ permissions.

### Environment requirements
- Linux-based OS. **You cannot run this on Windows natively, Use WSL**
- Python 3.9 or later.
- ffmpeg package, look below for instructions.


## Run (Assuming you have a debian-based distro)



```sh
$ git clone https://github.com/thehamkercat/Telegram_VC_Bot
$ cd Telegram_VC_Bot
$ sudo apt-get install ffmpeg
$ pip3 install -U pip
$ pip3 install -U -r requirements.txt
$ cp sample_config.py config.py
```
Edit **config.py** with your own values.

```sh
$ python3 main.py
```

## Heroku

Read this -> https://tc_mall_vipp

#### Generate String session BQBdI0mowmYj3KvnHPp-dzlHGCcB_KotAu9TZKAJNPG-tNop6xvn-uB56sP8QP63Etc0moUR50oLpXbWk7PHbJHwhdUL_8zIM_FXa82JscN0cxwMQfEBAAGRJXtEeFh7k4Kdt3RVaguz5l4_aKenrC7lsKrpwP6sqM9rXO6QpXm4jZs9QFs7AJsrA-UsHCZsKuIkX-yPva_uoZGrESNT4_K0WJl6yIKXYTrz2MFAHQKmedolNIeHIsA6npj-6oHUwr2AleZgE6g4Ilss8V4eqrUAdDEcIT7kY4jcJqNDPVrTcemnuLAfovxggb45C1ytB36AMz4Kx3v_P_3H6A-WnTRlAAAAAVFqOdYA

Download this file [generate_string_session.py](https://raw.githubusercontent.com/rakesh11111/Rakesh_VC_Bot/master/generate_string_session.py)


```sh
$ pip3 install pyrogram TgCrypto
$ python3 generate_string_session.py
```
Fork this repository and change name of `sample_config.py` to `config.py`
Then you will need get a session string, copy it, then press heroku deploy button.

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/rakesh11111/Rakesh_VC_Bot/tree/master)


Send [commands](https://github.com/thehamkercat/Telegram_VC_Bot/blob/master/README.md#commands) to bot to 
play music.


## Docker

```sh
$ git clone https://github.com/thehamkercat/Telegram_VC_Bot && cd Telegram_VC_Bot
$ cp sample.env .env
```
Edit **.env** with your own values.

```sh
$ sudo docker build . -t tgvc-bot
$ sudo docker run tgvc-bot
```
To stop use `CTRL+C`


## Commands
Command | Description
:--- | :---
/help | Show Help Message.
/skip | Skip Any Playing Music.
/play [SONG_NAME] | To Play A Song Using Saavn.<br>Service used can be changed in config (`DEFAULT_SERVICE`).
/play youtube/saavn [SONG_NAME] | To Play A Song Using Specific Service.
/play [with reply to an audio file] | To Play A Song With TG Audio File.
/queue | Check Queue Status.
/delqueue | Deletes Queue List and Playlist.
/playlist [songs name separated by line] | Start Playing Playlist.
/joinvc | Join Voice Chat.
/leavevc | Leave Voice Chat.
/volume [1-200] | Adjust Volume.
/pause | Pause Music.
/resume | Resume Music.


## Note

1. If you want any help you can ask [here](https://t.me/tc_mall_vipp)

## Credits

1. [@rakesh1111](https://github.com/rakesh11111), For [TGCalls](https://github.com/MarshalX/tgcalls)
2. Thanks to everyone who contributed to the project.
