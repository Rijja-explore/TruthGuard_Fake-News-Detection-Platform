# 🛡️ TruthGuard - Fake News Detection Platform

![TruthGuard](https://img.shields.io/badge/TruthGuard-AI%20Powered-blue)
![Flask](https://img.shields.io/badge/Flask-3.0+-green)
![Python](https://img.shields.io/badge/Python-3.8+-yellow)
![License](https://img.shields.io/badge/License-MIT-red)

An advanced AI-powered web application for detecting fake news and misinformation using Natural Language Processing (NLP) and Google Gemini AI integration.

## 📋 Table of Contents

- [Features](#features)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Project Milestones](#project-milestones)
- [Technology Presentation](#technology-presentation)
- [Simple Chatbot](#simple-chatbot)
- [API Endpoints](#api-endpoints)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

### 🔍 Core Functionality
- **AI-Powered Analysis**: Integration with Google Gemini AI for advanced content analysis
- **Multi-Source Detection**: Analyze text content and URLs
- **Real-time Processing**: Fast analysis with caching for improved performance
- **Credibility Scoring**: Comprehensive scoring system (0-10 scale)
- **Sensationalism Detection**: Identifies emotional manipulation and clickbait

### 👤 User Management
- **Secure Authentication**: User registration and login with password hashing
- **User Profiles**: Customizable avatars and profile management
- **Analysis History**: Track and review all previous analyses
- **Role-Based Access**: Admin and regular user roles

### 📊 Analytics & Reporting
- **Dashboard**: Comprehensive overview of analysis statistics
- **Visual Charts**: Interactive charts using Chart.js
- **Export Reports**: Download analysis results
- **Monthly Trends**: Track analysis patterns over time

### 💬 AI Chatbot
- **TruthBot Assistant**: Built-in chatbot for user guidance
- **Gemini Integration**: Smart responses using Google AI
- **Fallback System**: Rule-based responses when AI unavailable

### 🎨 Modern UI/UX
- **Responsive Design**: Mobile-first approach with Bootstrap 5
- **Animated Interface**: Smooth animations and transitions
- **Glass Morphism**: Modern design aesthetics
- **Dark/Light Themes**: Beautiful gradient backgrounds

## 🛠️ Technology Stack

### Backend
- **Flask** (3.0+) - Python web framework
- **SQLAlchemy** - ORM for database operations
- **Flask-Login** - User session management
- **Google Generative AI** - Gemini AI integration
- **NLTK** - Natural Language Processing
- **BeautifulSoup4** - Web scraping and parsing
- **Pandas & NumPy** - Data analysis

### Frontend
- **Bootstrap 5** - Responsive UI framework
- **jQuery** - DOM manipulation
- **Chart.js** - Data visualization
- **Font Awesome** - Icon library
- **Animate.css** - CSS animations

### Database
- **SQLite** - Development database
- **PostgreSQL** - Production ready (configurable)

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager
- Virtual environment (recommended)

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/Fake-News-Detection.git
cd Fake-News-Detection/Milestone-4-Complete
```

### Step 2: Create Virtual Environment
```bash
# Windows
python -m venv .venv
.venv\Scripts\activate

# Linux/Mac
python3 -m venv .venv
source .venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Set Up Environment Variables
Create a `.env` file in the `Milestone-4-Complete` directory:
```env
SECRET_KEY=your-secret-key-here
GEMINI_API_KEY=your-gemini-api-key-here
GEMINI_MODEL=gemini-2.5-flash
DATABASE_URL=sqlite:///truthguard.db
FLASK_ENV=development
```

### Step 5: Initialize Database
```bash
python app.py
# Database tables will be created automatically on first run
```

### Step 6: Run the Application
```bash
python app.py
```

The application will be available at `http://localhost:5000`

## ⚙️ Configuration

### Gemini API Setup
1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create or select a project
3. Generate an API key
4. Add the key to your `.env` file

### Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `SECRET_KEY` | Flask secret key for sessions | Random generated |
| `GEMINI_API_KEY` | Google Gemini API key | None |
| `GEMINI_MODEL` | Gemini model version | gemini-2.5-flash |
| `DATABASE_URL` | Database connection string | sqlite:///truthguard.db |
| `FLASK_ENV` | Environment mode | development |
| `MAX_CONTENT_LENGTH` | Max upload size | 16MB |

## 🚀 Usage

### Analyze Content

1. **Text Analysis**
   - Navigate to the Analysis page
   - Paste or type content in the text area
   - Click "Analyze Content"
   - View detailed results

2. **URL Analysis**
   - Enter a news article URL
   - The system will extract and analyze the content
   - Receive comprehensive credibility report

### User Registration
1. Click "Get Started Free"
2. Fill in registration form
3. Verify email (optional)
4. Start analyzing content

### Dashboard
- View total analyses performed
- Check accuracy statistics
- Monitor monthly trends
- Access quick analysis tools

## 📁 Project Structure

```
Fake-News-Detection/
├── README.md                          # Project documentation
├── Explanation/                       # Detailed component explanations
│   ├── admin dashboard explain.docx
│   ├── analyze page.docx
│   ├── analyze route logic.docx
│   ├── appmain.docx
│   ├── Base Template.docx
│   ├── dashboard explaination.docx
│   ├── index.docx
│   └── profile explanation.docx
├── Fake News Tool- Technology PPT/    # Technology presentations
│   ├── Fake News Detection & Verification Tool.pptx
│   └── NLP Technologies.pptx
├── simplechatbot/                     # Chatbot documentation
│   └── Enhanced Chatbot.docx
├── Milestone-1/                       # Basic application setup
│   ├── process/
│   │   ├── app.py
│   │   ├── instance/
│   │   ├── logs/
│   │   └── templates/
├── Milestone-2/                       # Enhanced features
│   ├── process/
│   │   ├── app.py
│   │   ├── instance/
│   │   ├── logs/
│   │   └── templates/
├── Milestone-3/                       # Advanced functionality
│   ├── process/
│   │   ├── app.py
│   │   ├── instance/
│   │   ├── logs/
│   │   └── templates/
└── Milestone-4-Complete/              # Final complete application
    ├── app.py                         # Main application file
    ├── requirements.txt               # Python dependencies
    ├── instance/
    │   └── truthguard.db             # SQLite database
    ├── static/
    │   └── uploads/                  # User uploaded files
    ├── templates/                    # HTML templates
    │   ├── base.html
    │   ├── index.html
    │   ├── login.html
    │   ├── register.html
    │   ├── dashboard.html
    │   ├── analyze.html
    │   ├── profile.html
    │   ├── about.html
    │   ├── contact.html
    │   ├── analysis_detail.html
    │   ├── analysis_history.html
    │   └── admin/
    └── logs/
        └── truthguard.log            # Application logs
```

## � Project Milestones

The project was developed incrementally across four milestones:

### Milestone 1: Foundation
- Basic Flask application setup
- User authentication system
- Simple analysis interface
- Database integration

### Milestone 2: Enhanced Features
- Advanced user dashboard
- Analysis history tracking
- Profile management
- Improved UI/UX

### Milestone 3: Advanced Functionality
- AI integration preparation
- Enhanced analysis capabilities
- Admin panel development
- Performance optimizations

### Milestone 4: Complete Implementation
- Full Google Gemini AI integration
- Comprehensive fake news detection
- Chatbot implementation
- Production-ready features
- Complete admin system

## 📊 Technology Presentation

The `Fake News Tool- Technology PPT/` folder contains detailed presentations about the technologies used:

- **Fake News Detection & Verification Tool.pptx**: Comprehensive overview of the detection methodology and tool capabilities
- **NLP Technologies.pptx**: Deep dive into Natural Language Processing techniques employed

## 🤖 Simple Chatbot

The `simplechatbot/` folder contains documentation for the integrated chatbot system:

- **Enhanced Chatbot.docx**: Detailed explanation of the chatbot architecture, implementation, and integration with the main application

The chatbot provides user assistance and is powered by Google Gemini AI for intelligent responses.

### Public Routes
- `GET /` - Landing page
- `GET /about` - About page
- `POST /register` - User registration
- `POST /login` - User login
- `GET /logout` - User logout

### Protected Routes (Login Required)
- `GET /dashboard` - User dashboard
- `GET /analyze` - Analysis page
- `POST /api/analyze` - Analyze content API
- `GET /profile` - User profile
- `POST /api/chatbot` - Chatbot interaction
- `GET /history` - Analysis history

### Admin Routes
- `GET /admin` - Admin dashboard
- `GET /admin/users` - User management

## 📸 Screenshots

### Landing Page
Modern, gradient-based landing page with animated elements.

### Analysis Interface
Clean, professional interface for content analysis with real-time results.

### Dashboard
Comprehensive analytics dashboard with charts and statistics.

### Profile Page
User profile management with customizable avatars.

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Google Gemini AI for advanced language processing
- NLTK community for NLP tools
- Bootstrap team for the UI framework
- Font Awesome for icons
- Chart.js for data visualization

## 📧 Contact

For questions or support, please open an issue on GitHub.

---

**Made with ❤️ by the TruthGuard Team**