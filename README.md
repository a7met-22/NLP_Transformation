# ✈️ Project Documentation: Advanced Preprocessing Pipeline

## 📝 Project Overview
This project implements a robust, industry-standard NLP preprocessing pipeline for analyzing customer sentiment in the airline industry. Using the **Twitter Airline Sentiment Dataset**, we transformed raw, noisy social media data into a high-signal corpus ready for Machine Learning modeling.

## 🚀 Key Features
- **Sentiment-Aware Cleaning:** Explicitly preserves negation words (not, no, never) to maintain polarity.
- **Multi-Library Support:** Optimized using `NLTK`, `spaCy`, `emoji`, and `contractions`.
- **Advanced Feature Engineering:** Converts emojis to text (😡 → enraged face) and expands contractions (don't → do not).
- **Validation Suite:** Integrated `unittest` framework to ensure pipeline integrity.

## 🛠️ The 11-Step Preprocessing Pipeline
1.  **Lowercasing:** Standardizes the corpus.
2.  **Noise Removal:** Strips URLs, HTML tags, and Email addresses.
3.  **Social Handle Management:** Removes @mentions while preserving #hashtag keywords.
4.  **Emoji Translation:** Converts icons to descriptive text to capture non-verbal sentiment.
5.  **Contraction Expansion:** Normalizes informal English text.
6.  **Numerical Filtering:** Removes flight numbers and times to reduce overfitting.
7.  **Punctuation Cleaning:** Removes standard and 'smart' Unicode punctuation.
8.  **Tokenization:** Segmenting text into meaningful units.
9.  **Custom Stopword Removal:** Eliminates high-frequency noise while shielding 'Sentiment Signals'.
10. **Lemmatization:** Uses WordNet to find dictionary roots (preferred over Stemming for semantic accuracy).
11. **Final Reconstruction:** Rebuilds tokens into a clean, normalized string.

## 📊 Data Impact & Statistics
| Metric | Before | After | Change |
| :--- | :--- | :--- | :--- |
| **Row Count** | 14,640 | 14,405 | -235 (Duplicates/Empty) |
| **Vocabulary Size** | 30,092 | 10,441 | -65% (Noise Reduction) |
| **Avg. Word Count** | 17.74 | 8.80 | -50% (Optimization) |

## 💡 Key Insights
- **The Signal:** After cleaning, the most frequent words shifted from grammatical noise (the, to, a) to sentiment-rich terms (flight, cancelled, service, thanks).
- **Sentiment Polarity:** Negative reviews were found to be significantly longer and more detailed than positive ones.
- **Dominant Complaints:** "Customer Service Issue" and "Late Flight" were the primary drivers of negative sentiment.

## 📂 File Structure
- `Tweets.csv`: Original raw dataset.
- `clean_airline_reviews.csv`: Final processed dataset for modeling.

---
**Status:** Dataset is verified and 100% ready for Sentiment Analysis modeling.

<img width="1583" height="584" alt="Airline" src="https://github.com/user-attachments/assets/1fe34054-572d-4328-807f-a8713421e205" />
