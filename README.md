# Assignment 2 – Text Processing and Classification using Apache Spark

Course: Data-intensive Computing (DIC 2026)  
Assignment: Assignment 2 – Text Processing and Classification  
Group: Group05

---

# Project Overview

This project implements distributed text processing and document classification using Apache Spark (PySpark).

The implementation contains two parts:

## Part 1 – RDD Processing

Implemented using Spark RDD operations.

Tasks:

- Load review dataset
- Text preprocessing
- Tokenization
- Stopword removal
- Generate `(term, category)` pairs
- Compute Chi-Square scores
- Extract relevant terms per category

Output produced:

```text
output_rdd.txt
```

---

## Part 2 – DataFrame / ML Pipeline

Implemented using Spark ML Pipeline.

Pipeline steps:

1. RegexTokenizer
2. StopWordsRemover
3. CountVectorizer
4. TF-IDF
5. StringIndexer
6. Logistic Regression classifier
7. Accuracy evaluation

Generated outputs:

```text
output_ds.txt
classification_results.txt
```

---

# Dataset

Input dataset:

```text
data/reviews_devset.json
```

Additional preprocessing resource:

```text
data/stopwords.txt
```

Dataset statistics:

- Documents: ~78,800
- Categories: 22

---

# Project Structure

```text
Group05_DIC2026_Assignment_2/

data/
│── reviews_devset.json
│── stopwords.txt

outputs/
│── output_rdd.txt
│── output_ds.txt
│── classification_results.txt

report/
│── report.pdf

src/
│── 00_check_environment.py
│── 01_part1_rdd_chisquare.py
│── 02_part2_ds_pipeline.py
│── utils_preprocessing.py

README.md
requirements.txt
```

---

# Requirements

Software:

- Python 3.11+
- Java JDK 17
- Apache Spark 3.5.1

Required packages:

```bash
pip install -r requirements.txt
```

---

# Environment Setup

Create environment:

```bash
python -m venv .venv
```

Activate (Windows):

```bash
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# Execution

Move into source directory:

```bash
cd src
```

Check environment:

```bash
python 00_check_environment.py
```

Run Part 1:

```bash
python 01_part1_rdd_chisquare.py
```

Run Part 2:

```bash
python 02_part2_ds_pipeline.py
```

---

# Produced Results

Execution generates:

```text
outputs/output_rdd.txt
outputs/output_ds.txt
outputs/classification_results.txt
```

---

# Experimental Result

Obtained classification accuracy:

```text
Accuracy = 0.6338
```

---

# Submission Files

Assignment submission contains:

- output_rdd.txt
- output_ds.txt
- report.pdf
- src/ implementation files
- README.md
