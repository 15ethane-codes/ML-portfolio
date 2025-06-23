# Image-to-Speech & Translation

This project extracts text from an image, translates it into another language, and converts it into natural speech. It combines Optical Character Recognition (OCR), translation APIs, and text-to-speech (TTS) synthesis in one pipeline.

## What It Does
- Uploads an image (e.g. handwritten or printed notes)
- Extracts text using `pytesseract` OCR
- Translates the text into a target language (e.g., Spanish)
- Converts both original and translated text into speech using `gTTS`

## Pipeline Steps
1. **Image Upload & Display**  
   User uploads any image with visible text. The image is displayed using `matplotlib`.

2. **Text Detection**  
   Converts the image to grayscale, applies median blurring, and extracts text with `pytesseract`.

3. **Text Translation**  
   Uses `googletrans` to translate the extracted text to a selected language.

4. **Text-to-Speech (TTS)**  
   Converts both the original and translated text to `.mp3` and plays the audio.

## Tech Stack
- Python, Google Colab
- Libraries: `pytesseract`, `opencv`, `Pillow`, `matplotlib`, `googletrans`, `gTTS`, `pyttsx3`

## Features
- Works with printed or handwritten text (has to be clean in pen)
- Supports multiple output languages
- Runs directly in Colab or local notebooks
- Produces real-time spoken audio playback

## Sample Use Case
> Upload a handwritten English note → Extracts text → Translates it into Spanish → Reads it aloud

## Future Improvements
- Add GUI or web interface with file drop support
- Enable language auto-detection
- Add real-time camera capture (e.g. from webcam)
- Option to select different voices, speeds, and TTS engines

Includes full Colab-ready notebook with all dependencies, preprocessing, and audio outputs.
