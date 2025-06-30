# 🎙️ Voice-to-Text Conversion using Python and Google Speech Recognition API

This project converts spoken words into text using the **Google Speech Recognition API**. It captures voice input through a microphone and transcribes it into readable text in real time using Python.

---

## 🚀 Features

- Real-time speech-to-text transcription  
- Utilizes Google Speech Recognition API  
- Supports English by default (can be configured for other languages)  
- Simple, lightweight, and efficient for command-line usage  

---

## 🛠 Tech Stack

- **Programming Language**: Python 3.x  
- **Libraries**:
  - `speech_recognition`
  - `pyaudio` (for microphone input)
  - `wave` (optional, for saving audio)
- **API**: Google Web Speech API

---

## 📋 How It Works

1. Microphone captures audio input.  
2. Audio is passed to Google's Web Speech API via the `speech_recognition` library.  
3. The recognized text is printed to the console.

---

## ▶️ How to Run

### 🔧 Install Dependencies

```bash
pip install SpeechRecognition
pip install PyAudio
```

> Note: On some systems, you may need to install PyAudio via a wheel file or package manager due to compilation issues.

### ▶️ Run the Script

```bash
python voice_to_text.py
```

Or, if using a notebook:

```python
import speech_recognition as sr

recognizer = sr.Recognizer()
with sr.Microphone() as source:
    print("Listening...")
    audio = recognizer.listen(source)

    try:
        print("Recognizing...")
        text = recognizer.recognize_google(audio)
        print(f"Transcription: {text}")
    except sr.UnknownValueError:
        print("Could not understand the audio")
    except sr.RequestError:
        print("API unavailable or network error")
```

---

## 💡 Use Cases

- Assistive technology for the hearing impaired  
- Voice command interfaces  
- Automated transcription for notes, interviews, meetings

---

## 📈 Future Improvements

- Add support for multiple languages  
- Store audio files for further processing  
- Integrate with a GUI or web app  
- Add noise filtering and keyword detection

---

## 👩‍💻 Developed by

**Tashwita Bhirud**  
B.Tech E&TC + AIML minor | Symbiosis Institute of Technology  

**Chelsi Biloniya**  
B.Tech E&TC + AIML minor | Symbiosis Institute of Technology  

**Nishika Bhayani**  
B.Tech E&TC + AIML minor | Symbiosis Institute of Technology  

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
