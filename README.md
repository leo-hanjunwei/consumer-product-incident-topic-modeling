# BERTopic Modeling on Consumer Product Incident Narratives

**Author:** Hanjun Wei  
**Organization:** UL Standards and Engagement – Data Science Team  
---

## 📘 Project Overview

This project applies **BERTopic**, a state-of-the-art Natural Language Processing (NLP) technique, to analyze consumer product incident narratives collected from **U.S. CPSC** and **Health Canada**. By uncovering hidden topics within these narratives, the study aims to surface meaningful patterns, evaluate their alignment with structured data, and understand their evolution over time.

Narratives, although flexible and rich in context, present challenges for large-scale analysis. This project demonstrates how modern NLP can bridge that gap.

---

## 📁 Project Structure

```
project/
│
├── data_consolidation/     # Scripts and outputs related to merging US & Canadian datasets
├── preprocessing/          # Data cleaning, language filtering, tokenization, lemmatization
├── topic_modeling/         # BERTopic model building, optimization, topic naming
├── topic_comparison/       # Comparison with LDA and BTM, structured data comparison
└── Report.pdf              # Full project report detailing methods, findings, and visualizations
```

---

## 🔍 Key Components

### 1. **Data Sources**
- **CPSC National Injury Information Clearinghouse** (USA)
- **Health Canada Consumer Product Incidents System**

### 2. **Preprocessing**
- Removal of redacted content and meaningless text fragments
- Language filtering (only English narratives retained)
- Tokenization, lemmatization, bigrams/trigrams
- Stopword and symbol removal

### 3. **BERTopic Modeling**
- Utilized **BERT + UMAP + HDBSCAN + c-TF-IDF**
- Identified **42 distinct topics**
- Determined optimal topic number using **NPMI coherence score**
- Dynamic topic modeling to capture topic evolution over time

### 4. **Topic Analysis**
- Manual topic naming based on keyword representation
- Hierarchical clustering to understand topic similarity
- Dynamic analysis shows rise in topics like "Mobility" and "Skin Rash"

### 5. **Comparison with Structured Data**
- Product types, hazards, injuries, and severity matched to topic trends
- Validation of topic meaning and evolution through structured variables

---

## 📊 Key Findings

- BERTopic outperformed traditional models (LDA, BTM) in coherence.
- Dynamic topic modeling revealed real-world product trends (e.g., rise of scooters, Fitbit rashes).
- BERTopic uncovered implicit similarities between products and conditions not evident in structured data.
- Topics can act as a bridge to unify structured and unstructured perspectives.

---

## 📄 How to Use

Each folder corresponds to a major pipeline step. To replicate or extend the analysis:
1. Start from `data_consolidation/` to merge and format the raw datasets.
2. Proceed to `preprocessing/` for narrative cleaning.
3. Use `topic_modeling/` to run the topic models.
4. In `topic_comparison/`, you'll find model benchmarking and structured data alignment analysis.

All final insights, visualizations, and narrative explanations are compiled in `Report.pdf`.

---

## 🧠 Final Thoughts

Narrative data carries untapped insight. With BERTopic, we gain scalable interpretability over complex reports. This project not only showcases the technical power of modern NLP, but also emphasizes its practical value in consumer product safety and regulatory domains.
