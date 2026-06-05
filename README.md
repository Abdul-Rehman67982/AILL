# The Game Personal - FastAPI Backend

## Overview
This project contains the FastAPI backend for the game/chat application.

### Tech Stack
- FastAPI
- Uvicorn
- WebSockets
- SQLite
- Railway (deployment)
- Netlify (frontend)

## Project Structure

```text
.
├── main.py
├── requirements.txt
├── chat.db
└── README.md
```

## Local Setup

### 1. Create a virtual environment

```bash
python -m venv .venv
```

### 2. Activate it

Windows:

```bash
.venv\Scripts\activate
```

Linux/Mac:

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the server

```bash
uvicorn main:app --reload
```

## Railway Deployment

Build Command:

```bash
pip install -r requirements.txt
```

Start Command:

```bash
uvicorn main:app --host 0.0.0.0 --port 10000
```

## Frontend Configuration

Backend URL:

```text
https://the-game-persronal-production.up.railway.app
```

WebSocket URL:

```text
wss://the-game-persronal-production.up.railway.app/ws
```

Example:

```javascript
const BASE_URL = "https://the-game-persronal-production.up.railway.app";

const socket = new WebSocket(
  "wss://the-game-persronal-production.up.railway.app/ws"
);
```

## Notes

- Do not upload `.venv` to GitHub.
- Keep all dependencies inside `requirements.txt`.
- Use `.gitignore` to exclude virtual environments and cache files.

Example `.gitignore`:

```text
.venv/
venv/
__pycache__/
*.pyc
```
