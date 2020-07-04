
<h1 align="center">Telegram Torrent Leecher 🔥</h1> 

<p align="center">
<a href="https://img.shields.io/github/issues/sawankumar/Telegram-Leech-Bot"><img alt="issues" src="https://img.shields.io/github/issues/sawankumar/Torrent-Leech-Bot"/></a>
<a href="https://img.shields.io/github/license/sawankumar/Telegram-Leech-Bot"><img alt="license" src="https://img.shields.io/github/license/sawankumar/Torrent-Leech-Bot"/></a>
<a href="https://sawankumar.gitlab.io/"><img alt="author" src="https://img.shields.io/badge/author-Sawan%20Kumar-red"/></a>
<a href="https://www.python.org/"><img alt="language" src="https://img.shields.io/badge/Made%20with-Python-1f425f.svg"/></a>
<a href="https://github.com/ellerbrock/open-source-badges/"><img alt="author" src="https://badges.frapsoft.com/os/v1/open-source.svg?v=103"/></a>
</p>

<hr>

> ## A Telegram Torrent (and youtube-dl) Leecher based on [Pyrogram](https://github.com/pyrogram/pyrogram)

# Features :-
    🔥 Mirror torrent to cloud storage.
    🔥 Support Drive/Teamdrive and all other cloud services that rclone.org supports.
	🔥 Mirror files from direct links.
	🔥 Upload file to Telegram.
	🔥 Make an archive and upload it to either Telegram or Cloud Storage.
	🔥 Mirror Telegram files to Cloud Storage.
	🔥 Get total size of your working cloud directory
	🔥 Custom file name
	🔥 Custom commands
    🔥 Unzip
    🔥 Unrar
    🔥 Untar


## Installing

### The Easy Way

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

### The Legacy Way
Simply clone the repository and run the main file:

```sh
git clone https://github.com/SpEcHiDe/PublicLeech.git
cd PublicLeech
virtualenv -p /usr/bin/python3 venv
. ./venv/bin/activate
pip install -r requirements.txt
# <Create config.py appropriately>
python3 -m tobrot
```

### An example of config.py 👇
```py
from tobrot.sample_config import Config

class Config(Config):
  TG_BOT_TOKEN = ""
  APP_ID = 6
  API_HASH = "eb06d4abfb49dc3eeb1aeb98ae0f581e"
  AUTH_CHANNEL = -1001234567890
```

### Variable Explanations :-

##### Mandatory Variables

