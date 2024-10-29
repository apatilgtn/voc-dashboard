# VoC Dashboard Setup Guide

## 1. Project Setup
```bash
# Create project directory
mkdir voc-dashboard
cd voc-dashboard

# Create backend and frontend directories
mkdir backend frontend
```

## 2. Backend Setup
```bash
# Navigate to backend directory
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Create requirements.txt with the content provided above

# Install dependencies
pip install -r requirements.txt

# Create main.py with the backend code provided earlier
```

## 3. Frontend Setup
```bash
# Navigate to frontend directory
cd ../frontend

# Initialize a new React project using Vite
npm create vite@latest . -- --template react

# Install required dependencies
npm install @radix-ui/react-alert-dialog @radix-ui/react-slot class-variance-authority clsx lucide-react react-dom recharts tailwindcss @radix-ui/react-select @radix-ui/react-tabs @radix-ui/react-switch

# Install development dependencies
npm install -D @types/node autoprefixer postcss tailwindcss

# Initialize Tailwind CSS
npx tailwindcss init -p

# Create the component files as provided earlier
```

## 4. Running the Application

### Start the Backend:
```bash
cd backend
# Activate virtual environment if not already activated
python main.py
```
The backend will run on http://localhost:8000

### Start the Frontend:
```bash
cd frontend
npm run dev
```
The frontend will run on http://localhost:5173

## 5. Default Login Credentials
```
Username: admin
Password: admin123
```

## 6. Directory Structure
```
voc-dashboard/
├── backend/
│   ├── venv/
│   ├── main.py
│   ├── requirements.txt
│   └── database.db
└── frontend/
    ├── src/
    │   ├── components/
    │   │   ├── Dashboard.jsx
    │   │   └── LoginForm.jsx
    │   ├── App.jsx
    │   └── main.jsx
    ├── package.json
    └── index.html
```

## 7. Testing the Setup

1. After starting both servers, open http://localhost:5173 in your browser
2. Log in using the default credentials
3. You should see the dashboard with:
   - Sentiment analysis graph
   - Total feedback count
   - Average sentiment score
   - Real-time updates every 30 seconds

## Common Issues and Solutions

1. CORS Issues:
   - Ensure the backend CORS middleware is properly configured
   - Check that the frontend is making requests to the correct backend URL

2. Database Issues:
   - If the database doesn't initialize properly, delete the database.db file and restart the backend

3. Dependencies Issues:
   - If you encounter any module not found errors, try reinstalling the dependencies
   - Ensure you're using the correct versions as specified in requirements.txt

4. Authentication Issues:
   - Clear your browser's local storage if you encounter login problems
   - Ensure the SECRET_KEY in the backend remains consistent

## Next Steps

After basic setup, you can:
1. Add more visualizations
2. Implement data filtering
3. Add user management
4. Enhance security features
5. Add data export functionality
