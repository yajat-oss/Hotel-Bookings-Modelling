**Hotel Booking Cancellation Analysis**

This project analyses a dataset of 119,390 hotel bookings from two hotels in Portugal, with the goal of predicting whether a booking is likely to be cancelled.
It was originally completed as the final assessment for the Maths in AI and Data Science course run by ASMP. I have since revisited the project independently, adding hotel-type segmentation models and additional linear regression analysis beyond the original specification.
The dataset is sourced from Kaggle.

**What the project covers:**

Exploratory Data Analysis — examining how cancellation rates vary across hotel type, market segment, lead time, booking changes, and guest composition.
Decision Tree Classification — five models of increasing complexity, starting from a single-feature baseline and progressing to multi-feature models. Models 4 and 5 segment the data by hotel type (City Hotel vs Resort Hotel), which improves performance and reflects genuine differences in booking behaviour between the two.
Linear Regression — three simple regression models exploring relationships between guest composition, special requests, and stay duration or daily rate.

**Key findings:**

Longer lead times and bookings made through online travel agents are strongly associated with higher cancellation rates
City Hotels have a significantly higher cancellation rate than Resort Hotels
Segmenting models by hotel type improves predictive performance
Simple single-feature models establish a useful baseline but lack the complexity to reliably detect cancellations in an imbalanced dataset

**Libraries used:**

pandas,  scikit-learn,  matplotlib, seaborn
