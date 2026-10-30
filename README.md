# 📚 CameraBot: Smart Classroom Assistant

A deep learning project that combines real-time object detection with a voice-controlled AI chatbot. A webcam feed is analyzed with YOLOv5, while you can talk to a local LLM through your microphone.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![YOLOv5](https://img.shields.io/badge/YOLOv5-00FFFF)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-Mistral-000000)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)

## ✨ Features

- **Live object detection**: webcam frames run through YOLOv5s (`yolov5s.pt`), on GPU when available
- **Voice input**: records from the microphone and transcribes it with Google Speech Recognition
- **Local AI chatbot**: answers with the Mistral model running in [Ollama](https://ollama.com/), keeping the conversation history

## 📂 Files

| File | Description |
|---|---|
| `main (1).py` | Streamlit version: camera feed on the left, chatbot on the right |
| `Temp_Try.py` | Desktop version built with PyQt5, with background threads for audio and video |
| `gpt.py` | Command-line chatbot using Ollama |
| `yolov5s.pt` | Pretrained YOLOv5 small weights |
| `CameraBot.pptx` | Project presentation |

## 🚀 Getting Started

1. Install [Ollama](https://ollama.com/) and pull the model:

   ```bash
   ollama pull mistral
   ```

2. Install the Python dependencies:

   ```bash
   pip install torch opencv-python yolov5 ollama sounddevice numpy SpeechRecognition streamlit PyQt5
   ```

3. Run the version you want:

   ```bash
   streamlit run "main (1).py"     # web app
   python Temp_Try.py              # desktop app
   python gpt.py                   # terminal chatbot
   ```

A webcam and microphone are required for the camera and voice features.
