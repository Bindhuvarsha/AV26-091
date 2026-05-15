# Jeeva Raksha - AI-Powered Medical Assistant

An intelligent healthcare application that combines AI-powered symptom analysis, hospital finder, and medical chat functionality.

## 🏗️ Project Structure

```
jeeva-raksha/
├── frontend/           # React Frontend Application
│   ├── src/           # React source code
│   ├── public/        # Static assets
│   ├── package.json   # Frontend dependencies
│   └── vite.config.js # Vite configuration
├── backend/           # Python FastAPI Backend
│   ├── server.py      # Main FastAPI application
│   ├── config.py      # Application configuration
│   ├── requirements.txt # Python dependencies
│   └── *.py          # Backend services
├── database/          # Database and Data Files
│   ├── data_set.csv  # Medical dataset
│   ├── symptoms_dataset.csv # Symptoms data
│   └── database.py   # Database operations
├── testing/           # Test Files and Scripts
├── development/       # Documentation and Dev Tools
│   ├── docs/         # Documentation files
│   ├── scripts/      # Setup and utility scripts
│   └── docker/       # Containerization files
└── README.md         # This file
```

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ and npm
- Python 3.8+
- Git

### Installation

1. **Clone and setup:**
   ```bash
   git clone <repository-url>
   cd jeeva-raksha
   npm run install:all
   ```

2. **Configure environment variables:**
   - Copy `.env.example` to `.env.local` in frontend/
   - Copy `.env.example` to `.env` in backend/
   - Add your API keys (OpenAI, Google Maps, Firebase)

3. **Start development servers:**
   ```bash
   npm run dev  # Starts both frontend and backend
   ```

   Or run separately:
   ```bash
   npm run dev:frontend  # React app on http://localhost:5173
   npm run dev:backend   # FastAPI on http://localhost:8000
   ```

## 📁 Directory Details

### Frontend (`/frontend`)
- **Framework:** React 18 with Vite
- **Styling:** Tailwind CSS
- **Features:** Responsive UI, routing, API integration

### Backend (`/backend`)
- **Framework:** FastAPI (Python)
- **Features:** REST API, AI integration, hospital search
- **Services:** OpenAI, Google Maps, Firebase

### Database (`/database`)
- **Data:** CSV datasets for medical information
- **Storage:** Firebase Firestore integration
- **Operations:** User data management

### Testing (`/testing`)
- **Unit tests:** Component and API tests
- **Integration tests:** End-to-end testing
- **Test data:** Mock data for testing

### Development (`/development`)
- **Documentation:** Setup guides, API docs
- **Scripts:** Automation and utility scripts
- **Docker:** Containerization setup

## 🔧 Development Commands

```bash
# Install all dependencies
npm run install:all

# Start development (both frontend & backend)
npm run dev

# Build frontend for production
npm run build:frontend

# Run tests
npm run test

# Lint code
npm run lint
```

## 🌐 API Endpoints

- `GET /` - API information
- `POST /analyze-symptoms` - AI symptom analysis
- `POST /similar-diseases` - Find similar diseases
- `GET /nearby-hospitals` - Hospital search
- `GET /medical-info/{disease}` - Disease information
- `POST /chat` - AI medical chat

## 🔑 Environment Variables

### Frontend (`.env.local`)
```
VITE_API_URL=http://localhost:8000
VITE_GOOGLE_MAPS_API_KEY=your_google_maps_key
VITE_FIREBASE_API_KEY=your_firebase_key
# ... other Firebase config
```

### Backend (`.env`)
```
OPENAI_API_KEY=your_openai_key
GOOGLE_MAPS_API_KEY=your_google_maps_key
FIREBASE_PROJECT_ID=your_firebase_project
FIREBASE_CREDENTIALS_PATH=../database/firebase-credentials.json
```

## 🐳 Docker Support

Build and run with Docker:
```bash
docker-compose -f development/docker-compose.yml up --build
```

## 📚 Documentation

- [Setup Guide](development/SETUP.md)
- [API Integration](development/API_INTEGRATION.md)
- [Quick Start](development/QUICK_START.md)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests
5. Submit a pull request

## 📄 License

MIT License - see LICENSE file for details