# Task for Cuetessa, Inc. – Predicting Valence of Pop Songs

## Objective

Valence describes the musical positiveness of a track, e.g. ranging from sad/depressed to happy/cheerful.  An automatic method of classifying the valence of pop songs is useful for playlist curation and other applications.  The aim of this task is to develop a Python-based module to predict the valence of newly released pop songs. Publicly available datasets can be used for training and testing


Two approaches are to use as input:
  - the audio data (e.g., .wav files) of songs 
    - Regression model trained using  audio features extracted from audio files
  - The lyrics of songs. 
     - Bidirectional Encoder Representations from Transformers (BERT) model to predict valence from lyrics

Due to lack of sufficient resources and the scale of this project:
- Sample of 500 songs taken from original dataset
- Audio previews for respective songs extracted for feature extraction


## Data Description

[Lyrics dataset on Kaggle](https://www.kaggle.com/datasets/edenbd/150k-lyrics-labeled-with-spotify-valence?resource=download) that contains:
- full lyrics and labels of more than 150,000 songs 
- The label is the Spotify valence attribute, ranging from 0 to 1.
  - It describes the musical positiveness conveyed by a track. 
  - Tracks with high valence sound more positive (happy, cheerful), while tracks with low valence sound more negative (sad, depressed). 
- Music attributes such as (tempo, danceability,loudness,etc) extracted and added  to original dataset using Spotify’s Web API for Developers. 
  - Spotify's Web API can extract relevant song data from the Spotify music catalog

![alt text](https://github.com/giova22i/Data-Science-Portfolio/blob/main/images/correlation.png)

## Libraries used
    - pandas
    - numPy
    - matplotlib
    - seaborn
    - spotipy
    - transformers
    - sklearn
    - Librosa

## Models Evaluated
    - Support Vector Regressor
    - RandomForestRegressor
    - KNeighborsRegressor
    - XGBRegressor
    - CatBoostRegressor
    - LGBMRegressor

## Insights

- Further training the model based on such dataset and assess if val_MAE is improving.
- Using the valence predicted by the CNN and the valence probability predicted for the songs’ lyrics by an NLP model as inputs to train a linear regression mixed model.
- Genre classification can also be completed using CNN
- Building a larger dataset by hiring a third-party provider (such as Appen) to rate Spotify songs preview’s valence.
