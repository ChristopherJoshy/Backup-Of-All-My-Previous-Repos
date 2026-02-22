KKNotes Bot
============

A simple Telegram bot (aiogram v3) for browsing and submitting academic resources with MongoDB storage.

Requirements
------------
- Python 3.11+
- Telegram Bot token
- Optional: MongoDB (local or Atlas). If MongoDB is unavailable, the bot falls back to in-memory storage.

Setup
-----
1) Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate
```

2) Install dependencies:

```bash
pip install -r requirements.txt
```

3) Create a .env file in the project root:

```env
# Required
BOT_TOKEN=your_telegram_bot_token

# Optional (defaults shown)
MONGODB_URI=mongodb://0.0.0.0:27017
DATABASE_NAME=kknotes_bot
ADMIN_IDS=1844964834
PENDING_EXPIRY_DAYS=20
```

Run
---
Start the bot:

```bash
python main.py
```

Notes
-----
- Logging writes to stdout and to bot.log.
- Admin panel is available via /admin for user IDs in ADMIN_IDS.
- Pending submissions auto-expire using a TTL index when MongoDB is enabled.

Project structure
-----------------
- `main.py` — entrypoint; starts polling.
- `bot.py` — bot/dispatcher setup and command config.
- `handlers.py` — user flows for browsing and submitting resources.
- `admin.py` — admin review actions (approve/reject, stats).
- `db.py` — MongoDB wrapper with in-memory fallback.
- `config.py` — environment variables and texts.
