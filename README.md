# Natural-Language-Processing-for-sentiment-analysis
Tweets are automatically judged as positive or negative. To train a model to do so, more than a million (1,048,572) labeled tweets are used from the "Sentiment Analysis Dataset" on Kaggle (https://www.kaggle.com/datasets/abhi8923shriv/sentiment-analysis-dataset). The data is too big to be shared here and is available on Kaggle. The tweets are separated into words and assigned with numerical values using Keras tokenizer and then are (zero-) padded to equalize their lengths to be of size 40 (the longest tokenized tweet). The total number of words that are used in the model are limited to 10k (to prevent overfitting). This numerical representation is then further transformed using an embedding layer within the model, where each word is assigned with a 10 dimensional vector. Eventually, each tweet is represented by a 40x10 matrix. The model includes LSTM (long short-term memory) layers, dense layers, a binary cross entropy loss function and the accuracy metric. The model achieves accuracy of 0.82 both in training and validation. Finally, the model is evaluated by plotting a confusion matrix and by judging a few "unseen" tweets.

Confusion Matrix:
![img1](https://github.com/Morikky/Natural-Language-Processing-for-sentiment-analysis/blob/main/Plots/confusion_matrix.png)


Using the model to judge unseen tweets:
![img2]()
