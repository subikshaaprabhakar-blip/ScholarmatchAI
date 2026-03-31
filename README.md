# ScholarmatchAI
Smart scholarship recommendation system
# ScholarMatch AI - Setup Instructions

## Project Structure
```
scholarmatch/
├── backend/
│   ├── server.js       ← Main Node.js/Express backend
│   ├── package.json    ← Backend dependencies
│   └── uploads/        ← Created automatically for file uploads
└── frontend/
    ├── index.html      ← Main HTML (entry point)
    ├── css/
    │   └── style.css   ← All styles
    └── js/
        ├── i18n.js     ← Multilingual support (EN/HI/TA)
        └── app.js      ← All frontend logic
```

## Setup & Run

### Step 1: Install Backend Dependencies
```bash
cd scholarmatch/backend
npm install
```

### Step 2: Start the Backend Server
```bash
node server.js
# OR for development:
npx nodemon server.js
```
Server will run at: http://localhost:3001

### Step 3: Open the App
Open your browser and go to: **http://localhost:3001**

## Features Implemented

### ✅ Authentication
- Login/Register with any username & password
- Session persistence

### ✅ 3-Step Profile Form
- Personal Details (name, gender, state, category)
- Academic Details (level, marks, stream, first graduate)
- Financial Details (annual income)
- Edit profile before searching
- "Find Scholarships" button

### ✅ AI Scholarship Matching Engine
- 13 real Indian government scholarships
- Match scoring based on income, marks, category, level, stream, gender
- Gap analysis and improvement suggestions
- Ranked results with match %

### ✅ Fraud Detection
- URL domain analysis (.gov.in = safe, .xyz = risky)
- Keyword pattern detection (fee, lottery, guaranteed)
- Risk scoring (0-100)
- Detailed warnings and positive indicators

### ✅ Document Manager
- Upload documents (PDF, JPG, PNG)
- Document type categorization
- Readiness score based on required docs
- Delete documents

### ✅ Application Tracker
- Add applications to tracker
- Status updates (Applied → Under Review → Approved → Disbursed)
- Timeline visualization
- Add notes

### ✅ AI Chatbot
- Non-intrusive floating button
- Answers questions about scholarships, deadlines, documents, etc.

### ✅ Multilingual Support
- English (EN)
- Hindi (हिंदी)
- Tamil (தமிழ்)
- Full UI translation on toggle

### ✅ Apply Now
- Redirects to official government scholarship portals
- Auto-adds to tracker when applying

### ✅ Deadline Predictor
- Days remaining calculation
- Urgent/Critical deadline flagging
- Dashboard deadline widget

## Scholarship Data
13 verified Indian government scholarships including:
- NSP PM Scholarship
- INSPIRE (DST)
- Post-Matric SC/ST scholarships
- OBC scholarships
- Minority fellowships
- UGC JRF
- AICTE Pragati
- Tamil Nadu CM Scholarship
- And more...

## Tech Stack
- **Frontend**: Vanilla HTML/CSS/JS (no framework, works everywhere)
- **Backend**: Node.js + Express
- **Storage**: In-memory (resets on server restart)
- **File Uploads**: Multer middleware

