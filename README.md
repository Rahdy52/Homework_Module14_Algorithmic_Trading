# Homework_Module14_Algorithmic_Trading
This Challenge is about creating Machine Learning Trading Bot

# Machine Learning Trading Bot

## Background

In this Challenge, you’ll assume the role of a financial advisor at one of the top five financial advisory firms in the world. Your firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, your firm has heavily profited by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave your firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. You’re thus planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, you’ll enhance the existing trading signals with machine learning algorithms that can adapt to new data.

## What You're Creating

You’ll combine your new algorithmic trading skills with your existing skills in financial Python programming and machine learning to create an algorithmic trading bot that learns and adapts to new data and evolving markets.

In a Jupyter notebook, you’ll do the following:

* Implement an algorithmic trading strategy that uses machine learning to automate the trade decisions.

* Adjust the input parameters to optimize the trading algorithm.

* Train a new machine learning model and compare its performance to that of a baseline model.

As part of your GitHub repository’s `README.md` file, you will also create a report that compares the performance of the machine learning models based on the trading predictions that each makes and the resulting cumulative strategy returns.


## Evaluation Report

### Baseline Performance

              precision    recall  f1-score   support

        -1.0       0.43      0.04      0.07      1804
         1.0       0.56      0.96      0.71      2288

    accuracy                           0.55      4092
   macro avg       0.49      0.50      0.39      4092
weighted avg       0.50      0.55      0.43      4092

![image](https://github.com/Rahdy52/Homework_Module14_Algorithmic_Trading/assets/66510693/5ceb30d8-07f9-470a-adfb-40be4fb99dc3)




### Tuned Baseline Trading Algorithm

                    precision    recall  f1-score   support

        -1.0       0.48      0.01      0.01      1733
         1.0       0.56      0.99      0.72      2217

    accuracy                           0.56      3950
   macro avg       0.52      0.50      0.37      3950
weighted avg       0.53      0.56      0.41      3950


![image](https://github.com/Rahdy52/Homework_Module14_Algorithmic_Trading/assets/66510693/88dfcbd9-b642-4df5-8321-353b7d3bb778)


### Evaluate a New Machine Learning Classifier

             precision    recall  f1-score   support

        -1.0       0.44      0.08      0.13      1804
         1.0       0.56      0.92      0.70      2288

    accuracy                           0.55      4092
   macro avg       0.50      0.50      0.41      4092
weighted avg       0.51      0.55      0.45      4092


![image](https://github.com/Rahdy52/Homework_Module14_Algorithmic_Trading/assets/66510693/4bd31e50-0331-4dd6-8112-58ac6c892197)


Conclusion:

The provided SVM model generated an accuracy score of 55% and a high recall score (96%) when buying but a low recall score (4%) when selling. This indicates the model performs extremely well when determining when to enter a position. Adjusting  the short SMA window to 8 from 4 and the long SMA window to 110 from 100 as well as the size of Training Data to 6 months did not have meaningful impact than that of the original baseline's. Accuracy score are almost the same but the recall for selling (-1) decreased indicating the tuned model missed a lot of relevant data points than the original.
The AdaBoost model performed slightly better in the selling position but not significantly and even dipped in recall when determining when to buy.



