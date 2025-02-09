# SemEval Datasets: Access and Merging Guide for ASBA

## Step 1: Download the Datasets
To download the SemEval datasets, you will need to visit the official sources for each task. Below are the links to the datasets:
- [SemEval 2014 Task 4](https://alt.qcri.org/semeval2014/task4/)
- [SemEval 2015 Task 12](https://alt.qcri.org/semeval2015/task12/)
- [SemEval 2016 Task 5](https://alt.qcri.org/semeval2016/task5/)

Important Note:
Before downloading the datasets, you will need to accept the license terms associated with each dataset. The license terms typically outline the permitted uses of the data, restrictions, and citation requirements.


## Step 2: Load the Datasets
Assuming you have downloaded the datasets in XML format, use `BeautifulSoup` to parse them and convert them into a structured DataFrame.

```python
import pandas as pd
from bs4 import BeautifulSoup
import os

def parse_semeval_xml(file_path):
    with open(file_path, 'r', encoding='utf-8') as f:
        content = f.read()
    
    soup = BeautifulSoup(content, 'xml')
    data = []
    
    for review in soup.find_all('sentence'):
        text = review.text.strip()
        aspects = review.find_all('aspectTerm')
        for aspect in aspects:
            term = aspect['term']
            polarity = aspect['polarity']
            data.append([text, term, polarity])
    
    return pd.DataFrame(data, columns=['text', 'aspect', 'sentiment'])

# Load datasets
rest14 = parse_semeval_xml('data/Restaurants_Train.xml')
lap14 = parse_semeval_xml('data/Laptops_Train.xml')
rest15 = parse_semeval_xml('data/Restaurants_Train_2015.xml')
rest16 = parse_semeval_xml('data/Restaurants_Train_2016.xml')
```

## Step 3: Normalize Column Names
Ensure that all datasets follow the same structure:

```python
# Standardizing column names
for df in [rest14, lap14, rest15, rest16]:
    df.columns = ['text', 'aspect', 'sentiment']
```

## Step 4: Merge the Datasets
Now, concatenate all datasets into a single DataFrame:

```python
# Merge datasets
mixed_dataset = pd.concat([rest14, lap14, rest15, rest16], ignore_index=True)

# Save the combined dataset
mixed_dataset.to_csv('data/mixed_absa_dataset.csv', index=False, encoding='utf-8')
```

## Step 5: Load and Verify the Merged Dataset

```python
# Load the dataset to check its structure
merged_data = pd.read_csv('data/mixed_absa_dataset.csv')
print(merged_data.head())
```

### Summary:
1. Download the datasets from SemEval official pages.
2. Use `BeautifulSoup` to parse XML files.
3. Normalize column names.
4. Merge all datasets.
5. Save the combined dataset for training.

This combined dataset (13,348 instances) can now be used for Aspect-Based Sentiment Analysis (ABSA) as discribed in the manuscript.
