# 🎭 Multimodal Emotion Recognition System (Audio + Text)

A deep learning-based **Multimodal Emotion Recognition (MER)** system that predicts human emotions by combining **speech audio** and **text transcripts**. The model leverages **PyTorch**, **BERT**, and **Bidirectional LSTM** to learn complementary features from both modalities, resulting in improved emotion classification compared to using a single modality.

---

## 📌 Table of Contents

- Overview
- Features
- Model Architecture
- Emotion Classes
- Dataset
- Project Structure
- Installation
- Usage
- Training
- Evaluation
- Results
- Technologies Used
- Future Improvements
- License

---

# 📖 Overview

Emotion Recognition is an important task in Artificial Intelligence with applications in:

- Human-Computer Interaction
- Virtual Assistants
- Healthcare Monitoring
- Customer Sentiment Analysis
- Call Center Analytics
- Education Technology

This project combines:

- **Audio Features**
- **Text Features**

using a multimodal deep learning architecture to improve prediction accuracy.

---

# ✨ Features

- 🎙️ Speech emotion recognition from audio
- 📝 Text emotion recognition using BERT
- 🔀 Audio + Text multimodal feature fusion
- 🧠 Bidirectional LSTM for sequential learning
- ⚖️ Weighted Cross Entropy Loss for handling class imbalance
- 📊 Accuracy, Precision, Recall and F1-score evaluation
- 📈 Confusion Matrix visualization
- 🎤 Real-time emotion prediction using microphone input
- 💾 Save and load trained models

---

# 🧠 Model Architecture

## Audio Branch

Input Audio

↓

Feature Extraction

- MFCC
- Chroma Features
- Mel Spectrogram

↓

Bidirectional LSTM

↓

Dense Layer

↓

Audio Embedding

---

## Text Branch

Input Text

↓

BERT Tokenizer

↓

BERT (bert-base-uncased)

↓

Bidirectional LSTM

↓

Dense Layer

↓

Text Embedding

---

## Multimodal Fusion

```
Audio Embedding
        +
Text Embedding
        ↓
Concatenation
        ↓
Fully Connected Layer
        ↓
Softmax
        ↓
Emotion Prediction
```

---

# 😊 Emotion Classes

The model predicts one of the following emotions:

| Label | Emotion |
|--------|----------|
| 😠 | Angry |
| 😄 | Happy |
| 😢 | Sad |
| 😐 | Neutral |

---

# 📂 Dataset

This project uses the **IEMOCAP (Interactive Emotional Dyadic Motion Capture)** dataset.

The dataset contains:

- Speech audio (.wav)
- Text transcriptions
- Emotion labels

### Dataset Structure

```
IEMOCAP/
│
├── Session1/
├── Session2/
├── Session3/
├── Session4/
└── Session5/
```

> **Note:** IEMOCAP is a licensed dataset and is not included in this repository.

Download from:

https://sail.usc.edu/iemocap/

---

# 📁 Project Structure

```
Multimodal-Emotion-Recognition/
│
├── dataset/
│
├── models/
│   ├── audio_model.py
│   ├── text_model.py
│   └── multimodal_model.py
│
├── preprocessing/
│   ├── audio_features.py
│   ├── text_preprocessing.py
│
├── training/
│   ├── train.py
│
├── evaluation/
│   ├── evaluate.py
│
├── inference/
│   ├── predict.py
│
├── saved_models/
│
├── requirements.txt
│
├── README.md
│
└── main.py
```

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/Multimodal-Emotion-Recognition.git

cd Multimodal-Emotion-Recognition
```

---

## Create Virtual Environment

```bash
python -m venv venv
```

Activate environment

Windows

```bash
venv\Scripts\activate
```

Linux/Mac

```bash
source venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 📦 Requirements

Major libraries used:

```
Python 3.10+

PyTorch

Transformers

Librosa

NumPy

Pandas

Scikit-learn

Matplotlib

Seaborn

TorchAudio
```

---

# 🚀 Usage

## Train the Model

```bash
python train.py
```

---

## Evaluate the Model

```bash
python evaluate.py
```

---

## Predict Emotion

```bash
python predict.py
```

---

## Real-Time Prediction

```bash
python realtime_prediction.py
```

Speak through the microphone to predict emotions in real time.

---

# 📊 Evaluation Metrics

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

Example:

```
Accuracy : 87%

Precision : 0.86

Recall : 0.87

F1 Score : 0.86
```

---

# 🛠️ Technologies Used

| Category | Technology |
|-----------|------------|
| Language | Python |
| Deep Learning | PyTorch |
| NLP | Hugging Face Transformers |
| Text Model | BERT |
| Audio Processing | Librosa |
| Neural Network | Bidirectional LSTM |
| Data Analysis | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Evaluation | Scikit-learn |

---

# 🔬 Audio Features Used

The audio branch extracts:

- MFCC (Mel Frequency Cepstral Coefficients)
- Chroma Features
- Mel Spectrogram

These features capture spectral and frequency characteristics of speech for emotion recognition.

---

# 📝 Text Processing

The text branch uses:

- BERT Tokenizer
- BERT Base Uncased
- Token Embeddings
- Bidirectional LSTM

to capture contextual semantic information from speech transcripts.

---

# 🔀 Multimodal Fusion

Instead of relying on only speech or text, the model combines information from both modalities by concatenating their learned feature embeddings before classification.

This multimodal approach improves robustness and overall prediction accuracy.

---

# 📈 Future Improvements

- Add video-based facial emotion recognition
- Transformer-based fusion network
- Attention-based multimodal fusion
- Deploy as a web application using Flask/Django
- REST API for emotion prediction
- Mobile application integration
- Support additional emotion categories

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push the branch
5. Open a Pull Request

---

# 📜 License

This project is intended for educational and research purposes.

Please ensure compliance with the IEMOCAP dataset licensing terms before using the dataset.

---

# 👨‍💻 Author

**Rajeswari B**

B.Tech Computer Science and Engineering

SASTRA Deemed University

GitHub: https://github.com/yourusername

---

## ⭐ If you found this project useful, consider giving it a star on GitHub!
