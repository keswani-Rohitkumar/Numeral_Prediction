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

But the accuracy for predicitng all the numerals were very low so I tried to find a different approach and experimented with predicting only the ones sequence and finally, I got the highest Accuravy of 35% in the validation data using Keras Sequential API to build the neural network.

![image](https://user-images.githubusercontent.com/51491512/120647640-bcee9400-c472-11eb-8b44-daedc5fab170.png)


![image](https://user-images.githubusercontent.com/51491512/120647424-7f8a0680-c472-11eb-9196-a83efa0625f3.png)

As it can be concluded that there is many minimal differnece over the 100 epochs
![image](https://user-images.githubusercontent.com/51491512/120647541-9e889880-c472-11eb-9e17-220fea62fa29.png)



