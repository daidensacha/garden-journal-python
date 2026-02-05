![](/documentation/images/summer-readme.png)

![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python)
![Flask](https://img.shields.io/badge/Flask-2.0-black?logo=flask)
![HTML5](https://img.shields.io/badge/HTML5-orange?logo=html5)
![CSS3](https://img.shields.io/badge/CSS3-blue?logo=css3)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow?logo=javascript)
![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-green?logo=mongodb)

🌱 Garden Almanac (Flask)

A digital garden journal built with **Python Flask** and a simple **HTML/CSS/JS frontend**.
Users can log entries about their plants, track progress over time, and view a timeline of gardening activity.

---

## 📖 Overview

This project was developed as part of my **Code Institute Full-Stack Diploma (MP3)**.
It focuses on CRUD operations, user inputs, and rendering a timeline-style UI for garden notes.

---

## 🛠 Tech Stack
- 🐍 Python (Flask)
- 🎨 MaterializeCSS
- 🖥 HTML5, CSS, JavaScript
- 🗄 MongoDB (Atlas)

---

## 🚀 Features

- Add, edit, and delete garden entries 🌼
- Timeline view of plant progress
- Search/filter entries
- Responsive layout

---

## 🔧 Installation & Running

### 1. Prerequisites

- Python **3.9+** (recommended: 3.9.x for compatibility)
- pip (Python package manager)
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) connection string

### 2. Clone & Setup

```bash
# Clone the repository
git clone https://github.com/daidensacha/mp3-garden-journal.git
cd mp3-garden-journal

# Create and activate virtual environment
python3.9 -m venv .venv
source .venv/bin/activate   # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### 3. Environment Variables

Create an `env.py` file in the project root (gitignored). Example

```python
import os

os.environ.setdefault("IP", "0.0.0.0")
os.environ.setdefault("PORT", "5000")
os.environ.setdefault("SECRET_KEY", "your-secret-key")
os.environ.setdefault(
    "MONGO_URI",
    "mongodb+srv://<username>:<password>@<cluster>.mongodb.net/garden_master?retryWrites=true&w=majority"
)
os.environ.setdefault("MONGO_DBNAME", "garden_master")
```

### 4. Run the App

```bash
python app.py
#or
flask run
```

The app will start at:
👉 http://127.0.0.1:5000
👉 or http://localhost:5000

---

## 🌿 Project Background

This was my **Milestone Project 3** during the Code Institute diploma.
The goal was to demonstrate **full CRUD functionality**, data persistence, and a user-friendly UI.
It also introduced me to **templating (Jinja2)** and organizing a Python Flask app with routes and models.

---

---

## 📸 Screenshots

Here’s the app in action:

### Home

![](/documentation/images/screenshots/home.jpg)

### Add Plant

![](/documentation/images/screenshots/add_plant.jpg)

### Added Plant

![](/documentation/images/screenshots/added_plant.jpg)

### Added Categories

![](/documentation/images/screenshots/added_categories.jpg)

### Added Event (Folded accordion)

![](/documentation/images/screenshots/added_event1.jpg)

### Added Event (Open accordion)

![](/documentation/images/screenshots/added_event2.jpg)

### User Profile

![](/documentation/images/screenshots/user_profile.jpg)

### Custom 404 Page

![404-page-not-found](/documentation/images/404-page-not-found.jpg)

---

---

## 🔮 Future Improvements

- Add user authentication (login & register)
- Weather API integration for contextual gardening data
- Switch database from SQLite → PostgreSQL for deployment
- Mobile-first redesign with Tailwind CSS

---

## 📜 License

MIT License — feel free to fork and adapt.

![License](https://img.shields.io/github/license/daidensacha/mp3-garden-journal)
![Last Commit](https://img.shields.io/github/last-commit/daidensacha/mp3-garden-journal)
![Open Issues](https://img.shields.io/github/issues/daidensacha/mp3-garden-journal)
![Tech](https://img.shields.io/badge/stack-Python%20%7C%20Flask%20%7C%20MongoDB-blue)

---

> _“A garden is a grand teacher. It teaches patience and careful watchfulness.”_
