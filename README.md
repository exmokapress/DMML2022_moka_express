# DMML2022_moka_express
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/25423296/163456776-7f95b81a-f1ed-45f7-b7ab-8fa810d529fa.png">
  <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>


## About the project

<!-- TO DO: add more details about me later -->

In this project we are expected to create a classifier that predicts the level of a French text, e.g. A1, A2, B1, B2, C1, C2

To train the classifier we are given 4800 labelled texts which are well balanced and have a base rate of 16.94%. To test the classifier we are asked to predict 1200 unlabelled texts, in form of a Kaggle competation. 

While using the basic vectorizer and classifier I was able to get the accuracy to some 40%. Tuning the configs and hyperparameters did improve the result. Combination of simple classifers also helped, though it was clear to me that a break throug would require something new. 

Vectorizer: tfidf vectorizer using a standard spacy tokenizer and allowing some config tuning
Classifier: tune some hyperparameters depending on the classifier
Logistic regression
KNN
Decision tree
Random forest

To try out something new, I first started exploring the word embedding. Using NLP sentence vectorizer each text was vectorized to a 300 dimentional vector. This process was surprisingly fast and the result out of it was an accuracy close to 50%. Randomly tuning the SVC classifer based on some desktop research the accuracy went above 50%. 

Vectorizer: 
Word embedding using nlp sentence vectorizer
Each text is vectorized to a 300 dimensional vector
Classifier: tune some hyperparameters depending on the classifier
Linear SVC 
SVC

To make it to 60% and advance in the leader board, again it would require a new strategy. I challenged myself to fine tune the pre trained models on hugging face. Following the blog of fine tuning a bert model, I managed to get the first fine tuning work. Unfortunately the result was not that promising. Out of the dispointment I started looking for other pre trained models specific for the French language. There I continued with other bert models, tried out cased and uncased. My last approach was to fine tune the camembert model by following a tutorial in the internet. 




Hugging face pre trained models can make a difference!
Challenges
Make the fine tuning work
Make the prediction work
Try out different models
Bert models
FlauBert models
Camembert models



| Rank | THING-TO-RANK |
|-----:|---------------|
|     1|               |
|     2|               |
|     3|               |


See the presentation 
Watch the video
