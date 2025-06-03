# Discord Control Music Bot

---

## 🇬🇧 English

**Play and control music on your Windows PC via Discord!**  
Search, queue, skip, pause, adjust volume, and more—all from your Discord server.

### Features

- Play by name, link, or playlist (YouTube)
- Queue management: add, remove, skip, replay, clear
- Pause/Resume, Stop, Volume control
- Persistent queue/message, tray icon, background mode
- Active channel restriction, interactive Discord UI
- Auto message cleanup, multi-language

---

### 🚀 Installation

**Download:**  
- 👉 [Download the latest release (.zip or .exe)](https://github.com/TorDotTaxi/discord/releases/latest)  
  *(Always use the latest release instead of cloning the repo!)*

**Or build your own .exe:**  
- Install Python 3.11.9 and required modules:
  ```sh
  pip install discord.py yt-dlp py-cord pycaw pystray pillow psutil comtypes pyinstaller
  ```
- Build the bot into a single .exe (recommended for easy use & background mode):
  ```sh
  python -m PyInstaller --onefile --noconsole --icon=icon.png --add-data "icon.png;." main.py
  ```
- Use the generated `main.exe` file to run the bot (no console window, tray icon enabled).

**Or run with Python:**  
  ```sh
  python main.py
  ```

**Install FFmpeg:**  
- Download: https://ffmpeg.org/download.html  
- Extract and add the `bin` folder to your system `PATH`.

**Create Discord Bot & Token:**  
- Go to [Discord Developer Portal](https://discord.com/developers/)
- Create new application > Bot > Reset Token > Save token to `token.json`:
  ```json
  { "BOT_TOKEN": "YOUR_BOT_TOKEN_HERE" }
  ```
- Enable "Message Content Intent" in Bot settings.
- Use OAuth2 URL Generator to invite bot to your server with permissions:
  - Read Messages, Send Messages, Manage Messages

---

### 🕹️ Usage

1. In your chosen Discord channel, type:
   ```
   !activate
   ```
   *(This sets the current channel as the bot's active channel. All commands must be used here.)*
2. Now you can use all features and commands below!

**Basic Commands:**
- `!play <name/link>` – Play song or playlist (add to queue)
- `!p <name/link>` – Alias for `!play`
- `!skip` – Skip current song
- `!stop` – Stop and clear queue
- `!pause` – Pause/Resume
- `!h` – Show help

**Interactive Controls:**
- ➕: Add song
- ⏭️: Skip
- 🛑: Stop
- ⏯️: Pause/Resume
- 🔁: Replay current song
- 🔉 / 🔊: Volume down/up
- 🗑️: Remove song from queue

---

### 💾 Persistence & Tray Icon

- The bot saves the queue and message state to disk. If you close the bot (via tray icon or exit), it will restore the queue/message on next start.
- Tray icon (bottom right of Windows): right-click to save & exit, or exit immediately.

---

### 🛠️ Advanced

- **Background/Tray Mode**: Bot runs in background, no console window.
- **Auto-cleanup**: Bot deletes command messages and invalid messages for a clean channel.
- **Multi-server support**: Each server can have its own queue/message.

---

### ❓ FAQ

- **Q: Does the bot play music in Discord voice channels?**  
  **A:** No, it plays music on your PC and lets you control it via Discord.
- **Q: Can I use Spotify/SoundCloud?**  
  **A:** Only YouTube (video, playlist, search) is supported.
- **Q: How to move the queue message to another channel?**  
  **A:** Delete the old message, use `!activate` in the new channel.

---

### 🧑‍💻 Credits & Support

Bot created by **skilroad**  
- **Facebook**: https://www.facebook.com/xhkvx/
- **Discord**: flashusdt

**Support me:**  
- [Buy Me a Coffee](https://t.me/xhkvx)  
- [MoMo Donation](https://t.me/xhkvx)

---

### 📝 License

MIT License. See [LICENSE](LICENSE) for details.

---
