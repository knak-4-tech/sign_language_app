# 📚 Sign Language Detection App

This project uses **FastAPI (Python)** for the backend and **Flutter (Dart)** for the frontend to detect and translate American Sign Language (ASL), British Sign Language (BSL), and Indian Sign Language (ISL).

## 🧩 Project Structure
```
sign_language_app/
├── backend/                             # FastAPI Backend
│   ├── models/                          # Folder to store trained models
│   │   ├── asl_model.h5                 # ASL Model
│   │   ├── bsl_model.h5                 # BSL Model
│   │   └── isl_model.h5                 # ISL Model
│   ├── app.py                           # FastAPI Server Code
│   ├── dockerfile                       # Dockerfile
│   └── requirements.txt                 # Backend Dependencies
├── flutter_app/                         # Flutter App
│   ├── assets/                          # Static assets like images
│   │   └── images/                      # Image files (PNG, JPG, etc.) 
│   │       └── ...
│   ├── test/                            # Unit/widget test files
│   │   └── widget_test.dart
│   ├── lib/                             # Flutter Library
│   │   ├── pages/                       # 
│   │   │   ├── community_page.dart      # Flutter Community Page
│   │   │   ├── detection_page.dart      # Flutter Detection Page
│   │   │   ├── home_page.dart           # Flutter Home Page
│   │   │   ├── learning_page.dart       # Flutter Learning Page
│   │   │   └── login_page.dart          # Flutter Login Page
│   │   ├── widgets/                     # Flutter Widgets
│   │   │   └── ...
│   │   └── main.dart                    # Main Flutter App
│   └── pubspec.yaml                     # Flutter Dependencies, assets, name, etc.
└── README.md                            # Project Documentation
```
## 🚀 Features
- ✅ ASL, BSL, and ISL recognition
- ✅ Real-time Video/Image Processing
- ✅ REST API integration

## 📥 Installation and Setup
### 🔥 Backend Setup
```bash
cd backend
python -m venv venv
source venv\Scripts\activate.bat  # On Windows use: venv\Scripts\activate
# pip install -r requirements.txt
uvicorn app:app --host 0.0.0.0 --port 8000
```
### 📱 Frontend Setup
```bash
cd ../flutter_app
flutter pub get
flutter run
```
## 📡 API Endpoints
- `POST /predict/` - Predicts the sign language

## 📝 Contact
```bash
#### For queries contact 
• Email:    kanak.tech@gmail.com
• Youtube:  https://www.youtube.com/@KNAK-4-tech
• GitHub:   https://github.com/knak-4-tech
• LinkedIn: https://www.linkedin.com/in/knak-4-tech/
• LinkTree: https://linktr.ee/knak_4_tech
```
