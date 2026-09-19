# Emotion Detector – Final Project

**Repository name:** oaqjp-final-project-emb-ai

**Project name:** Emotion Detector (AI-based web application using Watson NLP and Flask)

An emotion detection web application built as the final project for *Developing AI Applications with Python and Flask*.
The app sends user text to the Watson NLP **EmotionPredict** function and reports the scores for anger, disgust,
fear, joy and sadness together with the dominant emotion.

## Project structure

```
EmotionDetection/
├── __init__.py            # package initialiser, imports emotion_detection
└── emotion_detection.py   # emotion_detector(text_to_analyse) using Watson NLP
server.py                  # Flask web deployment (/ and /emotionDetector)
test_emotion_detection.py  # unit tests for the five emotions
templates/index.html       # web interface
static/mywebscript.js      # calls /emotionDetector from the page
```

## Running

```bash
pip install flask requests pylint
python3 server.py          # http://localhost:5000
python3 -m unittest test_emotion_detection.py
pylint server.py           # 10.00/10
```

Blank input returns HTTP 400 from Watson, which the application maps to `None` values and the
message **Invalid text! Please try again!**.
