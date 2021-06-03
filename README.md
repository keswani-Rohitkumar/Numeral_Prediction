# Numeral Prediction from short audio segment

In this project I have built a model that predicts the numerals of a short audio segment. The audio dataset was prepared by the batch of MSc Big Data Science at QMUL.

The trainingMLEND.csv consits of 20k rows and 4 columns. Each row corresponds to one of the items in our dataset, and each item is described by four attributes.

    File ID (audio file)
    Numeral
    Participand ID
    Intonation

Here I have extracted many features from the audio signal namely

    Power
    Pitch mean
    Pitch standard deviation
    Fraction of voiced region using librosa library.

I build 6 models which are

    SVM
    RandomForest
    KNN
    Naive Bayes
    Logistic Regression
    MuliLayer Perceptron Classifier
    Nueral Network using Keras Sequential API

I build these models and trained them on hyperparameters, tuning them with the help of GridSearch CV. I build these models for both normalised predictors and without normalised also and with extra features such as mfcc and experimented them.

I build these models for predicting all the numerals which were Ones Sequence (0-9), Teens Sequence(10-19), Large Sequence ( twenty, thirty, ...., hundred, thousand, million, billion). 

But the accuracy for predicitng all the numerals were very low so I tried to find a different approach and experimented with predicting only the ones sequence and finally, I achieved the highest Accuracy of 35% for the validation data using neural networks using Keras Sequential API.

![image](https://user-images.githubusercontent.com/51491512/120647640-bcee9400-c472-11eb-8b44-daedc5fab170.png)

![image](https://user-images.githubusercontent.com/51491512/120648136-34242800-c473-11eb-9f64-c4bd1c8560d4.png)

![image](https://user-images.githubusercontent.com/51491512/120648198-43a37100-c473-11eb-8bdd-dd47f79b1282.png)

It can be seen that there is a minimal change in accuracy over the 100 epochs for both training and validation.
