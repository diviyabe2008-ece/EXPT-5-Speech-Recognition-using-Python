# EXPT-5-Speech-Recognition-using-Python

# AIM: 

  To perform and verify speech recognition using Python .

# APPARATUS REQUIRED: 

PC installed with SCILAB. 

# PROGRAM: 
```
!pip install SpeechRecognition pydub

import speech_recognition as sr
from pydub import AudioSegment
from pydub.silence import split_on_silence

# Path to your audio file (upload this file to Colab's /content/ folder first)
audio_file_path = '/content/dtsp_audio.wav'

r = sr.Recognizer()

# Load the audio file
with sr.AudioFile(audio_file_path) as source:
    print("Reading audio file...")
    audio = r.record(source)  # read the entire audio file

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
<img width="1600" height="377" alt="image" src="https://github.com/user-attachments/assets/96950461-b47d-4e26-a89b-2409dd621444" />



# RESULT: 
Thus the speech recognition using SCILAB was performed and verified.
