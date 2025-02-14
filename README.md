# Multilingual Reputation Generation System - Datasets

## 📌 About This Repository

This repository contains the datasets used in the research paper:
📄 "Multilingual Reputation Generation System through Daily Opinion Mining Analysis", published in Results in Engineering.

The datasets included here were used for evaluating various components of the proposed system, such as aspect-based sentiment analysis (ABSA), sarcasm detection, deceptive review filtering, and reputation computation. These datasets originate from benchmark NLP datasets as well as manually collected and annotated reviews from social media platforms.

# 📂 Dataset Overview :

---

This part of the repository contains datasets for **Aspect-Based Sentiment Analysis (ABSA)** Below is a summary of the available datasets:

## 1️⃣ **SemEval 2014 Task 4 (Rest14 & Lap14)**  
- **Topic**: Restaurant & Laptop Reviews  
- **Size**: 6370 (Rest14), 3766 (Lap14)  
- **Task**: Aspect-Based Sentiment Analysis (ABSA)

## 2️⃣ **SemEval 2015 Task 12 (Rest15)**  
- **Topic**: Restaurant Reviews  
- **Size**: 2412  
- **Task**: Aspect-Based Sentiment Analysis (ABSA)

## 3️⃣ **SemEval 2016 Task 5 (Rest16)**  
- **Topic**: Restaurant Reviews  
- **Size**: 3242  
- **Task**: Aspect-Based Sentiment Analysis (ABSA)

## 4️⃣ **Mixed Dataset**  
- **Topic**: Restaurant & Laptop Reviews  
- **Size**: 13,348  
- **Task**: Aspect-Based Sentiment Analysis (ABSA)  
- This dataset is a combination of the datasets listed above.


For detailed instructions on how to access these datasets, please refer to the [**Mixed_SemEval_for_ABSA.md**](Mixed_SemEval_for_ABSA.md) file.


---------------------------------------------------------------------------

This part of the repository contains datasets for **Translation Evaluation**. Below is a summary of the available dataset:

## Multilingual Review Dataset  
- **Topic**: Smartphone Reviews (iPhone 16)  
- **Size**: 670 reviews in 5 languages (French, Hindi, Spanish, Turkish, Arabic)  
- **Sentiment Distribution**: 380 Positive, 265 Negative, 58 Sarcastic  
- **Task**: Evaluating Sentiment Preservation in Translations


For detailed instructions on how to access these datasets, please refer to the [**Translation Evaluation/**](Translation Evaluation/) file.

-----------------------------------------------------------------------------

3️⃣ Sarcasm Detection Datasets

Sarcasm Corpus V2

🏷️ Topic: General text reviews
🎯 Task: Sarcasm detection

Stanford Sentiment Treebank (SST-2)

🏷️ Topic: General text reviews
🎯 Task: Sentiment classification
--------------------------------------------------------------------------
4️⃣ Deceptive Review Detection Dataset

Deceptive Review Dataset (Collected from Social Media)

🏷️ Topic: Reviews from Twitter, Facebook, Yelp, TripAdvisor
📊 Size: 1000 reviews (682 genuine, 318 spam)
🎯 Task: Fake/deceptive review detection

---------------------------------------------------------------------------

5️⃣ Reputation Computation Datasets

Phone Product Dataset

🏷️ Topic: Smartphone brand reviews
📊 Size: 3000 reviews (1980 Positive, 700 Negative)
🎯 Task: Reputation Score Calculation

Web Application Dataset

🏷️ Topic: Online service reviews
📊 Size: 2500 reviews (1450 Positive, 820 Negative)
🎯 Task: Reputation Score Calculation


------------------------------------------------------------
------------------------------------------------------------

📜 Citation
If you use these datasets in your research, please cite our paper:

article{Boumhidi2025MultilingualReputation,
  author  = {Achraf Boumhidi, Abdessamad Benlahbib, Erik Cambria, El Habib Nfaoui},
  title   = {Multilingual Reputation Generation System through Daily Opinion Mining Analysis},
  journal = {Results in Engineering},
  year    = {2025}
}
