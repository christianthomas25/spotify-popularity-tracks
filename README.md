# Spotify Hit Song Prediction (Machine Learning Project)

## Overview
This project applies machine learning techniques to predict whether a song will become a hit using Spotify data.

The goal is to support record labels and music companies in making data-driven investment decisions by identifying high-potential tracks early and allocating marketing resources more efficiently.

---

## Business Problem
The music industry follows a hits-driven model where a small number of songs generate a disproportionate share of revenue.

Key challenges:
- Missing a hit leads to significant opportunity cost  
- Promoting non-hit songs results in wasted marketing spend  
- Decisions are often subjective rather than data-driven  

This project addresses the problem of selecting which songs to promote.

---

## Dataset
- Source: Spotify dataset (Kaggle)  
- Initial size: ~114,000 tracks  
- Final cleaned dataset: 81,343 tracks  

Features include:
- Danceability  
- Energy  
- Loudness  
- Acousticness  
- Instrumentalness  
- Genre  

Target variable:
- Binary classification (Hit vs Non-Hit) based on top 25% popularity threshold  

---

## Methodology

### Data Preparation
- Removed duplicates and inconsistencies  
- Performed feature engineering (e.g. mood intensity)  
- Grouped genres into broader categories  
- Handled outliers and data types  

### Models Tested
- Decision Tree  
- Random Forest  
- XGBoost  

### Final Model
XGBoost was selected due to:
- Best overall performance across metrics  
- Strong generalization  
- Balanced precision and recall  

---

## Results

- ROC-AUC: ~0.76  
- Accuracy: ~66%  
- Recall: ~0.74  

The model effectively identifies high-potential songs while maintaining stability across training and test sets.

---

## Key Insights

### Audio Features Drive Success
Audio characteristics are more predictive than genre:
- Loudness  
- Energy  
- Danceability  

### Characteristics of Hit Songs
- Higher loudness increases success probability  
- Vocal tracks outperform instrumental songs  
- High danceability correlates with hits  
- High acousticness reduces likelihood of success  

---

## Business Impact

A profit-based framework was applied:

- Gain from correctly identifying a hit: €10,000  
- Cost of missing a hit: €5,000  
- Cost of promoting a non-hit: €1,000  

Key conclusion:
Maximizing recall (capturing more hits) leads to higher overall profit, even with increased false positives.

---

## Recommendations

1. Prioritize early investment in high-potential tracks  
2. Implement a tiered marketing strategy  
3. Use audio features in production and selection decisions  

---

## Limitations
- Does not include artist popularity or brand strength  
- Does not account for social media or virality effects  
- Based only on Spotify data  
- Does not capture evolving music trends  

---

## Tech Stack
- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- SHAP  

---

## Team
- Thomas Christian Matenco  
- Enzo Jerez  
- Roberto Cummings  
- Jia Yi Rachel Lee  
- Maria-Irina Popa  

---

## Key Takeaway
A data-driven, high-recall strategy that prioritizes identifying potential hits leads to superior financial outcomes compared to conservative selection approaches.
