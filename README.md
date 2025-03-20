# Audio Transcription and Text-to-Speech (TTS) Application

This project provides an interactive web application built with Streamlit, integrating two key functionalities:
1. **Audio Transcription** using Deepgram API.
2. **Text-to-Speech (TTS)** using the Zonos model for speech synthesis.

## Features

### 1. **Audio Transcription with Deepgram**
   - Upload an audio file (e.g., `.wav`, `.mp3`, `.ogg`).
   - Transcribe the audio to text in real-time using the Deepgram API.
   - Support for transcription in Hindi (`hi`).
   - Output transcription text with the ability to download it.

### 2. **Text-to-Speech (TTS) with Zonos**
   - Enter text to be synthesized into speech.
   - Upload a reference audio file to embed a speaker's voice.
   - Select language preferences (English, Spanish, French, etc.).
   - Generate high-quality speech output in a variety of languages.
   - Option to download the generated speech audio.

## Requirements

To run the project, you will need the following dependencies:

- `streamlit==1.18.0`
- `deepgram-sdk==1.0.1`
- `httpx==0.24.0`
- `torch==2.1.0`
- `torchaudio==2.1.0`
- `phonemizer==1.0.0`
- `zonos==0.1.0`

You can install all required dependencies using:

```bash
pip install -r requirements.txt
