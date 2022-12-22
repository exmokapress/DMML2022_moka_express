# DMML2022_moka_express
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/25423296/163456776-7f95b81a-f1ed-45f7-b7ab-8fa810d529fa.png">
  <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>


# About the project

In this project we are expected to create a classifier that predicts the level of a French text, e.g. A1, A2, B1, B2, C1, C2.

To train the classifier we are given 4800 labelled texts which are well balanced and have a base rate of 16.94%. To test the classifier we are asked to predict 1200 unlabelled texts, in form of a Kaggle competation. 

## Tfidf vectorizer 

While using the tfidf vectorizer and standord classifiers like logistic regression, knn, decision tree, random forest, I was able to get the accuracy to some 40%. Tuning the configs and hyperparameters did improve the result, combination of simple classifers through a soft or a hard voting also helped, though it was clear to me that a break through would require something new. 

See notebook https://github.com/exmokapress/DMML2022_moka_express/blob/main/code/fr_difficulty_detection_tfidf_vectorizer.ipynb

## Word embedding

To try out something new, I first started exploring the word embedding. Using NLP sentence vectorizer each text was vectorized to a 300 dimentional vector. This process was surprisingly fast and the result out of it was an accuracy close to 50%. Randomly tuning the SVC classifer based on some desktop research made the accuracy above 50%. 


## Pre trained hugging face models

To make the accuracy to 60% and further advance in the leader board, again it would require a new strategy. I challenged myself to fine tune the pre trained models on hugging face. Following the blog of fine tuning a bert model, I managed to get the first fine tuning work. Unfortunately the result was not that promising, accuracy even below 50%. Out of the dispointment I started looking for other pre trained models specific for the French language and tried out cased vs uncased models. My last approach on hugging face models was to fine tune the camembert model by following a tutorial in the internet. 


## Result summary

|            | Logreg best config, 80% data |  KNN tuned hp, 80% data   |
|-----:      |------------------------------|---------------------------|
|    Accuracy|   45.56%                     |       43.75%              |
|     2.     |                              |                           |
|     3.     |                              |                           |

## Other material

See the presentation 

Watch the video
