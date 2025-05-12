# Sentiment Analysis using Rule-Based Thematic Approach

## Overview

This project performs sentiment analysis on a product reviews dataset using a rule-based approach enhanced by thematic word classification. It includes data preprocessing, thematic word identification, sentiment scoring, and exporting results.

## Features

* Loads and parses a large JSON-based review dataset.
* Cleans and preprocesses review text by removing punctuation and stop words.
* Performs thematic analysis using pre-defined positive and negative word sets.
* Applies a rule-based sentiment classifier with weighted scores adjusted based on thematic word frequency.
* Saves results with predicted sentiment to a text file.

## Dataset

* Dataset: Amazon Cell Phones and Accessories Review Dataset (JSON format)
* Fields Used: `reviewText`, `overall`

## Methodology

### 1. **Data Loading and Preprocessing**

* Extracts review text and ratings.
* Cleans text by removing punctuation and converting to lowercase.
* Removes common English stop words.

### 2. **Thematic Analysis**

* Counts occurrences of words from predefined sets:

  * Positive Words (e.g., "awesome", "excellent", "perfect")
  * Negative Words (e.g., "bad", "terrible", "poor")

### 3. **Sentiment Scoring**

* Assigns weights to keywords using a dictionary.
* Adjusts weights based on frequency from thematic analysis.
* Computes cumulative sentiment score per review.
* Classifies sentiment as:

  * `positive` (score > 0.5)
  * `negative` (score < -0.5)
  * `neutral` (otherwise)

### 4. **Saving Results**

* Stores each review along with its predicted sentiment in an output text file.

## How to Run

1. Place the dataset JSON file at the specified path.
2. Run the notebook in a Python environment with standard libraries.
3. Output is saved in a `.txt` file containing sentiment-tagged reviews.

## Sample Output

```
I love this case! It's beautiful and durable. - positive
The screen protector didn't fit at all. Waste of money. - negative
Decent product for the price. - neutral
```

## Technologies Used

* Python 3
* Regular Expressions (`re`)
* JSON Parsing
* File I/O

## Author

* Ayaan Khan (i222066)

## License

This project is for educational purposes only as part of a Big Data Analytics assignment.
