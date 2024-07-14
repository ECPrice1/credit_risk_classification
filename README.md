# Credit Risk Classification Report

## Overview of the Analysis

* The purpose of this exercise to take the sample dataset and create a model that can be used to determine whether a loan application would results in either a "healthy loan" or a "high risk loan". A lender would seek to only approve the former and avoid the latter as they may result in a financial loss to the business. 
* The dataset includes information on 77,536 loans that were determined in the end to be either healthy or high risk.
* Data collected on each loan includes: loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks and total debt.
* Within the code, the dataset is divided into training and testing sets. 75% of the loans were used to first create or train the model and the remaining 25% were used to test how well the model performed.
* Because there are only 2 possible outcomes, the methodology used within the model is a logistic regression (binary classification).
* Results are analyzed using a generated classification report and confusion matrix.

## Results


* Accuracy is the metric used to describe the number of correct predictions overall and is often the ultimate metric in determining the efficacy of the model. Accuracy within the model was determined to be 99%, which is very good.

* Precision, the measure of how many of the positive predictions made are correct (true positives), shows as "1.00" for healthy loans in the classification report (which is rounded) and is just shy of being 100%, which illustates that the model does incredibly well at determining healthy loans. At 85%, the model doesn't do as well at correctly predicting high risk loans.

* Recall / Sensitivity is a measure of how many of the positive cases the classifier correctly predicted, over all the positive cases in the data. Similar to what we see in the precision metric, the model's recall on healthy loans, 99%, illustrate it's ability to correctly classify healthy loans. At 91%, the recall for high risk loans illustrates that it doesn't do as well with high risk loans. 

* F1-Score, which combines both precision and recall in a "harmonic mean", illustrates the same trend and shows 1.00 or nearly 100% for healthy loans and 88% for high risk loans. 

## Summary

* Overall accuracy of the model is quite good at 99%. 

The model's ability to predict a healthy loan is nearly perfect (99.5%) with 18,663 healthy loans correctly recognized as healthy and only 56 healthy loans that are incorrectly classified as high risk. If this were used as a credit underwriting tool, that would be acceptable, and those 56 customers incorrectly classified may have an opportunity for a manual credit review, if for example they were declined. From a lenders perspective, these false negatives simply represent a missed opportunity and do not present any major financial or reputational risk.

The model correctly classified 85% of high risk loans. 102 loans were incorrectly considered to be healthy that were actually high risk. This is the area of the confusion matrix that a lender would want to pay attention to as these loans, again in an underwriting scenario, would represents potential bad loans that were approved. Whether or not 85% is acceptable for a lender depends on a multitude of factors (rate, margin and delinquency trends within the industry segment), but in this case, high risk loans appear to occur a relatively low percentage of the time overall and only 102 bad loans out of over 19,000 is likely an acceptable margin of error. Said another way, if high risk loans naturally occured at a much higher rate and represented a greater proportion of the overall population, 85% may not be acceptable, but with overall accuracy at 99%, this appears to be a very good model. 






