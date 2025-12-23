This project implements a Speaker Identification and Speaker Verification system using both Machine Learning (ML) and Deep Learning (DL) approaches. The system analyzes speech signals to identify or verify a speaker based on unique vocal characteristics.

The project follows a complete speech processing pipeline, including dataset creation, automated audio trimming, feature extraction, model training, evaluation, and deployment through a Streamlit web application.
Objectives:-
Develop a reliable speaker identification and verification system
Compare traditional ML models with deep learning models
Implement automated audio preprocessing using TextGrid files
Evaluate performance using accuracy and confusion matrices
Provide a user-friendly web interface for real-time testing
------------------------------------------------------------
Folder Structure
Speaker_ID/
│
├── Dataset/
│   ├── SPEAKER 1/
│   ├── SPEAKER 2/
│   └── ...
│
├── deep_models/
│   ├── extract_ecapa.py
│   ├── extract_xvector.py
│   ├── evaluate_deep_models.py
│
├── models/
│   ├── ml/
│   └── deep/
│
├── results/
│   ├── confusion_matrix_ecapa.png
│   ├── confusion_matrix_xvector.png
│
├── utils.py
├── utils_confusion.py
├── app.py
├── requirements.txt
└── README.md
------------------------------------
Speech Dataset Creation
Number of Speakers: 10 (Male & Female)
Recording Protocol: Same sentence recorded multiple times per speaker
Environment: Controlled indoor conditions
Audio Format: WAV
Sampling Rate: 16 kHz
Channels: Mono
-------------------------------------
Automated Audio Trimming
Audio segmentation using Praat TextGrid files
Python-based parsing of TextGrid annotations
Automatic silence removal and trimming
Generation of clean, speaker-specific WAV files
Manual verification of trimmed audio quality
-------------------------
Feature Extraction
Machine Learning Features
Mel-Frequency Cepstral Coefficients (MFCCs)
Deep Learning Embeddings
ECAPA-TDNN
X-Vector
These embeddings provide fixed-length speaker representations suitable for verification and identification.
---------------------------------------------------
Models Used
Machine Learning Models
Support Vector Machine (SVM)
Random Forest
Gradient Boosting
Deep Learning Models
ECAPA-TDNN (pre-trained)
X-Vector (pre-trained)
ML models are trained using MFCC features, while deep learning models use extracted speaker embeddings.
-----------------------------------------------------------------------
Evaluation Methodology
Speaker Identification
Closed-set identification
Accuracy-based evaluation
Speaker Verification
Genuine vs Impostor trials
Cosine similarity scoring
Threshold-based decision making
2×2 confusion matrix visualization
-----------------------------------------------------------------------
Performance Metrics
Accuracy
Confusion Matrix (True Accept, False Accept, False Reject, True Reject)
ML vs Deep Learning comparison
Computational efficiency analysis
-----------------------------------------------
Web Application
Built using Streamlit
Supports:
Audio upload or recording
ML / Deep Learning model selection
Real-time speaker identification & verification
Visual output of results
--------------------------------------------------


--------------How to Run the Project ---------------
1️. Clone the Repository

git clone https://github.com/your-username/Speaker-Identification-Verification.git
cd Speaker-Identification-Verification

2️. Create Virtual Environment

python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

3. Install Dependencies

pip install -r requirements.txt

4️. Run ML Training

python train_ml_models.py

5. Evaluate Deep Models

python deep_models/evaluate_deep_models.py

6. Launch Web App

streamlit run app.py
