# Efficient Text Analysis of Blogs: Clustering and Classification Techniques for Content Insights

## 📌 Introduction
Natural Language Processing (NLP) plays a pivotal role in machine learning and data science, enabling the computational analysis of human language. With the explosion of user-generated content such as blogs and social media, extracting meaningful insights from large volumes of unstructured text has become increasingly important.

This project analyzes blog posts sourced from the **Blog Authorship Corpus**, which contains over **681,000 posts** from **19,320 authors**, totaling **140M+ words**. To manage computational complexity, a **subset of 10,000 posts** was selected.  
The key objective is to apply **clustering** and **classification** techniques to:
- Group similar blog posts.
- Predict demographic attributes (e.g., gender).
- Generate insights for content organization, recommendation, and analysis.

---

## 🎯 Problem Statement and Justification
Unstructured blog text poses challenges for analysis and organization. This project addresses:
- How to cluster blog posts into meaningful groups.
- How to classify author demographics (gender) from text.  

The analysis supports applications in **content recommendation, topic modeling, and targeted insights**, helping improve the organization and usability of large-scale text data.

---

## ✅ Assumptions and Scope
- Dataset is pre-cleaned (minimal noise, irrelevant content removed).
- Traditional clustering methods (KMeans, Affinity Propagation, Hierarchical) are applicable.
- Hierarchical clustering is useful for visualizing text group relationships.
- Scope: **Text clustering + gender classification** from blog content.

---

## 🛠️ Data Preprocessing
Key preprocessing steps:
- **Text normalization** (lowercasing, punctuation removal).
- **Tokenization** (splitting into words).
- **Stopword removal** (removing uninformative words).
- **Lemmatization** (reducing words to base form).

---

## 📊 Exploratory Data Analysis (EDA)
- Substantial variation in word usage and post lengths.  
- **Frequent words**: “time”, “one”, “know”, “think”, “people”.  
- Word clouds provided early thematic insights.  

---

## 🤖 Machine Learning Approach

### 🔹 Classification Models (Gender Prediction)
| Model                   | Accuracy | AUC  |
|--------------------------|----------|------|
| Support Vector Machine   | **Best** | 0.89 |
| Logistic Regression      | 80.95%   | -    |
| Naive Bayes              | 80.75%   | -    |
| Ridge Classifier         | 81.20%   | -    |
| Random Forest            | 77.75%   | -    |
| K-Nearest Neighbors      | 60.35%   | -    |

- **SVM** achieved the best results, showing strong discrimination with AUC = 0.89.  
- Misclassifications mostly involved **female posts predicted as male**.

### 🔹 Clustering Methods
- **KMeans**: Balanced, interpretable clusters with distinct keywords.
- **Affinity Propagation**: Produced variable cluster sizes, sometimes unstable.
- **Hierarchical Clustering**: Effective for **visualizing relationships** between clusters.

Representative cluster reviews revealed **themes and sentiments** in author behaviors.

---

## 📚 Related Works
- **Text Clustering Survey** – Overview of clustering algorithms (KMeans, Hierarchical, LDA).  
- **Demographic Adaptation in Text Classification** – Use of demographic attributes (e.g., gender/age) to improve classification.  
- **Pre-Trained Models + Autoencoders** – Improved clustering using SentenceBERT and deep learning approaches.  

---

## 🚧 Research Gaps
- Limited to **traditional clustering/classification** methods.  
- Could improve with:
  - **SentenceBERT / Transformers** for embeddings.
  - **Deep embedded clustering** for scalability.
  - **Robust evaluation metrics** for clustering interpretability.  

---

## 📂 Data Description
Dataset: **Blog Authorship Corpus (2004)**  

| Column  | Description                        | Unique Values | Top Values (Count)         |
|---------|------------------------------------|---------------|-----------------------------|
| id      | User identifier                    | 214           | 589736 (2294), 883178 (1616)|
| gender  | Gender of user                     | 2             | male (5916), female (4084) |
| age     | Age of user                        | 24            | 35 (2315), 36 (1708), 17 (1185) |
| topic   | Occupation/interest                | 27            | indUnk (3287), Tech (2654) |
| sign    | Zodiac sign                        | 12            | Aries (4198), Sagittarius (1097) |
| date    | Date of post                       | 718           | 05,Aug,2004 (2329)         |
| text    | Blog post content                  | 9949          | Longest text repeats 13x   |

---

## 📌 Key Insights
- SVM is the most effective classifier for gender prediction.  
- KMeans provided interpretable and meaningful blog groupings.  
- Blog clustering reveals **content trends and author interests**.  
- Future work should integrate **modern NLP models** for scalability and interpretability.  

---

## 🚀 How to Run
1. Clone this repo:
   ```bash
   git clone <repo-url>
   cd blog-nlp-analysis
