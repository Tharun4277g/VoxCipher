# VoxCipher
# README for Speech-to-Text, Translation, and Text-to-Speech Converter

## Overview
This project demonstrates a Python-based application that processes speech recognition, translates text into a random language, and converts both the original and translated text into audio files using the Google Text-to-Speech (gTTS) library. The project combines multiple functionalities including:
- Speech recognition from an audio file.
- Translation of recognized text into a randomly selected language.
- Text-to-Speech conversion of both the original and translated text.

## Features
1. **Speech Recognition**: Convert speech from an audio file into text using the `SpeechRecognition` library.
2. **Morse Code Conversion**: Convert the recognized speech to morse code and back to plain text.
3. **Text Translation**: Translate the recognized text into a randomly selected language using the `translate` library.
4. **Text-to-Speech Conversion**: Convert both the original English text and the translated text to speech and save them as `.wav` audio files using the `gTTS` library.

## Libraries Used
- `SpeechRecognition`: For speech-to-text conversion.
- `gTTS`: For converting text to speech.
- `translate`: For translating text into a different language.
- `random`: To randomly select a language for translation.

## Requirements
Make sure the following Python libraries are installed:
```bash
pip install SpeechRecognition
pip install gtts
pip install translate
```

## Usage
1. **Speech Recognition**:
   - Load an audio file and convert the speech in the file to text using the `SpeechRecognition` library.

2. **Morse Code Conversion**:
   - Encode the recognized text into Morse code and decode it back to English.

3. **Text Translation**:
   - Randomly select a language from a list of languages.
   - Translate the recognized text into the selected language using the `translate` library.

4. **Text-to-Speech**:
   - Convert both the recognized English text and the translated text into audio using `gTTS`.
   - Save the audio files in `.wav` format and play them using `IPython.display.Audio`.

## Code Walkthrough
```python
from gtts import gTTS
from IPython.display import Audio
from translate import Translator
import random

# Language assigned for the audio
language = "en"

# Object assigned for converting text to speech
gtts_object = gTTS(text=english_plain_text, lang=language, slow=False)

# Saving the content in the audio file in .wav format
gtts_object.save("/content/gtts.wav")

# Playing the saved audio file
Audio("/content/gtts.wav")

# List of random languages to choose from
languages = ["English", "Spanish", "French", "German", "Russian", "Mandarin", "Arabic", "Portuguese", "Italian"]

# Selecting a random language
random_language = random.choice(languages)
print("Random language:", random_language)

# Creating a translator object for the selected language
translator = Translator(to_lang=random_language)

# Translating the text to the random language
translation = translator.translate(text)
print("The translation of text is:", translation)

# Converting the translated text to speech in a specific language (e.g., Korean)
text_to_say = translation
language = "ko"  # Korean language code

# Creating gTTS object for the translated text
gtts_object = gTTS(text=text_to_say, lang=language, slow=False)

# Saving the translated speech as an audio file
gtts_object.save("/content/gtts.wav")

# Playing the saved audio file
Audio("/content/gtts.wav")
```

## How to Run the Code
1. Ensure you have the required libraries installed.
2. Run the Python script.
3. The script will process an audio file for speech recognition, convert the recognized text into Morse code and back to plain text, translate it into a randomly chosen language, and convert the translated text to speech.

## Notes
- The script processes an audio file containing speech, so ensure that the file is in a format that the `SpeechRecognition` library supports.
- The translation is done into a randomly selected language each time the script is run.
- Both the original and translated texts are converted to speech and saved as `.wav` files.

