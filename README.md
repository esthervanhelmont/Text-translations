# Text-translations
## Text Translation & Sentiment Analysis Using Transformer Models  
By automatically translating text and detecting the emotional tone across multiple languages, this project helps make communication clearer, more inclusive, and easier to analyse at scale.  
This enables faster content understanding in international teams, improves customer-facing workflows, and supports consistent reporting across multilingual datasets.


**Impact:**  
This workflow helps organisations understand multilingual text more quickly — from customer feedback to interviews, support tickets or survey results.  
Concretely, this means companies can respond faster, reduce misunderstandings, and build better data-driven insights across language barriers.

---

## Summary  
This project processes text in different languages using Transformer-based NLP models.  
The workflow includes:

- Detecting the original language  
- Translating the text into English  
- Generating a sentiment score  
- Combining all results into a clean, usable output table  

It supports consistent analysis of multilingual documents and enables insights that would otherwise be hidden behind language differences.

---

## Hypothesis  
We assume that modern Transformer models (e.g., from Hugging Face) can:

1. **Accurately identify the language** of each text entry  
2. **Translate** the content reliably into English  
3. **Analyse sentiment** in a meaningful and consistent way  

If these steps work well together, even complex multilingual datasets can be analysed without manual translation, saving time and improving consistency.

---

## Dataset / Input Info  
- **Source:** Any CSV or text dataset containing multilingual text  
- **Content:** Individual text messages, sentences or paragraphs  
- **Output fields:**  
  - `original_text`  
  - `translated_text`  
  - `sentiment_label` (positive / negative / neutral)  
  - `sentiment_score`  
  - `detected_language`  

---

## Notebook Index  

### **01. Text_Translations_Esther-van-Helmont.ipynb**  
Core functions and workflow:

#### **Language Detection**
- Uses a classification model to predict the original language  
- Adds a new column: `Original Language`  

#### **Translation**
- Uses a transformer-based translation pipeline  
- Translates any non-English text into English  
- Adds a new column: `translated_text`  

#### **Sentiment Analysis**
- Runs a sentiment model to classify emotional tone  
- Adds a new column: `sentiment` and `sentiment_score`  

#### **Batch Processing**
- Processes long lists of texts efficiently  
- Handles missing, short or problematic inputs safely  
- Returns a clean combined output DataFrame  

#### **Output**
- Final dataset includes:  
  - Original text  
  - Detected language  
  - Translated text  
  - Sentiment predictions  
- Ready for export, reporting and further analysis  

---

## Final Results  
The notebook successfully:

- Detects multiple languages  
- Translates text to English with high quality  
- Classifies text sentiment consistently  
- Produces a clean table usable for analytics, dashboards or reports  

This workflow enables large-scale multilingual analysis without manual translation, making it practical for organisations operating across borders or with diverse audiences.

---

## Takeaway  
This project shows how modern NLP can simplify multilingual text analysis.  
By combining language detection, translation and sentiment analysis, you can extract insights from diverse text sources quickly and consistently — even across many languages.
