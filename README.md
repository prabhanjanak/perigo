Here is your improved `README.md` file with clear instructions on usage, input/output, environment variables, and cross-platform compatibility:  

---

# **Audio Transcription and Text-to-Speech (TTS) Application**  

This project is a **Streamlit-based web application** that integrates:  
1. **Audio Transcription** using Deepgram API  
2. **Text-to-Speech (TTS)** using the Zonos model for speech synthesis  

The application is compatible with **Windows, Linux, and macOS** and supports **multiple languages** for transcription and synthesis.  

## **Features**  

### **1. Audio Transcription with Deepgram**  
✅ Upload an audio file (`.wav`, `.mp3`, `.ogg`).  
✅ Transcribe speech to text in real-time using Deepgram.  
✅ Supports **Hindi (`hi`)** and other languages.  
✅ Download transcription as a `.txt` file.  

### **2. Text-to-Speech (TTS) with Zonos**  
✅ Enter text to convert into speech.  
✅ Upload a reference audio file to generate voice embeddings.  
✅ Choose a language for synthesis (English, Spanish, French, etc.).  
✅ Generate high-quality speech with **voice cloning**.  
✅ Download generated speech as a `.wav` file.  

---

## **Installation Guide**  

### **1. Clone the Repository**  
```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### **2. Create a Virtual Environment**  
```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate      # Windows
```

### **3. Install Dependencies**  
```bash
pip install -r requirements.txt
```

---

## **Configuration: Setting Up Environment Variables**  

Before running the app, create a `.env` file in the project root directory and add the following:  

```plaintext
DEEPGRAM_API_KEY=<your-deepgram-api-key>
ESPEAK_KEY=<your-espeak-key>
TTS_ASSET_PATH=<path-to-store-audio-files>
```

- `DEEPGRAM_API_KEY`: Get this from [Deepgram's website](https://deepgram.com/) after signing up.  
- `ESPEAK_KEY`: Obtain this after signing up on the eSpeak website.  
- `TTS_ASSET_PATH`: Specify a directory where generated audio files will be saved.  

Example:  
```plaintext
DEEPGRAM_API_KEY=abc123xyz
ESPEAK_KEY=eskey123
TTS_ASSET_PATH=/home/user/tts_output
```

On Windows, use:  
```plaintext
TTS_ASSET_PATH=C:\Users\YourName\tts_output
```

---

## **How It Works**  

### **Audio Transcription**  
1. Upload an audio file (`.wav`, `.mp3`, `.ogg`).  
2. The app sends the file to Deepgram for transcription.  
3. The transcribed text is displayed on the screen.  
4. Download the transcription as a `.txt` file.  

### **Text-to-Speech (TTS)**  
1. Enter text in the provided text box.  
2. Upload an optional **reference voice** for speaker embedding.  
3. Choose a language (English, French, Spanish, etc.).  
4. Click **"Generate Speech"** to synthesize speech using Zonos.  
5. Download the generated `.wav` file.  

---

## **Running the Application**  

After setting up everything, **run the Streamlit app**:  

```bash
streamlit run app.py
```

---

## **Platform-Specific Notes**  

### **Windows**  
- Install `espeak-ng` manually from [this link](https://espeak-ng.org/download.html).  
- Modify the `.env` file paths accordingly (e.g., `C:\path\to\folder`).  

### **Linux (Ubuntu/Debian)**  
- Install eSpeak:  
  ```bash
  sudo apt update && sudo apt install espeak-ng libespeak-ng-dev
  ```
- Ensure correct permissions for `TTS_ASSET_PATH`.  

### **MacOS**  
- Install eSpeak using Homebrew:  
  ```bash
  brew install espeak-ng
  ```

---

## **Output File Locations**  

| Feature         | Output File Type | Save Location |
|----------------|----------------|--------------|
| Transcription  | `.txt`          | Downloaded directly |
| TTS Audio      | `.wav`          | Saved in `TTS_ASSET_PATH` |

---

## **License**  
This project is licensed under the MIT License.  

---
