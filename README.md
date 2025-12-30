# 📄 AI Resume Analyzer & Job Match System  
A full-stack AI-powered ATS system that analyzes resumes, extracts skills, rates candidate profiles, and matches resumes with job descriptions using LLMs, NLP, and semantic similarity models.

---

## 🚀 Overview

The **AI Resume Analyzer** is a smart ATS-style system that:

- Extracts Skills, Projects, Experience & Education from a resume  
- Generates an AI-powered summary  
- Identifies missing skills & weaknesses  
- Scores the resume out of 100  
- Matches resume with a Job Description (JD)  
- Gives Job Match Score using embeddings (0–100%)  
- Provides actionable improvement suggestions  

This project uses **Google Gemini LLM + FastAPI + Bootstrap** and is perfect for:
- Students preparing for placements  
- HR automation  
- Career portals  
- ML/NLP portfolio showcase  

---

## 🧠 Tech Stack

### **Frontend**
- HTML  
- CSS  
- Bootstrap  
- AOS Animation Library  
- JavaScript  
- Glassmorphism UI  

### **Backend**
- FastAPI  
- Python  
- Uvicorn  
- Google Gemini API  
- pdfplumber  
- python-docx  
- Sentence Transformers  
- NumPy  

---

## 🎨 Features

### 📌 Resume Analysis (LLM-Powered)
- Skill extraction  
- Technical skills detection  
- Experience summarization  
- Project extraction  
- Weaknesses & missing skills  
- Resume scoring  
- AI improvement suggestions  

### 📌 Job Match System
- Upload JD + Resume  
- Calculates similarity using MiniLM Sentence Transformer  
- Generates Job Match Score (%)  
- Identifies matched & missing skills  

### 📌 Modern Attractive UI
- Animated gradient background  
- Glassmorphism cards  
- Smooth fade-in animations  
- Full-screen loader  
- Mobile responsive  

---

## 📁 Project Structure
AI-Resume-Analyzer/
│── backend/
│ │── main.py
│ │── requirements.txt
│ │── utils/
│ │ ├── extract_text.py
│ │ ├── llm_resume.py
│ │ ├── match.py
│ │── uploads/
│
└── frontend/
│── index.html
│── style.css (optional)
│── app.js (optional)


---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/AI-Resume-Analyzer.git
cd AI-Resume-Analyzer/backend
Install Backend Dependencies
pip install -r requirements.txt

```

# 3️⃣ Add Your Gemini API Key

In llm_resume.py:

genai.configure(api_key="YOUR_GEMINI_API_KEY")

# 4️⃣ Run the Backend Server
uvicorn main:app --reload

---

### API Endpoints
## 1.analyze-resume


Upload:

- Resume (PDF / DOCX)

Return:

- Skills

- Projects

- Experience

- Summary

- Rating

- Suggestions

---

## 2. Match Resume with JD
POST /match-job/


Upload:

Resume

JD text file

Return:

Match Score

Matching & missing skill analysis


---

## requirements.txt
- fastapi
- uvicorn
- python-multipart
- pdfplumber
- python-docx
- google-generativeai
- sentence-transformers
- numpy

---

## 🧠 Models Used
LLM

Gemini 2.0 Pro / Flash
Used for:

Skill extraction

Summary generation

Improvement suggestions

Scoring

NLP Model

SentenceTransformer: all-MiniLM-L6-v2
Used for:

JD–Resume semantic similarity

Job match score

---

## 🔧 Deployment Guide
Backend Deployment (Render / Railway)

Push backend folder to GitHub

Create new web service

Add environment variable:

GEMINI_API_KEY = your_key


Start Command:

uvicorn main:app --host 0.0.0.0 --port 10000

Frontend Deployment (Netlify / Vercel)

Upload frontend/ folder

Update backend URL in app.js or inside <script>
