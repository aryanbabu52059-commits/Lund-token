# Auto Token SMS Bot — Railway Deploy Guide

## Step 1 — BOT_TOKEN set karo
`bot.py` line 17 pe apna token daalo:
```
BOT_TOKEN = "your_token_here"
```

## Step 2 — ADMIN_ID set karo
`bot.py` line 18 pe apna Telegram user ID daalo:
```
ADMIN_ID = 123456789
```

## Step 3 — Railway pe deploy

### Option A — GitHub se
```bash
git init
git add .
git commit -m "deploy"
git remote add origin <your-github-repo>
git push -u origin main
```
Railway → New Project → GitHub Repo → select karo → done

### Option B — Railway CLI
```bash
npm install -g @railway/cli
railway login
railway init
railway up
```

## Step 4 — Volume add karo (data save ke liye)
Railway Dashboard → Project → Add Volume → Mount path: `/app`

## Files included
- `bot.py` — main bot
- `requirements.txt` — dependencies
- `Procfile` — Railway worker config
- `runtime.txt` — Python version
- `.gitignore` — unwanted files ignore

## Bot ready hone ka sign
Log mein ye dikhe:
```
🔥 BOT STARTED - VERSION 2.0.4 🔥
```
