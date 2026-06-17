# 🎭 Multimodal Emotion Recognition System (Audio + Text)

A deep learning-based multimodal emotion recognition system that detects human emotions using both speech audio and text. Built using PyTorch, BERT, and LSTM on the IEMOCAP dataset.

---

## 🚀 Features

- 🎙️ Audio emotion recognition using MFCC, Chroma, Mel Spectrogram
- 📝 Text emotion analysis using BERT (bert-base-uncased)
- 🔗 Multimodal fusion (Audio + Text)
- 📊 Accuracy, Classification Report, Confusion Matrix
- 🎧 Real-time emotion prediction using microphone
- ⚖️ Handles class imbalance using weighted loss

---

## 🧠 Model Architecture

### Audio Branch
- MFCC + Chroma + Mel Spectrogram features
- Bidirectional LSTM (128 hidden units)

### Text Branch
- BERT encoder
- LSTM layer for sequential representation

### Fusion Layer
- Concatenation of audio + text features
- Fully connected layer → 4 emotion classes

---

## 🎯 Emotion Classes

- Angry 😠
- Happy 😄
- Sad 😢
- Neutral 😐

---

## 📁 Dataset

IEMOCAP Dataset is used:
- Audio (.wav)
- Transcriptions
- Emotion labels

Dataset path:
