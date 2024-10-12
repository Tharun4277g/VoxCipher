# VoxCipher - Python Project

## Overview
**VoxCipher** is a Python-based project that integrates multiple functionalities related to speech processing, Morse code conversion, and language translation. The core of the project revolves around converting audio into text, encoding that text into Morse code, decoding it back to text, and then converting it back into speech. Additionally, the project includes a translation module that translates a given word (e.g., "hello") into various languages and generates speech for the translated word.

### Key Features
1. **Speech to Text**: Converts spoken words from an audio file into text using the `SpeechRecognition` library.
2. **Text to Morse**: Encodes the recognized text into Morse code.
3. **Morse to Text**: Decodes the Morse code back into plain text.
4. **Text to Speech**: Converts the decoded text back into speech using the Google Text-to-Speech (`gTTS`) library.
5. **Language Translation**: Translates the word "hello" into different languages based on user input and converts the translated word into speech.

### Workflow Summary
1. **Speech to Text**: 
   - Input audio is processed to extract speech and convert it to text.
   - The `SpeechRecognition` library is used for this purpose.
   
2. **Text to Morse**:
   - The extracted text is encoded into Morse code using a predefined mapping of characters to Morse symbols.
   
3. **Morse to Text**:
   - The encoded Morse code is decoded back into plain text.

4. **Text to Speech**:
   - The decoded text is converted back into speech using the `gTTS` (Google Text-to-Speech) library.
   - The output speech is saved as an audio file.

5. **Translation and Text-to-Speech**:
   - The word "hello" is translated into a language chosen by the user (e.g., Spanish, French, German, Korean, etc.).
   - The translated text is converted into speech, and the audio output is generated.

## Installation

To use VoxCipher, you need to install the following Python libraries:

```bash
pip install SpeechRecognition
pip install gtts
pip install translate
```

## How to Run

1. **Speech to Text, Morse Code Conversion, and Text-to-Speech Loop**:
   - The project first converts audio input to text using speech recognition.
   - Then, it converts the text into Morse code and back into plain text.
   - Finally, it generates a speech output from the decoded text using `gTTS`.

2. **Language Translation and Text-to-Speech**:
   - The project offers a simple interface where the user can choose a language.
   - The word "hello" is translated to the chosen language, and the translated word is converted into speech using `gTTS`.

## Example Usage

### Speech to Text and Morse Code Loop:

```python
from speech_recognition import Recognizer, AudioFile
from gtts import gTTS
import os

# Recognize speech from audio, convert it to Morse, and back to text
# Finally convert text to speech and save as .wav
```

### Language Translation:

```python
from translate import Translator
from gtts import gTTS

# Translate 'hello' into a selected language and convert it into speech.
```

## Supported Languages for Translation
- **English**
- **Spanish**
- **French**
- **German**
- **Korean**
- **Mandarin**
- **Arabic**
- **Portuguese**
