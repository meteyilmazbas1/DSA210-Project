# Gender and Emotion in Song Lyrics

## Motivation    
Music often mirrors human emotions and identities. This project explores whether male and female artists express emotions differently through their lyrics.  
The goal is to find linguistic and emotional patterns that distinguish gender-based songwriting styles.

## Research Questions
1. Do male and female artists differ in average sentiment (positive/negative tone)?
2. Are certain emotions (e.g., joy, sadness, anger) more dominant in one gender's songs?
3. Are there differences in word usage and self-referential language ("I", "me", "my")?

## Data Sources
- **Lyrics Dataset:** [Genius Song Lyrics (Kaggle)](https://www.kaggle.com/datasets/alik05/songlyrics) — contains artist, song title, lyrics, genre, and year.  
- **Artist Gender Dataset:** 
  - [MusicBrainz API](https://musicbrainz.org/doc/MusicBrainz_API) — to fetch artist gender programmatically.  
  - or create a small CSV (`artist_gender.csv`) combining data from Wikipedia / MusicBrainz for 100–200 popular artists.
- Both datasets will be merged on `artist_name` to enrich the lyrics data with gender information.

## Methodology
1. **Data Collection & Cleaning**
   - Load lyrics and gender datasets.
   - Remove duplicates, handle missing data, filter for English lyrics.
   - Normalize artist names and years.
2. **Feature Extraction**
   - Sentiment scores (TextBlob / VADER)
   - Emotion categories (NRC Emotion Lexicon or NRCLex)
   - Lexical features: word count, pronoun ratio, type-token ratio.
3. **Exploratory Data Analysis (EDA)**
   - Compare average sentiment by gender.
   - Visualize emotion distributions (violin plots, bar charts).
   - Conduct statistical tests (t-test / Mann-Whitney / ANOVA).
4. **Machine Learning (Optional)**
   - Binary classification: predict gender based on lyric features.
   - Models: Logistic Regression, Random Forest.
   - Evaluate using ROC-AUC, precision, recall.
5. **Visualization**
   - Emotion distributions per gender.
   - Word clouds for most frequent terms.
   - Feature importance (SHAP or permutation importance).

## Expected Outcomes
- Quantitative evidence of emotional and linguistic differences between male and female artists.  
- Visual insights (charts, word clouds, feature importance).  
- A reproducible Jupyter notebook and documented Python code.

## Tools & Libraries
pandas
numpy
matplotlib
seaborn
nltk
textblob
nrclex
scikit-learn
requests
langdetect
