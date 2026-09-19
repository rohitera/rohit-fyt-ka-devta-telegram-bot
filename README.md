# ROHIT FYT KA DEVTA Telegram Bot

Railway-ready Python deployment for the ROHIT FYT KA DEVTA Telegram bot. The existing attack, media, admin, and utility behavior is preserved while the menu only advertises commands that are registered and available.

## Railway variables

Set `BOT_TOKEN` for one bot, or `BOT_TOKENS` for multiple comma/newline-separated Telegram bot tokens. Do not commit tokens. `GITHUB_USERNAME` is optional metadata and is set to `rohitera` in `.env.example`; `GITHUB_TOKEN` is not read or stored by the bot.

The uploaded source previously contained exposed Telegram tokens. Those values were removed from the deployable files; rotate/revoke them in BotFather before using replacement tokens. GitHub tokens must never be committed to this repository.

## Run

```bash
pip install -r requirements.txt
BOT_TOKEN=your_token python3 bot.py
```

Railway uses `railway.json`/`Procfile` and starts `python3 bot.py`.
