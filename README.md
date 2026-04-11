# Hotel Booking Cancellation Analysis

This project analyses 119,390 hotel bookings from two hotels in Portugal
between July 2015 and August 2017, with the goal of predicting whether a
booking is likely to be cancelled.

It was originally completed as the final assessment for the Maths in AI
and Data Science course run by ASMP. I have since independently extended
it by adding a correlation heatmap for feature selection, additional EDA,
a stronger multi-feature classification model, feature importance analysis,
a confusion matrix, cross-validation, a ROC curve, and a multi-feature
linear regression model.

The dataset is sourced from Kaggle.

## What the project covers

**Exploratory Data Analysis** — investigating how cancellation rates vary
across hotel type, market segment, lead time, booking changes, number of
special requests, and whether the guest is a returning visitor.

**Decision Tree Classification** — five models of increasing complexity.
The first two act as baselines using a single feature each. Model 3 adds
behavioural history. Models 4 and 5 segment the data by hotel type to
reflect the difference in cancellation behaviour between City and Resort
hotels. The best model uses seven features selected from the correlation
analysis, one-hot encodes hotel type, and applies class balancing to
address the imbalance in the dataset.

**Model Evaluation** — the best model is evaluated using precision,
recall, a confusion matrix, 5-fold cross-validation, and a ROC curve
with AUC score.

**Linear Regression** — four models predicting average daily rate and
length of stay. Three single-feature baselines are compared against a
multi-feature model to show the improvement from combining predictors.

## Key findings

- Lead time and previous cancellations are the strongest predictors of
  whether a booking will be cancelled
- City Hotels have a significantly higher cancellation rate than Resort
  Hotels, which justified building separate models for each
- Guests who make special requests or have stayed before are much less
  likely to cancel
- Simple single-feature models are too limited to detect cancellations
  reliably due to class imbalance — adding more features and balancing
  the classes significantly improves recall
- Combining multiple features in linear regression produces a better
  model for predicting average daily rate than any single predictor alone

## Libraries used

`pandas` · `scikit-learn` · `matplotlib` · `seaborn` · `numpy`
