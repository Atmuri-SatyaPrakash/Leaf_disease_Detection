# 🌿 Leaf Disease Detection System

AI-powered leaf disease detection system with a FastAPI backend and Streamlit web app, using Meta Llama Vision via Groq API for accurate disease identification, severity assessment, and treatment recommendations.

## System Demo

![Leaf Disease Detection Demo](https://github.com/shukur-alom/leaf-diseases-detect/blob/main/Media/video.gif)


**Live Website** - [Leaf disease Detection](https://atmuri-satya-prakash-leaf---disease---detection.streamlit.app/)

## 🎯 Key Features

### 🎯 Core Capabilities
- **Advanced Disease Detection**: 500+ diseases across fungal, bacterial, viral, pests, and nutrient deficiencies.
- **Severity Assessment**: Classifies mild, moderate, severe with confidence scores.
- **Treatment Recommendations**: Evidence-based solutions per disease.
- **Real-time Processing**: Optimized for sub-5-second response times.

### 🏗️ Architecture Components
- **FastAPI (app.py)**: RESTful API service with automatic OpenAPI documentation
- **Streamlit (main.py)**: Interactive web interface with modern UI/UX design
- **Core AI (Leaf Disease/main.py)**: Advanced disease detection engine powered by Meta Llama Vision
- **Utility (utils.py)**: Image processing and data transformation utilities
- **Cloud Deployment**: Production-ready with Vercel integration and scalable architecture

## 🚀 Quick Start Guide

### Prerequisites
- **Python 3.8+** (3.9+ recommended for optimal performance)
- **Groq API Key** ([Get your free key here](https://console.groq.com/))
- **Git** for repository cloning

### 1. Clone & Setup
```bash
git clone https://github.com/Atmuri-SatyaPrakash/leaf-diseases-detect
cd leaf-diseases-detect/Front
python -m venv venv
# Windows
.\venv\Scripts\Activate.ps1
# Linux/macOS
source venv/bin/activate
```

### 2. Install Dependencies
**Install all required packages:**
```bash
pip install -r requirements.txt
```

### 3. Configuration Environment
Create a .env with:
```ini
GROQ_API_KEY=your_groq_api_key
MODEL_NAME=meta-llama/llama-4-scout-17b-16e-instruct
DEFAULT_TEMPERATURE=0.3
DEFAULT_MAX_TOKENS=1024
```

### 4. Launch Application
- **Streamlit**: ```streamlit run main.py --server.port 8501```
- **FastAPI**: ```uvicorn app:app --reload --port 8000```

## 📡 API Endpoints
- **POST /disease-detection-file**: Upload image, returns JSON with disease info, severity, confidence, and treatment.
- **GET /**: API status and available endpoints.

## 🧪 Testing
- **Run tests**: ```python test_api.py```
- **Manual**: Upload images via Streamlit or test API with cURL/Python requests.

## 🌐 Deployment
**Vercel:**
```bash
npm install -g vercel
vercel --prod
```
Set ```GROQ_API_KEY``` in environment variables.

## Performance
- **Response Time**:2-5s
- **Accuracy**: 85-95%
- **Concurrent Requests**: 150+ per minute
- **Image Formats**: JPEG, PNG, WebP, BMP, TIFF

## 🤝 Contributing
- Fork & clone repository
- Create a dev environment, install dependencies (pytest, black, isort, mypy)
- Follow PEP8, type hints, docstrings, unit tests
- Submit PRs for bug fixes, features, UI improvements, performance, and testing
