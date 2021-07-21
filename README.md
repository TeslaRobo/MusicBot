# Tesla MusicBot [ Pytgcalls ]

Telegram VoiceChat Bot To Play Music With Pytgcalls From Various Sources In Your Group.

https://user-images.githubusercontent.com/73926361/126449730-b140eb76-6894-48b8-be31-dce95a9d3d15.mp4

## Requirements

### Account requirements
- A Telegram account to use as the music bot, **You cannot use regular bot accounts, as they cannot join voice chats. *It must be a user account.***
- API_ID and API_HASH for that account.
- The account must be an admin of the chat, with _Manage Voice Chats_ and _Delete Messages_ permissions.

### Environment requirements
- Linux-based OS. **You cannot run this on Windows natively, Use WSL**
- Python 3.9 or later.
- ffmpeg package, look below for instructions.

## Run (Assuming you have a debian-based distro)

```sh
$ git clone https://github.com/MadBoy-X/MusicBot
$ cd MusicBot
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

#### Generate String session [IMPORTANT]
- Get it by running [This Repl](https://replit.com/@madboy482/Pyrogram-Session) 
or 
- Download this file [generate_string_session.py](https://raw.githubusercontent.com/MadBoy-X/MusicBot/master/generate_string_session.py) using below commands :

```sh
$ pip3 install pyrogram TgCrypto
$ python3 generate_string_session.py
```
Fork this repository and change name of `sample_config.py` to `config.py`
Then you will need get a session string, copy it, then press heroku deploy button.

[![Deploy To Heroku](https://www.herokucdn.com/deploy/button.svg)](https://dashboard.heroku.com/new?button-url=https%3A%2F%2Fgithub.com%2FMadBoy-X%2FMusicBot&template=https%3A%2F%2Fgithub.com%2FMadBoy-X%2FMusicBot)

Send [Commands](https://github.com/MadBoy-X/MusicBot/blob/master/README.md#commands) to bot to play music.

## Docker

```sh
$ git clone https://github.com/MadBoy-X/MusicBot && cd MusicBot
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
/play [SONG_NAME] | To Play A Song Using YouTube.<br>Service used can be changed in config (`DEFAULT_SERVICE`).
/play youtube/saavn/deezer [SONG_NAME] | To Play A Song Using Specific Service.
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
- If you want any help you can ask [Here](https://t.me/TeslaRobo_Chat)
- 
# Credits 📍
### • MADBOY   »»  <a href="https://github.com/madboy482" alt="MadBoy"> <img src="https://img.shields.io/badge/MADBOY-30302f?logo=github" /></a>
### • PRANAV   »»  <a href="https://github.com/Pranav18262" alt="Pranav"> <img src="https://img.shields.io/badge/PRANAV-625D5D?logo=github" /></a>

## Special Thanks to :
- [Telegram_VC_Bot](https://github.com/TheHamkerCat/Telegram_VC_Bot)
- @MarshalX [For TgCalls]
