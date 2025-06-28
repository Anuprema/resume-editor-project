# Resume Editor – Front End Internship Assignment

This is a full-stack web application that allows users to upload, edit, enhance, and download resumes. The frontend is built with React (bootstrapped using Create React App), and the backend is implemented using FastAPI.

---

## Features

- Upload resume files (.pdf or .docx) — parsing is mocked
- Edit sections such as Name, Experience, Education, and Skills
- Enhance individual sections with a mock AI backend
- Save the complete resume to backend
- Download the final resume as a `.json` file

---

## Project Structure

```
resume-editor-project/
├── frontend/           # React app (Create React App)
│   ├── public/
│   └── src/
│       ├── components/
│       └── App.js
├── backend/            # FastAPI app
│   └── main.py         # FastAPI routes and logic
├── README.md           # Project documentation
└── requirements.txt    # Python backend dependencies
```

---

## Frontend Setup (React)

1. Navigate to the frontend folder:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

4. Open the app in your browser at:  
   [http://localhost:3000](http://localhost:3000)

---

## Backend Setup (FastAPI)

1. Navigate to the backend folder:
   ```bash
   cd backend
   ```

2. (Optional) Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate       # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Start the FastAPI server:
   ```bash
   uvicorn main:app --reload
   ```

5. Access the backend at:  
   [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## API Endpoints

### `POST /ai-enhance`

**Request:**
```json
{
  "section": "summary",
  "content": "Experienced developer with a passion for building applications."
}
```

**Response:**
```json
{
  "enhanced": "Highly experienced software developer with a strong passion for delivering scalable and efficient applications."
}
```

---

### `POST /save-resume`

**Request:**
```json
{
  "name": "John Doe",
  "experience": [...],
  "education": [...],
  "skills": [...]
}
```

**Response:**
```json
{
  "message": "Resume saved successfully"
}
```

---

## Feature Checklist

- [x] Upload mock resume file (.pdf/.docx)
- [x] Edit resume fields dynamically
- [x] Enhance sections with "AI" (mocked)
- [x] Save resume via backend
- [x] Download resume as `.json`

---

## Tech Stack

- **Frontend:** React, JavaScript, Axios
- **Backend:** FastAPI, Python, Uvicorn
- **Other Tools:** Create React App

---

##  Notes

- Resume parsing and AI enhancement are mocked for the purpose of this assignment.
- Resume data is stored temporarily in memory or to a file — no database used.

---

## Author

Submitted as part of the Front End Development Internship Assignment – June 2025.
