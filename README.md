# Sentiment Analysis on Product Reviews

A simple, rule-based sentiment analysis pipeline implemented in a Jupyter Notebook. This project demonstrates how to:

- Load and preprocess a JSON Lines dataset of product reviews
- Perform exploratory data analysis (review counts, rating distribution, review length statistics)
- Build positive and negative word frequency lexicons via thematic analysis
- Preprocess review text (lowercasing, punctuation removal, tokenization, stop-word filtering)
- Apply a rule-based classifier to label each review as positive or negative
- Save the annotated results to an output file for further analysis or reporting

## Features

- **Data Loading**: Parses each line of a JSONL file into Python objects using `json`.
- **Exploration**: Computes basic statistics on review texts and ratings using `statistics`.
- **Thematic Analysis**: Gathers positive and negative word counts from the corpus.
- **Text Preprocessing**: Cleans and tokenizes text with regular expressions; removes common stop words.
- **Sentiment Classification**: Labels reviews by comparing counts of positive vs. negative terms.
- **Result Export**: Writes a tab-separated file of original reviews alongside predicted sentiment labels.

## Prerequisites

- Python 3.7 or newer
- No external libraries beyond the standard library (`json`, `re`, `statistics`)
- Jupyter Notebook (optional, to view and run interactively)

## Getting Started

1. **Clone the Repository**
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```

2. **Prepare the Dataset**
   - Place your review file (one JSON object per line, with `reviewText` and `overall` fields) in the root folder, e.g. `reviews.jsonl`.

3. **Run Interactively (Notebook)**
   ```bash
   jupyter notebook i222066_AyaanKhan_A0.ipynb
   ```

4. **Run as Script**
   If you prefer, extract the code into `sentiment_analysis.py` and run:
   ```bash
   python sentiment_analysis.py --input reviews.jsonl --output output.txt
   ```

5. **View Results**
   - The output file (default `output.txt`) contains each review and its predicted sentiment (`positive` or `negative`).

## File Structure

```
├── i222066_AyaanKhan_A0.ipynb   # Main notebook with full implementation
├── reviews.jsonl               # Input dataset (JSON Lines format)
├── output.txt                  # Generated sentiment-labeled results
└── README.md                   # This file
```

