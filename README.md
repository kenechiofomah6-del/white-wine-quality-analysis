# White Wine Quality Analysis

## Project overview

I used Python to explore how alcohol level and pH vary across sensory
quality ratings in a public white wine dataset. I also tested how well
a linear regression model could predict those ratings.

## Why I chose this project

At Viju Foods, I measured pH, Brix, and acidity during beverage quality
checks. This project helped me build on that experience by analysing
beverage measurements and evaluating a prediction model in Python.

## Data and methods

I used `winequality-white.csv` from the
[UCI Wine Quality dataset](https://archive.ics.uci.edu/dataset/186/wine+quality).
The file contains 4,898 records. The `quality` column contains the
sensory rating.

I used pandas to check and summarise the data, Matplotlib to plot
average alcohol and pH by rating, and Spearman correlation to compare
associations with sensory quality. I kept one copy of each identical
full row for the correlation and modelling sections, leaving 3,961
records. I then used scikit-learn to compare linear regression with
a median baseline on 793 held-out records.

## Key findings

- Wines rated 7 averaged 11.37% alcohol and pH 3.214. Wines rated 5
  averaged 9.81% alcohol and pH 3.169.
- Alcohol had the strongest association with sensory rating among the
  four measurements examined, with a Spearman correlation of 0.476.
- Linear regression achieved a mean absolute error of 0.597 rating
  points, compared with 0.648 for the median baseline. This was an
  improvement of 0.051 rating points on the test set.

## Limitations

The analysis used one white wine dataset. Only five test records had
a rating of 3, so the prediction error for that rating is based on
a small group. Evaluating the approach for another beverage would
require data from that product.

## How to run the notebook

1. Download `winequality-white.csv` from the UCI link above if needed.
2. Put the CSV in the same folder as `White-Wine-Quality-Analysis.ipynb`.
3. Install the required packages if they are missing:
   `pip install pandas matplotlib scikit-learn`.
4. Open the notebook in Jupyter and run all cells from top to bottom.