# 📤 Telegram TXT to Video Uploader Bot

A powerful **Pyrogram-based Telegram Bot** that reads video links from TXT files, downloads them, and uploads them directly to Telegram with support for queues, batches, progress bars, resumable processing, and multiple video sources.

---

# ✨ Features

* 📂 Upload videos from TXT files
* 🎥 Supports direct MP4 links
* 📺 Supports M3U8 playlists
* 🔐 Supports DRM workflows (if configured)
* 🚀 Fast Telegram uploads
* 📊 Real-time download & upload progress
* 📁 Batch processing
* ⏸ Resume processing after interruptions
* 👤 Multi-user support
* 🛡 Admin-only commands
* ⚡ Async architecture using Pyrogram
* 📡 Works on VPS, Railway, Render and local machines

---

# 📦 Requirements

* Python 3.10 or newer
* FFmpeg installed and added to PATH
* Telegram API ID
* Telegram API Hash
* Telegram Bot Token

Python dependencies:

```text
aiofiles
aiohttp
beautifulsoup4
cloudscraper
m3u8
pycryptodome
pyrogram
pyromod
python-dotenv
pytube
pytz
requests
TgCrypto
yt-dlp
```

Install:

```bash
pip install -r requirements.txt
```

---

# 🔧 Create Telegram Application

Visit:

https://my.telegram.org

Login with your phone number.

Navigate to:

API Development Tools

Create a new application and copy:

* API_ID
* API_HASH

---

# 🤖 Create Bot

Open Telegram.

Search:

@BotFather

Run:

```
/newbot
```

Follow the instructions and copy your Bot Token.

---

# ⚙ Configuration

Create a `.env` file.

Example:

```env
API_ID=12345678
API_HASH=0123456789abcdef0123456789abcdef

BOT_TOKEN=123456:ABCDEFxxxxxxxxxxxxxxxx

OWNER_ID=123456789

LOG_CHANNEL=-1001234567890

DATABASE=users.json

DOWNLOAD_DIR=downloads

TEMP_DIR=temp
```

If your project uses `config.py`, edit the variables there instead.

---

# 📁 Project Structure

```
Bot/
│
├── bot.py
├── main.py
├── config.py
├── requirements.txt
├── .env
├── downloads/
├── temp/
├── logs/
└── modules/
```

(The exact structure may vary depending on your fork.)

---

# ▶ Running Locally

```bash
git clone <repository>

cd forked_Txt-to-video-uploader

pip install -r requirements.txt

python main.py
```

or

```bash
python bot.py
```

depending on the project entry point.

---

# 📤 How to Use

## Step 1

Start the bot.

```
/start
```

---

## Step 2

Upload a TXT file containing video URLs.

Example:

```
https://example.com/video1.mp4

https://example.com/video2.mp4

https://example.com/video3.m3u8
```

One URL per line.

---

## Step 3

The bot automatically:

* Reads every link
* Downloads the video
* Uploads it to Telegram
* Deletes temporary files
* Continues with the next link

---

# 📜 Supported Links

* MP4
* M3U8
* Direct HTTP video links
* Some streaming services (depending on implementation)
* yt-dlp supported websites

---

# 👤 Admin Commands

Typical commands include:

```
/start
/help
/users
/broadcast
/stats
/restart
/ping
```

Available commands depend on your configuration.

---

# 📊 Progress Display

The bot shows:

* Download speed
* Upload speed
* ETA
* Percentage
* Downloaded size
* Uploaded size

---

# 📂 Queue System

Supports multiple files.

Features:

* Sequential uploads
* Batch processing
* Automatic cleanup
* Error recovery

---

# 🚀 Deployment

## Railway

1. Create a Railway project.
2. Upload repository.
3. Add environment variables.
4. Deploy.

---

## Render

1. Create a Background Worker.
2. Connect GitHub repository.
3. Add environment variables.
4. Deploy.

---

## VPS

Ubuntu example:

```bash
sudo apt update

sudo apt install ffmpeg

git clone <repository>

cd forked_Txt-to-video-uploader

python3 -m venv venv

source venv/bin/activate

pip install -r requirements.txt

python main.py
```

---

# 🪟 Windows

Install:

* Python
* FFmpeg

Run:

```bash
pip install -r requirements.txt

python main.py
```

---

# 🐧 Linux

```bash
sudo apt install ffmpeg

pip install -r requirements.txt

python main.py
```

---

# 🛠 Troubleshooting

## TgCrypto Missing

```bash
pip install TgCrypto
```

---

## FFmpeg Not Found

Install FFmpeg and ensure it is available in your system PATH.

---

## FloodWait Error

Telegram rate-limited the bot.

Wait for the required duration before retrying.

---

## Peer ID Invalid

Ensure:

* Bot is added to the chat/channel.
* Bot has admin permissions.
* Chat ID is correct.

---

## Invalid API_ID

Verify your API credentials from:

https://my.telegram.org

---

## Login Failed

Check:

* Bot Token
* API_ID
* API_HASH

---

# ❤️ Credits

* Pyrogram
* Pyromod
* yt-dlp
* FFmpeg
* Telegram Bot API

---

# ⚠ Disclaimer

This project is intended for educational and personal use only.

Users are responsible for complying with the Terms of Service of any websites they interact with and for respecting applicable copyright laws.

---

# ⭐ Support

If you find this project useful:

⭐ Star the repository.

🐞 Report issues via GitHub Issues.

💡 Contributions and pull requests are welcome.

---

## License

Use, modify and distribute according to the repository's license.
