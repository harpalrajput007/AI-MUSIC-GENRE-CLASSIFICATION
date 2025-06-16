# 🎶 AI Music Genre Classifier 🎧

An AI-powered web application that predicts the genre of an uploaded music file using machine learning and audio signal processing.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-Web%20Framework-lightgrey)
![License](https://img.shields.io/badge/License-MIT-green.svg)

---

## 📁 Project Structure

```
.
├── app.py                  # Main Flask application
├── utils.py                # Feature extraction logic using Librosa
├── model.pkl               # Trained ML model (e.g., Random Forest)
├── templates/
│   ├── index.html          # Upload form UI
│   └── result.html         # Result display with visualization
├── static/
│   ├── uploads/            # Uploaded audio files
│   └── plots/              # Spectrograms of uploaded audio
├── requirements.txt        # Python dependencies
└── README.md
```

---

## 🧠 Technologies Used

### 🎯 Core Libraries

- `Flask` – Lightweight Python web framework
- `Librosa` – Audio processing and feature extraction
- `Scikit-learn` – Model training and prediction
- `Matplotlib` – Spectrogram plotting

### 🖼 Frontend

- HTML5 + CSS3 (Glassmorphism UI)
- JavaScript (audio visualizer using Canvas API)
- Jinja2 templating (for dynamic HTML)

---

## 🎵 Features Extracted

- MFCCs (Mel-frequency cepstral coefficients): mean & std
- Chroma frequencies: mean & std
- Spectral contrast: mean

---

## 🔍 ML Model

- Model: Trained using scikit-learn (e.g., Random Forest or similar)
- Input: 108-dimensional feature vector from audio
- Output: Predicted genre + Confidence %
- Classes: `['blues', 'classical', 'country', 'disco', 'hiphop', 'jazz', 'metal', 'pop', 'reggae', 'rock']`

---

## 🌐 Web Interface Flow

1. User uploads an audio file
2. Backend extracts features with `utils.py`
3. Model predicts genre and confidence
4. Spectrogram is generated
5. Audio player, genre description, confidence bar & visualization shown in result

---

## 📊 Visualization

- Spectrogram: created using `matplotlib` & `librosa.display`
- Audio Visualizer: Canvas bars synced to audio playback

---

## 📥 Supported Audio Formats

- `.mp3`, `.wav`, `.ogg`, `.flac`

---

## ⚙️ Setup Instructions

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/music-genre-classifier.git
cd music-genre-classifier

# 2. Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # on Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the application
python app.py
```

---

## 🧪 Sample Screenshot

```
[Insert sample UI screenshot here if desired]
```

---

## 📝 License

This project is licensed under the MIT License. Feel free to use, modify, and share!
