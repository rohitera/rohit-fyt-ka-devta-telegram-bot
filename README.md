# ROHIT FYT KA DEVTA Telegram Bot

Railway-ready Python deployment for the ROHIT FYT KA DEVTA Telegram bot. The existing attack, media, admin, and utility behavior is preserved while the menu only advertises commands that are registered and available.

## Railway variables

Set `BOT_TOKEN` for one bot, or `BOT_TOKENS` for multiple comma/newline-separated Telegram bot tokens. Set `OWNER_ID` to the owner's numeric Telegram user ID and optionally set `SUDO_IDS` to comma/newline-separated trusted user IDs. `ADMIN_IDS` is accepted as a backwards-compatible alias for `SUDO_IDS`. Only the owner and sudo IDs can use privileged commands. Do not commit tokens. `GITHUB_USERNAME` is optional metadata and is set to `rohitera` in `.env.example`; `GITHUB_TOKEN` is not read or stored by the bot.

The uploaded source previously contained exposed Telegram tokens. Those values were removed from the deployable files; rotate/revoke them in BotFather before using replacement tokens. GitHub tokens must never be committed to this repository.

## Run

```bash
pip install -r requirements.txt
BOT_TOKEN=your_token python3 bot.py
```

Railway uses `railway.json`/`Procfile` and starts `python3 bot.py`.

## Menu and features

The main menu is named **ROHIT FYT KA DEVTA**. It keeps these working sections:

- **Attack** — name changer modes, spam modes, swipe/slide actions, raid NC, game-over action, and stop.
- **Music** — song search and playback.
- **Settings** — speed, NC/spam thread controls, prefix changes, and per-menu media settings.
- **Stop Cmds** — current, global, spam, NC, raid NC, swipe, photo-loop, and bot-exit controls.
- **Admin Ctrl** — owner/sudo-only user management, bot management, status, and thread status.
- **Utility** — group photo save/loop/cleanup and status.
- **Status / Full Help** — live status and the complete registered command list.

## Access behavior

`OWNER_ID` and `SUDO_IDS` are the only IDs allowed to use privileged commands. Other users can browse the normal menu, but a blocked text command receives:

```text
❌ Sirf owner ya sudo user ye command use kar sakta hai.
```

If a non-owner opens **Admin Ctrl**, the button shows:

```text
❌ You are not admin!
```
