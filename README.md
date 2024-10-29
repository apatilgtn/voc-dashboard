# voc-dashboard



# Voice of Customer Dashboard MVP

## Project Structure
```
voc-dashboard/
├── backend/
│   ├── main.py
│   ├── requirements.txt
│   └── database.db
├── frontend/
│   ├── package.json
│   ├── src/
│   │   ├── App.jsx
│   │   ├── components/
│   │   │   ├── Dashboard.jsx
│   │   │   └── LoginForm.jsx
│   │   └── main.jsx
│   └── index.html
└── README.md
```

## Setup Instructions

### 1. Backend Setup
```bash
# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
cd backend
pip install -r requirements.txt

# Run the backend server
python main.py
```

### 2. Frontend Setup
```bash
# Install dependencies
cd frontend
npm install

# Run the development server
npm run dev
```

## Sample Data
To populate the dashboard with initial data, use the provided API endpoints with sample feedback entries.

## Default Credentials
Username: admin
Password: admin123

## Features
- Basic authentication
- Feedback sentiment analysis
- Real-time data updates
- Export functionality
- Basic filtering
