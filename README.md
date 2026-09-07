# EXPT-5-Speech-Recognition-using-Python

# AIM: 

# To perform and verify speech recognition using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
!pip install SpeechRecognition pydub

import speech_recognition as sr
from pydub import AudioSegment

# Path to uploaded audio file
audio_file_path = '/content/Screen Recording 2026-09-06 170258.wav'

r = sr.Recognizer()

# Load the audio file
with sr.AudioFile(audio_file_path) as source:

    print("Reading audio file...")

    audio = r.record(source)

    print("Attempting to recognize speech...")

    try:
        text = r.recognize_google(audio)

        print("Recognized Text:")
        print(text)

    except sr.UnknownValueError:
        print("Google Speech Recognition could not understand audio")

    except sr.RequestError as e:
        print(f"Could not request results from Google Speech Recognition service; {e}")
```

# OUTPUT: 

<img width="1741" height="260" alt="image" src="https://github.com/user-attachments/assets/1d895008-17be-4e3f-9c72-291e0511a166" />

# RESULT: 
Thus the speech recognition using SCILAB was performed and verified.
