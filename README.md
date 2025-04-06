# 📚 Sign Language Detection App

This project uses **FastAPI (Python)** for the backend and **Flutter (Dart)** for the frontend to detect and translate American Sign Language (ASL), British Sign Language (BSL), and Indian Sign Language (ISL).

## 🤟 Real-Time Sign Language Detection using Transformer and MediaPipe

This project detects and classifies American Sign Language (ASL) alphabet signs using image or real-time video input, powered by a Transformer model and Google's MediaPipe library.

## 🧩 Project Structure

```
sign_language_app/
├── backend/                                         # FastAPI Backend
│   ├── app.py                                       # FastAPI Server Code
│   ├── config.json                                  # Model, dataset, and feature config
│   ├── dockerfile                                   # Dockerfile
│   ├── main.py                                      # Real-time webcam inference
│   ├── models/                                      # Folder to store trained models
│   │   ├── asl_transformer.pth                      # Trained model (generated after training)
│   │   │   └── dataset/                             # ASL sign folders
│   │   │       └── A, B, C...                       # Images folder
│   │   │           └── img1.jpg, img2.jpg, ...
│   │   ├── bsl_transformer.pth                      # Trained model (generated after training)
│   │   └── isl_transformer.pth                      # Trained model (generated after training)
│   ├── preprocessing.py                             # Image-based landmark extraction and tensor saving
│   ├── training.py                                  # Transformer model training logic
│   └── ...                                          # Future development
├── flutter_app/                                     # Flutter App
│   ├── android/                                     # Android devices specification
│   ├── assets/                                      # Static assets like images
│   │   └── images/                                  # Image files (PNG, JPG, etc.)
│   │       └── ...
│   ├── build/                                       # Stores auto generated build files created during app compilation
│   ├── ios/                                         # IOS devices specification
│   ├── lib/                                         # Flutter Library
│   │   ├── main.dart                                # Main Flutter App
│   │   ├── pages/
│   │   │   ├── community_page.dart                  # Flutter Community Page
│   │   │   ├── detection_page.dart                  # Flutter Detection Page
│   │   │   ├── home_page.dart                       # Flutter Home Page
│   │   │   ├── learning_page.dart                   # Flutter Learning Page
│   │   │   └── login_page.dart                      # Flutter Login Page
│   │   └── widgets/                                 # Flutter Widgets
│   │       └── ...
│   ├── pubspec.yaml                                 # Flutter Dependencies, assets, name, etc.
│   ├── test/                                        # Unit/widget test files
│   │   └── widgÄet_test.dart
│   └── windows/                                     # Contains platform-specific code
│       └── runner/                                  # build-in file for specific system
├── README.md                                        # Overview of reprojectory
├── requirements.txt                                 # Backend Dependencies
└── venv/                                            # Python virtual environment directory
```

## 🚀 Features

- ✅ ASL, BSL, and ISL recognition
- ✅ Real-time Video/Image Processing
- ✅ REST API integration
- ✅ Real-time webcam ASL recognition
- ✅ Static image landmark processing using MediaPipe Holistic
- ✅ Transformer-based architecture for classification
- ✅ Dataset preprocessing & normalization
- ✅ Config-driven pipeline

## 📥 Installation and Setup

### 🔥 Backend Setup

#### Clone the repository:
```bash
git  clone  https://github.com/your-username/sign_language_app.git
cd  sign_language_app
```

#### Create a Python virtual environment (Windows):
```bash
cd  backend
python  -m  venv  venv
venv\Scripts\activate.bat
```

#### Install dependencies:
```bash
pip  install  -r  requirements.txt
```

#### Host the file
```bash
uvicorn  app:app  --host  0.0.0.0  --port  8000
```

### 📱 Frontend Setup
```bash
cd  ../flutter_app
flutter  pub  get
flutter  run
```

### 🛠 Configuration
Edit the `config.json` file to update:
```json
{
"input_dim": 2580,
"d_model": 128,
"nhead": 4,
"num_encoder_layers": 3,
"vocab_size": 26,
"num_landmarks": 860,
"asl_alphabet_dir": "dataset/"
}
```

### 🧼 Preprocessing
To preprocess image data and generate training tensors:
```bash
python preprocessing.py
```
This creates a `preprocessed_data.pt` file.

### 🏋️‍♀️ Training
Train the ASL Transformer model:
```bash
python training.py
```
The trained model will be saved to `models/asl_transformer.pth`.

## 📹 Real-Time Inference
Run the real-time ASL recognition (webcam must be available):
```bash
python  main.py
```
Press `Q` to quit the video stream window.

## 📋 Requirements
- Python 3.8+
- MediaPipe
- OpenCV
- PyTorch
- NumPy
- scikit-learn

## 📡 API Endpoints
-  `POST /predict/` - Predicts the sign language

## 🙌 Acknowledgements
- [MediaPipe](https://google.github.io/mediapipe/)
- [ASL Alphabet Dataset](https://www.kaggle.com/datasets/grassknoted/asl-alphabet)

## 🧠 Future Improvements
- Word-level or sentence-level recognition
- GUI or mobile app integration (Flutter front-end)
- Support for BSL/ISL

## 📝 Contact

#### **For queries contact**
```bash
•  Email:  kanak.tech@gmail.com
•  Youtube:  https://www.youtube.com/@KNAK-4-tech
•  GitHub:  https://github.com/knak-4-tech
•  LinkedIn:  https://www.linkedin.com/in/knak-4-tech/
•  LinkTree:  https://linktr.ee/knak_4_tech
```