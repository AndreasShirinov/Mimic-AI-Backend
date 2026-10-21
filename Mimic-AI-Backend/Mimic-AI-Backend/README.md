# Mimic AI Backend

Backend for Roblox Mimic NPC using Flask + OpenAI API.

Render settings:
- Language: Python 3
- Build Command: `pip install -r requirements.txt`
- Start Command: `gunicorn --bind 0.0.0.0:$PORT app:app`
- Environment:
  - `OPENAI_API_KEY`: your OpenAI API key
  - `MIMIC_BACKEND_TOKEN`: a long random password, also configured as a Roblox Experience Secret
  - `OPENAI_MODEL`: `gpt-4o-mini` (optional)

`GET /` checks server status; `POST /chat` expects a JSON payload with `history` and `context` and an `X-Mimic-Token` header.

Never put actual API keys or tokens in this repository.
