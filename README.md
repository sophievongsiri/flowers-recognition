Video presentation of results: [SophieVongsiri_FinalProjectRecording.mp4 - OneDrive](https://onedrive.live.com/?id=A2933A6A1FD11785%21s6b2907f3bfba4eb9be037615d2002e9e&cid=A2933A6A1FD11785&redeem=aHR0cHM6Ly8xZHJ2Lm1zL3YvYy9hMjkzM2E2YTFmZDExNzg1L0lRRHpCeWxydXItNVRyNERkaFhTQUM2ZUFSZ0RnSWFfSFkybjhEX1pteng3amk0P25hdj1leUp5WldabGNuSmhiRWx1Wm04aU9uc2ljbVZtWlhKeVlXeEJjSEFpT2lKVGRISmxZVzFYWldKQmNIQWlMQ0p5WldabGNuSmhiRlpwWlhjaU9pSlRhR0Z5WlVScFlXeHZaeTFNYVc1cklpd2ljbVZtWlhKeVlXeEJjSEJRYkdGMFptOXliU0k2SWxkbFlpSXNJbkpsWm1WeWNtRnNUVzlrWlNJNkluWnBaWGNpZlgwPSZlPWg3ZHFPSw&parId=A2933A6A1FD11785%21sd74405d1addf4b6ab4642821d68ab061&o=OneUp)

I ran the following experiments to determine the best machine learning model to classify flower data:

2 options for data normalization
PCA with 2 options for number of components (dimensions)
Feature Selection (2 options)
4 different types of classifiers
Ensemble methods: Stacking and AdaBoost
Use k-fold cross validation with k=4 for all validations (nested 4-fold if needed)
Use Pipelines and GridSearch
Base your algorithm/parameter selection on accuracy, AUC of ROC, and F1-measure

Chosen Classifiers: KNN, SVM, Random Forest, MLP
Data Sets: PCA with 10, 50, 200, 400 components, Standard Scaler, Feature Selection: 50 most important features & Variance < .02, Original Data

General Steps for Evaluating Classifiers:
Perform GridSearch and/or Pipeline over different datasets and parameters with 4-fold cross validation
Identify dataset based suited for classifier based on accuracy and/or AUC of ROC and F1 measure
Graph best performing dataset(s) over different parameters with 4-fold cross validation
Compare training and validation accuracy, AUC of ROC, F1 measure, and consistency of accuracy across the 4 folds

Evaluating AdaBoost:
Iterated over different learning rates to determine the optimal parameter

Evaluating Stacking:
Compared confusion matrices and common misclassifications between chosen classifiers to select classifiers for the stacking model
Used Logistic Regression as the meta model
Iterated over different parameters to determine best values for stacking

Conclusion:
Stacking (KNN & MLP) was the best model for data as it maintained high accuracy and will limit overfitting.
