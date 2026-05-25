# Sentiment-Oriented Lexical Analysis of *Alice’s Adventures in Wonderland*

**Texts analyzed:**  
- *Down the Rabbit Hole* (Chapter 1)  
- *A Mad Tea Party* (Chapter 7)  
- *The Queen’s Croquet-Ground* (Chapter 8)

## Project Description

This project investigates sentiment‑oriented lexical patterns in three chapters of *Alice’s Adventures in Wonderland*. As a linguist exploring NLP, I was interested in how simple computational methods can highlight stylistic and emotional tendencies in literary text without relying on large pretrained models or external sentiment libraries.

The analysis is based on a small, manually curated set of positive and negative lexical items. After preprocessing the text (normalization, punctuation removal, stop‑word filtering), the script identifies occurrences of these sentiment‑marked words and calculates their density per 1000 words. Although intentionally minimalistic, this approach already reveals contrasts between chapters with more chaotic, conflict‑driven scenes and those with lighter, descriptive passages.

The project demonstrates how handcrafted linguistic resources, combined with basic Python and NLTK tools, can produce meaningful insights into narrative tone. It also serves as a foundation for future work, including expanded lexicons, visualization, and comparisons with established sentiment analysis tools such as VADER.

This repository is part of my broader journey of integrating linguistic intuition with computational methods and building a small portfolio of transparent, interpretable NLP experiments.

---

## Project Overview

The goal of this project was to:

- preprocess three chapters of *Alice’s Adventures in Wonderland*  
- remove punctuation and stop words  
- identify occurrences of predefined **positive** and **negative** lexical items  
- calculate:  
  - **positive word count**  
  - **negative word count**  
  - **positive density** (per 1000 words)  
  - **negative density** (per 1000 words)  
- extract lists of all positive and negative words found in each chapter  

The project uses a simple lexicon-based approach to sentiment tendencies, without machine learning or external sentiment dictionaries.

---

## Methodology

The analysis pipeline includes:

- normalization (lowercasing, replacement of curly quotes)  
- punctuation removal using regular expressions  
- tokenization via `.split()`  
- stop-word filtering using NLTK  
- manual positive/negative lexicon  
- counting occurrences and calculating densities  

All computations are performed on the cleaned, stop‑word‑filtered corpus to ensure comparability across chapters.

---

## Results

### Raw output

```
down_the_rabbit_hole.txt
Positive words: 1
Negative words: 2
Found positive: ['glad']
Found negative: ['fear', 'afraid']
Positive density: 1.02
Negative density: 2.05

mad_tea_party.txt
Positive words: 2
Negative words: 3
Found positive: ['glad', 'beautiful']
Found negative: ['mad', 'mad', 'afraid']
Positive density: 1.82
Negative density: 2.73

queens_croquet_ground.txt
Positive words: 2
Negative words: 2
Found positive: ['laughter', 'glad']
Found negative: ['afraid', 'frightened']
Positive density: 1.73
Negative density: 1.73
```

### Summary Table

| Chapter                     | Positive | Negative | Positive density | Negative density |
|-----------------------------|----------|----------|------------------|------------------|
| Down the Rabbit Hole        | 1        | 2        | 1.02             | 2.05             |
| A Mad Tea Party             | 2        | 3        | 1.82             | 2.73             |
| The Queen’s Croquet-Ground | 2        | 2        | 1.73             | 1.73             |


---

## Interpretation

Although the lexicon is intentionally small and manually curated, the results already show interesting contrasts between chapters.  
For example:

- Chapters with more chaotic or conflict-driven scenes tend to show higher negative density.  
- Chapters with descriptive or whimsical narrative passages show fewer sentiment-marked words overall.  

This simple method demonstrates how even minimal lexical resources can reveal stylistic tendencies.

---

## Future Work

Possible extensions:

- expanding the sentiment lexicon  
- adding neutral/emotive categories  
- visualizing densities across chapters  
- comparing sentiment curves within a single chapter  
- experimenting with external sentiment dictionaries (e.g., VADER, LIWC-style lists)  
- applying the method to non-literary texts (forums, articles, UGC)

---

## Code

The full Python script is available in:

- `sentiment_analysis.py`

---

## Data

To make the project reproducible, include:

- `down_the_rabbit_hole.txt`  
- `mad_tea_party.txt`  
- `queens_croquet_ground.txt`

