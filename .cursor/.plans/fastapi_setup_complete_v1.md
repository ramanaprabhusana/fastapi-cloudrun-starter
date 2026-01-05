# FastAPI Setup Complete v1

## Goal
Create a minimal FastAPI API with two GET endpoints:
- /hello returns a casual hello message
- /goodbye returns a casual goodbye message

## Files in this project
- main.py
  - Defines `app = FastAPI()`
  - Implements:
    - GET /hello
    - GET /goodbye
- requirements.txt
  - fastapi==0.104.1
  - uvicorn[standard]==0.24.0
- README.md
  - Local run instructions
  - Endpoint URLs
- Dockerfile
  - Uses python:3.11-slim
  - Installs requirements.txt
  - Runs uvicorn on host 0.0.0.0 and port from $PORT (default 8080)

## Local run steps (macOS)
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
