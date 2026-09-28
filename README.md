# FitBuddy - AI Workout Generator

FitBuddy is a fully functioning, AI-powered web application that generates personalized workout plans using **Google Gemini 1.5 Pro** and targeted nutrition/recovery tips using **Google Gemini 1.5 Flash**.

## Features
- **Personalized Workout Generation**: Enter your stats (age, weight, goal, intensity) to receive a highly detailed 7-day workout plan.
- **Nutrition Tips**: AI-generated nutrition tip matching your specific fitness goal.
- **AI Feedback Processing**: Don't like a part of the workout? Submit feedback directly in the UI, and FitBuddy will use AI to tweak and update your plan on the fly.
- **Admin Dashboard**: View all users and their workout plans in a clean, scrollable tabular view.
- **Data Persistence**: Everything is securely saved using an SQLite database with SQLAlchemy ORM.

## Tech Stack
- **Backend Framework**: FastAPI
- **Server**: Uvicorn
- **Language**: Python
- **Frontend**: Jinja2 Templates, HTML, CSS (Custom Design)
- **Database**: SQLite (SQLAlchemy ORM)
- **AI Integration**: Google GenAI API (Gemini-1.5-Pro, Gemini-1.5-Flash)

## Deployment Instructions

To run FitBuddy locally, follow these steps:

### 1. Create a Python Virtual Environment
Open a terminal in the project root and run:
`python -m venv venv`

Activate the virtual environment:
- **Windows**: `venv\Scripts\activate`
- **Mac/Linux**: `source venv/bin/activate`

### 2. Install Requirements
Install dependencies easily via pip:
`pip install -r requirements.txt`

### 3. Add Gemini API Key
Rename `.env.example` to `.env` or create a new `.env` file in the root structure.
Open `.env` and add your Google API Key:
`GOOGLE_API_KEY=your_actual_key_here`

### 4. Run Uvicorn Server
Execute the app with live reload enabled:
`uvicorn app.main:app --reload`

### 5. Access the Application
Open your web browser and navigate to the application using:
[http://127.0.0.1:8000](http://127.0.0.1:8000)

*(FastAPI interactive API docs are also generated automatically at `/docs`)*
