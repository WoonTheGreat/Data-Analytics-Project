## Predicting Borrower Payback with Lending Club Dataset

This project is to create a predictive model by using Decision Trees and Random Forests to predict whether a borrower will pay back investors on the platform Lending Club.

The goal is to identify the best people to invest in, which are the people most likely to pay you back.

----

By using **pandas_profiling.ProfileReport(loan_data)**, there's alot of useful information.

The histograms of each variable as it helps give a better understand of the data and the distributions.

However, the variable, "not fully paid" is not balanced, thus we will need to keep this in mind as we train and test our model.

The datas are then explored by using **matplotlib.pyplot as plt** to see how the variables interact with each other.

----

Based on various plots and charts drawn, some points can be identified:
-  debt consolidation is the number 1 reason for wanting a loan.
-  small business loans had a slightly higher proportion of fully paid vs not
-  the higher the fico score, the lower the interest rate you received

----

## Using Decision Tree Model & Random Forest Model

- Random Forest Model makes less overall errors than the Decision Tree Model
- The confusion matrix and classification report will be what we rely on for understanding our model.

Due to decision trees and random forest models are very sensitive to inbalanced datasets, weight(class_weight = "balanced") is applied to see if the model improves.
- By balancing the data, Decision Tree Model increased it's accuracy slightly.
- Random Forest Model had reduced performance.
- Decision Tree Model are chosen due to less type 1 errors (less false positivies).

----

## Conclusion

Decision tree and random forest models are created to try and predict loan defaults from this dataset. 

Although the random forest had a greater overall accuracy, the decision tree had less false positives, which is the error we want to minimize when considering who to loan money to - we want to minimize loaning to people who we think will pay back, but who end up not paying the money. 

The decision tree model could then be utilized on new datasets to determine if one should loan money or not to the user.
