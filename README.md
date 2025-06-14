# aidiary

aidiary is a journaling app I built with Flask to help users reflect on their mental health. It combines basic sentiment analysis with PHQ-9 inspired scoring to give users insights based on what they write in their diary entries.

The goal is to create a simple and private space where people can track how they're doing emotionally, get suggestions based on patterns in their writing, and monitor their wellness over time.

---

## Features

- Secure user registration and login
- PHQ-9-based keyword scanning to detect possible mental health symptoms
- Sentiment analysis using TextBlob
- Custom suggestions and feedback for each entry
- Initial quiz to establish a wellness baseline
- Track progress over time via API (ready for graphing or front-end charting)

---

## Tech Stack

- **Backend**: Python, Flask
- **Frontend**: HTML, CSS
- **Database**: SQLite
- **NLP**: TextBlob, regex-based keyword detection
- **Security**: Password hashing with Werkzeug

---

## How to Run It

1. Clone the repo:

   ```bash
   git clone https://github.com/xzacklin/aidiary.git
   cd aidiary
   ```

2. (Optional) Create a virtual environment:

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Start the app:
   ```bash
   python app.py
   ```

Then just go to `http://localhost:5000` in your browser.

---

##  File Overview

- `app.py`: main app file with route setup
- `auth.py`: handles user auth (register, login, logout)
- `quiz.py`: quiz logic for initial wellness score
- `diary.py`: diary entry creation, sentiment tagging, suggestions
- `helper.py`: keyword matching and sentiment functions
- `db.py`: sets up and connects to the SQLite database
- `templates/`: all the HTML files
- `static/`: CSS and any JS (minimal for now)
- `diary.db`: your local SQLite database

---

## 💡 Future Improvements

- Add chart visualizations of mood trends
- Notification or reminder system
- Mobile layout improvements
- Option to export entries as PDF or CSV
- Use a more advanced NLP model for deeper insights

---

## 📄 License

MIT – use it, tweak it, or build off it.
