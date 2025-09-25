# DATA 603 - Platforms for Big Data Processing  
### Assignment: MapReduce Implementation  

**Student:** Abdul Faisal Hussain Mohammed  
**DOB:** 06/24/2003  

---

## 📌 Overview
This assignment demonstrates the use of **MapReduce** in Python to process and analyze text files. The task is divided into two parts:
1. **Word Count (file1.txt)** – Count the frequency of words in a given text file.  
2. **Non-English Word Detection (file2.txt)** – Identify and count words that do not belong to the English dictionary.

---

## ⚙️ Implementation Details
- Implemented using **Python** with the following key modules:
  - `re` → for tokenizing words using regular expressions.  
  - `multiprocessing.Pool` → for parallel processing of map functions.  
  - `collections.Counter` → for efficient word counting.  
  - `pyspellchecker` → to validate English words.  

- **Mapper Functions**:
  - `mapper_word_count` → Extracts words and maps each to `(word, 1)`.  
  - `mapper_non_english` → Extracts words not in the English dictionary.  

- **Reducer Functions**:
  - Aggregate mapped outputs and count word frequencies using `Counter`.  

---

## 📂 Input Files
- **file1.txt** → Used for word count.  
- **file2.txt** → Used for detecting non-English words.  

---

## 📑 Output
- **Console Output** → Displays the top 20 most frequent words.  
- **Saved Results**:
  - `file1_output.txt` → Contains top 20 word counts from `file1.txt`.  
  - `file2_output.txt` → Contains top 20 non-English word counts from `file2.txt`.  

---

## 🚀 Running the Code
1. Place `file1.txt` and `file2.txt` in the working directory.  
2. Run the Python script:
   ```bash
   python assignment.py
