# Trading Signal Classification: A Lesson in Class Imbalance

**Adetola Ridwat Odulaja** · Academic machine learning project

A study of technical-indicator features and the pitfalls of evaluating highly imbalanced labels.

**Focus:** Feature engineering · Label design · Critical model evaluation

## Question

Can classifiers reproduce Buy, Sell, and Hold labels defined by combined MACD and RSI rules?

## Approach

The notebook retrieves historical Tesla prices, calculates MACD and RSI indicators, constructs rule-based labels, and compares Logistic Regression, Random Forest, and SVM classifiers.

## Key finding

The notebook reports extremely sparse actionable labels: one Buy and no Sell labels in the dataset. The saved test set contains 302 Hold examples and no Buy or Sell examples.

All three saved classification reports show 100% accuracy on that Hold-only test set. **This does not demonstrate useful Buy/Sell prediction.** Minority-class capability cannot be assessed without test examples.

## Why it matters

The strongest lesson is about data and evaluation: a headline metric can look excellent while failing to answer the actual business question. Label distribution, baseline comparisons, and class-level support should be examined before interpreting model performance.

## Explore the work

- [Executed notebook](Project_3_ML_for_Predicting_Trading_Signals.ipynb)
- [Submitted report](pROJECT%203%20-%20ML%20for%20Predicting%20Trading%20Signals.pdf)

## Run

Open the notebook in Google Colab and run sequentially. It uses yfinance, Pandas, NumPy, Matplotlib, and scikit-learn. Data retrieval and library behavior can affect repeatability.

## Limitations & next improvements

Labels are derived from indicators also used as features, so this is rule reproduction rather than demonstrated forecasting. Revisit label design, use chronological evaluation, compare against a Hold baseline, and ensure actionable classes have adequate support. No profitable trading or live deployment is established. Saved outputs were not rerun during this review.

[Explore my portfolio](https://github.com/Ridwat/Ethical-AI-Analysis/blob/main/PORTFOLIO.md)