* `TG_BOT_TOKEN`: Create a bot using [@BotFather](https://telegram.dog/BotFather), and get the Telegram API token.

* `APP_ID`
* `API_HASH`: Get these two values from [my.telegram.org/apps](https://my.telegram.org/apps).
  * N.B.: if Telegram is blocked by your ISP, try our [Telegram bot](https://telegram.dog/UseTGXBot) to get the IDs.

* `AUTH_CHANNEL`: Create a Super Group in Telegram, add `@GoogleIMGBot` to the group, and send /id in the chat, to get this value.

* `RCLONE_CONFIG`: Create the rclone config using the rclone.org and read the rclone section for the next.

* `DESTINATION_FOLDER`: Name of your folder in ur respective drive where you want to upload the files using the bot.

##### Set Rclone

1. Set Rclone locally by following the official repo : https://rclone.org/docs/
2. Get your `rclone.conf` file.
will look like this
```
[NAME]
type = 
scope =
token =
client_id = 
client_secret = 

```
3. Only copy the config of drive u want to upload file.
4. Copy the entries of `rclone.conf` 
5. Your copied config should look like this:
 ```
type = 
scope =
token =
client_id = 
client_secret = 

and everythin except `[NAME]`

```

6. Paste copied config in `RCLONE_CONFIG`

7. Hit deploy button.

</p>

##### Optional Variables

* `DOWNLOAD_LOCATION`

* `MAX_FILE_SIZE`

* `TG_MAX_FILE_SIZE`

* `FREE_USER_MAX_FILE_SIZE`

* `MAX_TG_SPLIT_FILE_SIZE`

* `CHUNK_SIZE`

* `MAX_MESSAGE_LENGTH`

* `PROCESS_MAX_TIMEOUT`

* `ARIA_TWO_STARTED_PORT`

* `EDIT_SLEEP_TIME_OUT`

* `MAX_TIME_TO_WAIT_FOR_TORRENTS_TO_START`

* `FINISHED_PROGRESS_STR`

* `UN_FINISHED_PROGRESS_STR`

* `TG_OFFENSIVE_API`

* `CUSTOM_FILE_NAME`

* `LEECH_COMMAND`

* `YTDL_COMMAND`

* `TELEGRAM_LEECH_COMMAND_G`

* `INDEX_LINK`: (Without `/` at last of the link, otherwise u will get error) During creating index, plz fill `Default Root ID` with the id of your `DESTINATION_FOLDER` after creating. Otherwise index will not work properly.
## Available Commands

* `/ytdl`: This command should be used as reply to a [supported link](https://ytdl-org.github.io/youtube-dl/supportedsites.html)

* `/leech`: This command should be used as reply to a magnet link, a torrent link, or a direct link. [this command will SPAM the chat and send the downloads a seperate files, if there is more than one file, in the specified torrent]

* `/leech archive`: This command should be used as reply to a magnet link, a torrent link, or a direct link. [This command will create a .tar.gz file of the output directory, and send the files in the chat, splited into PARTS of 1024MiB each, due to Telegram limitations]

* `/gleech`: This command should be used as reply to a magnet link, a torrent link, or a direct link. And this will download the files from the given link or torrent and will upload to the drive using rclone.

* `/gleech archive` This command will compress the folder/file and will upload to your google drive.

* `/leech unzip`: This will unzip the .zip file and dupload to telegram.

* `/gleech unzip`: This will unzip the .zip file and upload to drive.

* `/leech unrar`: This will unrar the .rar file and dupload to telegram.

* `/gleech unrar`: This will unrar the .rar file and upload to drive.

* `/leech untar`: This will untar the .tar file and upload to telegram.

* `/gleech untar`: This will untar the .tar file and upload to drive.

* `/tleech`: This will mirror the telegram files to ur respective cloud drive.

* `/tleech unzip`: This will unzip the .zip telegram file and upload to drive.

* `/tleech unrar`: This will unrar the .rar telegram file and upload to drive.

* `/tleech untar`: This will untar the .tar telegram file and upload to drive.

## FAQ

* [Only work with direct link for now] It is like u can add custom name as prefix of the original file name.
Like if your file name is `gk.txt` uploaded will be what u add in `CUSTOM_FILE_NAME` + `gk.txt`

Only works with direct link.No magnet or torrent.

And also added custom name like...

You have to pass link as 
`www.download.me/gk.txt | new.txt`

The file will be uploaded as `new.txt`.


## How to Use?

* Send any one of the available command, as a reply to a valid link.

* Files Larger than 1500MB are splitted into parts, and uploaded to Telegram group. To join the files, Download all the parted files, place them in the same directory.
  
  👉 Windows < 10 Users: 
  
  `Extract the contents of Hl-join.zip into the directory where splited parts of a file are placed, and run the the join32.exe to join the files.`
  
  `Hl-join.zip Location : This repository/hl-join/hl-join.zip`
  
  👉 GNU/Linux Users: 
  
  `cat filename.00001 filename.00002 filename.00003 > filename`
   Replace filename in the above command, as required.
  
* If you got a file.tar.gz from the bot:

  👉 Windown 10 Users : 
  
  `Install [7-zip](https://www.7-zip.org/download.html)`
  
  `Extract the .tar.gz file.`
  
  👉 GNU/Linux users : 
  
  `Just right click and select "Extract Here" if you use Ubuntu.`


## Thanks to :heart:

* Gautamajay52 for his [TorrentLeech-Gdrive](https://github.com/gautamajay52)
* SpEcHiDe for his [Public Leech](https://github.com/SpEcHiDe/PublicLeech)
* Dan Tès for his [Pyrogram Library](https://github.com/pyrogram/pyrogram)
* Robots for their [UploadBot](https://telegram.dog/UploadBot)
* AjeeshNair for his [torrent.ajee.sh](https://torrent.ajee.sh)
* And gotstc, aryanvikash and HasibulKabir.

