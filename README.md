<div align="center">

# 🎮 Steam Deal Bot

### A powerful multi-platform gaming deals Discord bot with a full GUI control panel

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Discord.py](https://img.shields.io/badge/discord.py-2.x-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discordpy.readthedocs.io)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://microsoft.com/windows)

</div>

---

## 📖 About

**Steam Deal Bot** is a Discord bot that automatically hunts for the best gaming deals across multiple platforms and posts them as beautiful rich embeds to your Discord server. Built with Python, it features a sleek **CustomTkinter GUI** so you can configure and control everything without editing any code.

> Never miss a free game or a massive sale again — the bot does the watching for you.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔵 **Steam** | Free games + discounted titles via Steam Store API |
| ⬛ **Epic Games** | Weekly free games + upcoming free game alerts |
| 🟢 **Microsoft Store** | Xbox/PC deals via CheapShark aggregator |
| 🤖 **AI Summaries** | Google Gemini AI-powered deal descriptions |
| 🎮 **Co-op Detection** | Filters deals specifically for co-op games |
| 🛡️ **Smart Filtering** | Min discount %, min rating, min original price |
| 🖼️ **Rich Embeds** | Game art, Metacritic scores, Steam ratings, specs |
| 🔁 **Auto-Scan** | Configurable interval (1h, 6h, 12h, 24h) |
| 📊 **GUI Dashboard** | Start/stop bot, live logs, real-time stats |
| 🚫 **No Duplicates** | Tracks sent deals to prevent repeated posts |
| ⚡ **One-click Launch** | Windows `.bat` launcher with venv support |

---

## 🚀 Getting Started

### Prerequisites

- Python **3.10** or higher
- A Discord Bot Token ([Get one here](https://discord.com/developers/applications))
- A Discord server where you have admin permissions

### Installation

**Option A — Windows One-Click (Recommended)**

```
Double-click run_bot.bat
```

The script will automatically activate a virtual environment, install dependencies, and launch the bot GUI.

---

**Option B — Manual Setup**

**1. Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/steam-deal-bot.git
cd steam-deal-bot
```

**2. Create & activate a virtual environment**
```bash
python -m venv .venv

# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Run the bot**
```bash
python bot.py
```

---

## ⚙️ Configuration

All configuration is done through the **GUI** — no code editing required. Simply:

1. Paste your **Discord Bot Token**
2. Enter your **Channel ID**
3. Select your target **platforms**
4. Set your **deal filters**
5. Hit **Start Bot** 🚀

The settings are saved automatically to `config.json`.

### Config Options

| Setting | Default | Description |
|---|---|---|
| `TOKEN` | `""` | Your Discord Bot Token |
| `CHANNEL_ID` | `""` | Target Discord channel ID |
| `platforms.steam` | `true` | Enable Steam deals |
| `platforms.epic_games` | `true` | Enable Epic Games deals |
| `platforms.microsoft` | `true` | Enable Microsoft Store deals |
| `show_coop_deals` | `true` | Include co-op tagged games |
| `use_ai` | `true` | Enable Gemini AI summaries |
| `min_discount` | `40` | Minimum discount percentage |
| `min_original_price` | `9.99` | Minimum original game price (USD) |
| `min_rating` | `60` | Minimum Steam/Metacritic rating |
| `scan_interval_hours` | `6` | How often to scan for new deals |

---

## 📁 Project Structure

```
steam-deal-bot/
├── bot.py               # 🤖 Main bot logic + GUI (CustomTkinter)
├── config.json          # ⚙️  User configuration
├── requirements.txt     # 📦 Python dependencies
├── run_bot.bat          # ▶️  Windows one-click launcher
├── setup_bot.py         # 🔧 Project scaffold utility
├── sent_deals.json      # 💾 Cache of sent deals (auto-generated)
├── Procfile             # 🚢 Deployment config (Railway/Heroku)
└── assets/              # 🖼️  Bot images and icons
```

---

## 🔌 APIs Used

| API | Purpose | Free? |
|---|---|---|
| [Steam Store API](https://store.steampowered.com/api/) | Featured deals, free games, app details | ✅ Yes |
| [Epic Games Promotions API](https://store-site-backend-official.ak.epicgames.com/) | Weekly free games | ✅ Yes |
| [CheapShark API](https://apidocs.cheapshark.com/) | Multi-store deal aggregation | ✅ Yes |
| [Google Gemini API](https://ai.google.dev/) | AI-powered deal descriptions | ✅ Free tier |

---

## 🛠️ Built With

- **[discord.py](https://discordpy.readthedocs.io/)** — Discord API wrapper
- **[CustomTkinter](https://customtkinter.tomschimansky.com/)** — Modern GUI framework
- **[Pillow](https://pillow.readthedocs.io/)** — Image processing
- **[Requests](https://docs.python-requests.org/)** — HTTP requests

---

## 🔒 Security

> ⚠️ **Important**: Never commit your Discord Bot Token to GitHub!

To keep your token safe:

1. Add `config.json` and `.env` to your `.gitignore`
2. Use environment variables or GitHub Secrets for deployment
3. Regenerate your token immediately if accidentally exposed at [Discord Developer Portal](https://discord.com/developers/applications)

A `.gitignore` template for this project:
```gitignore
# Sensitive config
config.json
.env

# Bot cache
sent_deals.json

# Python
__pycache__/
*.pyc
.venv/
```

---

## 🚢 Deployment

The bot includes a `Procfile` for easy deployment to platforms like **Railway** or **Heroku**:

```
worker: python bot.py
```

For cloud deployment, set your `TOKEN` and `CHANNEL_ID` as environment variables on the platform.

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add amazing feature'`
4. **Push** to the branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 📬 Contact

Have questions or suggestions? Feel free to open an [Issue](../../issues) on GitHub.

---

<div align="center">

**Made with ❤️ by Usif Mohmd**

*If this project helped you, consider giving it a ⭐ star on GitHub!*

</div>
