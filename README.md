aidiary
aidiary is a mental wellness journaling app built with Flask. It lets users log daily reflections, automatically analyzes their mood using a PHQ-9-inspired scoring system, and generates custom insights based on natural language processing.

It’s designed to help people reflect on their emotional patterns over time — kind of like a smart diary that knows what you’re going through and nudges you with helpful prompts.

What It Does
Secure Login/Register System – Users can create accounts, log in, and log out.

PHQ-9 Based Mood Scoring – Each diary entry is analyzed for emotional keywords and tone.

Sentiment Analysis – Uses TextBlob to detect how positive or negative the entry is.

Wellness Score – Blends sentiment and symptom weight to track a user’s mental health over time.

Custom Tips – Based on detected symptoms (like sleep or energy issues), the app suggests thoughtful next steps.

Quiz-First Flow – Users take a short quiz on first login to establish their initial wellness baseline.

Progress Visualization – Entries are timestamped and tracked for future graphing (API-ready).

Tech Stack
Backend: Python (Flask), SQLite

Frontend: Jinja2 templates (HTML), basic CSS

NLP Tools: TextBlob, Regex, Custom PHQ-9 Keyword Matching

User Management: Werkzeug Security for password hashing

Other: JavaScript (minimal), Chart.js-compatible API for progress

Getting Started
Clone this repo
git clone https://github.com/xzacklin/aidiary.git && cd aidiary

(Optional) Create a virtual environment
python3 -m venv venv && source venv/bin/activate
(Windows: venv\Scripts\activate)

Install dependencies
pip install -r requirements.txt

Run it
python app.py
Visit http://localhost:5000 in your browser.

File Breakdown
app.py – Entry point that ties everything together

auth.py – Register, login, logout logic

quiz.py – First-time wellness quiz

diary.py – Core journal logic + sentiment + suggestions

helper.py – NLP/AI logic: scoring, tagging, tips

db.py – SQLite init and connection helpers

templates/ – All HTML views

static/ – CSS and potential JS

diary.db – Prepped SQLite DB (auto-generated if missing)

Future Ideas
Add charts to visualize wellness trends over time

Token-based reminders or streaks

AI summarizer for monthly mood trends

Fully offline mode with localStorage sync

License
MIT – Feel free to build on this.
