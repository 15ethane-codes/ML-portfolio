# Emotion-Based Music Recommender

A machine learning project that recommends songs based on user emotions. Users type how they feel, and the system outputs personalized song suggestions, combining NLP, AI, and music curation.

---

## Features
- Detects six emotions: **Joy, Sadness, Anger, Fear, Surprise, Love**
- User-friendly input: natural language sentences (*“How do I feel?”*)
- Recommends curated playlists for each emotion
- Built using **BERT-based emotion classifier** (`bhadresh-savani/bert-base-uncased-emotion`)
- Interactive demo via **Gradio**
- Optionally integrates with Spotify dataset for additional song info

---

## How It Works
1. **User Input:** User types a sentence describing their mood/input their mood.
   e.g., `"I feel happy and excited today!"`
2. **Emotion Detection:** BERT-based classifier predicts one of six emotions
3. **Song Recommendation:** System selects 5 songs from the corresponding playlist or Spotify dataset
4. **Display:** Returns the detected emotion and recommended songs to the user

---

## Example Inputs & Outputs

| Emotion   | Example User Input                          | Sample Recommended Songs             |
|-----------|--------------------------------------------|-------------------------------------|
| Joy       | “I feel lighthearted and full of energy.”  | “Happy - Pharrell Williams”, …      |
| Sadness   | “I feel down and need something gentle.”   | “Someone Like You - Adele”, …       |
| Anger     | “I’m frustrated and want to let off steam.”| “Break Stuff - Limp Bizkit”, …      |
| Fear      | “I feel nervous and need something calming.”| “Everybody’s Got To Learn Sometime - Beck”, … |
| Surprise  | “I’m amazed and want something exciting.”  | “A Sky Full of Stars - Coldplay”, …|
| Love      | “I feel affectionate and want romantic music.” | “All of Me - John Legend”, …     |


![image_alt](https://github.com/15ethane-codes/ML-portfolio/blob/761997f7fe6131d1827edc932b9f87fc11f155a6/Screenshot%20(6).png)

![image_alt](https://github.com/15ethane-codes/ML-portfolio/blob/761997f7fe6131d1827edc932b9f87fc11f155a6/Screenshot%20(7).png)
---

## Future Improvements

- Add more emotions or mood subcategories.
- Integrate Spotify API for real time streaming.
- Include Grad-CAM or attention visualizaitons on input text
- Build a web app interface for easier interaction
