# DMML2022_moka_express
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/25423296/163456776-7f95b81a-f1ed-45f7-b7ab-8fa810d529fa.png">
</picture>


# About the project

In this project we are expected to create a classifier that predicts the level of a French text, e.g. A1, A2, B1, B2, C1, C2.

To train the classifier we are given 4800 labelled texts which are well balanced and have a base rate of 16.94%. To test the classifier we are asked to predict 1200 unlabelled texts, in form of a Kaggle competation. 

## Tfidf vectorizer 

While using the tfidf vectorizer and standord classifiers like logistic regression, knn, decision tree, random forest, I was able to get the accuracy to some 40%. Tuning the configs and hyperparameters did improve the result, combination of simple classifers through a soft or a hard voting also helped, though it was clear to me that a break through would require something new. 

See notebook 
[here](https://github.com/exmokapress/DMML2022_moka_express/blob/main/code/fr_difficulty_detection_tfidf_vectorizer.ipynb)

## Word embedding

To try out something new, I first started exploring the word embedding. Using NLP sentence vectorizer each text was vectorized to a 300 dimentional vector. This process was surprisingly fast and the result out of it was an accuracy close to 50%. Randomly tuning the SVC classifer based on some desktop research made the accuracy above 50%. 

See notebook 
[here](https://github.com/exmokapress/DMML2022_moka_express/blob/main/code/fr_difficulty_detection_word_embedding.ipynb)


## Pre trained hugging face models

To make the accuracy to 60% and further advance in the leader board, again it would require a new strategy. I challenged myself to fine tune the pre trained models on hugging face. Following the blog of fine tuning a bert model, I managed to get the first fine tuning work. Unfortunately the result was not that promising, accuracy even below 50%. Out of the dispointment I started looking for other pre trained models specific for the French language and tried out cased vs uncased models. My last approach on hugging face models was to fine tune the camembert model by following a tutorial in the internet. 

See notebook bert models 
[here](https://github.com/exmokapress/DMML2022_moka_express/blob/main/code/fr_difficulty_detection_bert_models_hugging_face.ipynb)

See notebook camembert models 
[here](https://github.com/exmokapress/DMML2022_moka_express/blob/main/code/fr_difficulty_detection_camembert_models_hugging_face.ipynb)

## Result summary

Tfidf vectorizer 
|            | Logreg best config, 80% data |  KNN tuned hp, 80% data   |Decision tree, 80% data    |Random forest, 80% data    |
|-----:      |------------------------------|---------------------------|---------------------------|---------------------------|
|    Accuracy|   45.56%                     |       43.75%              |      32.60%               |        42.71%             |

Word embedding
|            | Linear SVC, 80% data |  SVC, 80% data   |SVC tuned hp, 80% data   |SVC tuned hp, all data    |
|-----:      |------------------------------|---------------------------|---------------------------|---------------------------|
|    Accuracy|   48.44%                    |       48.54%              |      50.31%              |        51.17%             |

Hugging face pre trained models
|            | flaubert, all data |  camembert-base, 80% data   |camembert-base, all data    |camembert-base, more data    |
|-----:      |------------------------------|---------------------------|---------------------------|---------------------------|
|    Accuracy|   54.75%                     |       56.67%            |      59.58%           |        60.67%             |

## Other material

See the presentation 
[here](https://github.com/exmokapress/DMML2022_moka_express/blob/main/documentation/French%20language%20difficulty%20detection%20-%20Moka%20Express.pdf)

Watch the video
