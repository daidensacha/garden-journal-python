# Garden Journal (Python Flask)

A digital garden journal built with **Python Flask** and a simple **HTML / CSS / JavaScript frontend**.
Users can log entries about their plants, track progress over time, and view a timeline of gardening activity.

---

## 📖 Overview

This project was developed as part of my **Code Institute Full‑Stack Diploma (Milestone Project 3)**.
It focuses on CRUD operations, user input handling, MongoDB data modeling, and server‑rendered templates using Jinja.

The repository contains historical documentation from the original submission as well as a cleaned‑up, modernized setup guide for local development.

---

## 🛠 Tech Stack

- 🐍 Python 3.9 (original target)
- 🌶 Flask 2.x
- 🗄 MongoDB (Atlas)
- 🎨 MaterializeCSS
- 🖥 HTML5, CSS3, JavaScript
- 🧩 Jinja2 Templates

---

## 🚀 Features

- Add, edit, and delete garden entries 🌱
- Timeline view of plant progress
- Category‑based organization
- Search and filtering
- Responsive UI

---

## 🔧 Local Development Setup

### 1. Prerequisites

- Python **3.9.x** (recommended for current compatibility)
- pip
- MongoDB Atlas account

### 2. Clone & Setup

```bash
git clone https://github.com/daidensacha/mp3-garden-journal.git
cd mp3-garden-journal

python3.9 -m venv .venv
source .venv/bin/activate

pip install -r requirements.txt
```

---

## 🔐 Environment Variables

You may choose **either** a local `env.py` file **or** Phase for secret management.

### Option A — env.py (classic)

Create an `env.py` file in the project root (gitignored):

```python
import os

os.environ.setdefault("IP", "0.0.0.0")
os.environ.setdefault("PORT", "5000")
os.environ.setdefault("SECRET_KEY", "your-secret-key")
os.environ.setdefault(
    "MONGO_URI",
    "mongodb+srv://<user>:<pass>@<cluster>.mongodb.net/garden_master"
)
os.environ.setdefault("MONGO_DBNAME", "garden_master")
```

Ensure `env.py` is listed in `.gitignore`.

---

### Option B — Phase (recommended)

Store secrets using Phase:

```bash
phase secrets set SECRET_KEY
phase secrets set MONGO_URI
phase secrets set MONGO_DBNAME
```

Run the app with injected secrets:

```bash
phase run "python app.py"
```

Phase replaces `env.py` entirely and is safer for long‑term maintenance.

---

## ▶️ Running the App

```bash
python app.py
```

The app will be available at:

- http://127.0.0.1:5000
- http://localhost:5000

---

## 🔮 Upgrade Path (Recommended)

This project is stable but based on an older stack.
To extend its lifespan, follow this incremental upgrade path.

### Step 1 — Python

Current:
- Python 3.9

Upgrade path:
- Python 3.11 (recommended next step)
- Python 3.13 (later, once dependencies support it)

Actions:
- Create a fresh virtual environment per version
- Resolve deprecations and warnings
- Re‑freeze dependencies

---

### Step 2 — Dependencies

- Upgrade Flask incrementally (2.x → latest 2.x)
- Review breaking changes in:
  - Flask
  - Werkzeug
  - Jinja2
- Replace deprecated APIs
- Pin versions explicitly in `requirements.txt`

---

### Step 3 — Flask Modernization (Optional)

- Migrate to application factory pattern
- Introduce `flask run` with `.flaskenv`
- Replace `env.py` with Phase or `.env`
- Add type hints and linting

---

### Step 4 — Architecture Improvements (Optional)

- Blueprint separation
- Service layer for MongoDB logic
- Switch MaterializeCSS → Tailwind
- Add authentication via Flask‑Login or migrate to Django / Next.js backend

---

## 📁 Documentation

- `README_OLD.md` — original submission documentation
- `/documentation/` — testing, UX, schema, and screenshots
- This README — cleaned, current development guide

---

## 📜 License

MIT License — feel free to fork, study, and adapt.

---

> _“A garden is a grand teacher. It teaches patience and careful watchfulness.”_
