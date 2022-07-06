# SoundScapify - Song Recommender based on Soundscape


## Introduction
### Background
Music has been along our side throughout our life. When we are babies, our parents would sing lullabies at night to make us asleep. When we are students, music accompaniments help us go through vicious cycles of exams and projects. Even as an adult, music help us go through a lot when we are bored, happy, sad or angry. Therefore, music plays a major role in our livelihood.      

### Problem Statement
Based on the information above, the project aims to build a **song recommender** based on the **current ambience and similar mood**. To accomplish the application, we first need to build a **classifier model** to classify the **ambient soundscape** in order for the recommender to give relevant and best result. Our target for model is to achieve more than **80%** accuracy. Based on the classified ambience, we then obtained a range of **audio features** that will be utilised to obtain similar songs.

### Proposed Approach
For this project, we will be utilising a deep learning model, which is **Long Short-Term Memory (LSTM) Neural Network**, which is one type of **Recurrent Neural Network** that has the ability to utilise order dependence. This means that the model will train based on the time sequence and "remember" the previous time sequence info to be incorporated in the current time sequence learning. This type of model works well in sequence prediction problems, and in our case, identifying the ambience sound.

**The Valence-Arousal plane** is also utilised in this project. The great thing of the model is it is able to identify mood of an audio within the 2-axis plane. The two features that are utilised are valence and arousal(energy). **Arousal** is an emotional dimension of musically energy level, while **Valence** is an emotional dimension of the comfortable level of the listener, which can be translated to whether the audio sounds happier or not [[1]](https://ieeexplore.ieee.org/document/8982519).

For the recommender, we uses Spotify's own recommender that we can access from **Spotify API** with additional information provided based on the classification made earlier. The info that is feeded including recently played tracks, minimum & maximum valence value and minimum & maximum energy value for the tracks recommended.

Overall, the **workflow** is as per below:
1. Find soundscape dataset
2. Explore and preprocess the dataset
3. Build a LSTM model and tune it
4. Build dataset of songs with audio features info
5. Explore the songs dataset
5. Create a criteria range for valence and energy
6. Create an app as a proof of concept (POC)

For this project, we will have 4 parts of notebook as follows:  
1. Introduction and Train Dataset EDA
2. Model Training
3. Model Prediction with Test Dataset
4. Song Dataset Retrieval

Apart from notebooks, we also needed a couple of .py scripts that is meant for the app development:
1. `app.py` -  contains the app function and features that has been developed
2. `authorization.py` - contains the authorization key of your Spotify API, such as client id, client secret and redirect url which can be retrieved from Spotify API upon registration 
3. `spotify.py` - contains collection of functions that are utilizing the Spotify API 

### Data Dictionary
This project involves the following datasets:  

|Dataset|Description|
|:---|:---|
|`fold1_train.csv`|Original dataset from [TAU Urban Acoustic Scenes 2022 Mobile, development dataset](https://zenodo.org/record/6337421) that contains filename and label of 1-second clips from multiple cities across Europe and recorded in 10 different acoustic scenes meant for training purposes| 
|`fold1_test.csv`|Original dataset from [TAU Urban Acoustic Scenes 2022 Mobile, development dataset](https://zenodo.org/record/6337421) that contains filename and label of 1-second clips from multiple cities across Europe and recorded in 10 different acoustic scenes meant for test purposes, the size of this dataset is 1/10th of the train dataset| 
|`valence_arousal_dataset.csv`|Dataset of songs from multiple genres that is scraped using [Spotify API](https://developer.spotify.com/documentation/web-api/) which includes the valence and energy value of the songs|
|`recommend_criteria.csv`|Dataset of criteria for the valence and energy range based on the label, which is extracted from `valence_arousal_dataset.csv`|

The datasets contains the following information/features:  

|Feature|Type|Dataset|Description|
|:---|:---:|:---:|:---|
|filename|*str*|`fold1_train.csv` & `fold1_test.csv`|The filename of 1-second clips from the dataset| 
|scene_label|*str*|`fold1_train.csv`|The labels of the acoustic scene where the audio is captured|
|id|*str*|`valence_arousal_dataset.csv`|The Spotify id of the songs in the dataset|
|genre|*str*|`valence_arousal_dataset.csv`|The genre of the songs in the dataset|
|track_name|*str*|`valence_arousal_dataset.csv`|The track name of the songs in the dataset|
|artist_name|*str*|`valence_arousal_dataset.csv`|The artist name of the songs in the dataset|
|valence|*float*|`valence_arousal_dataset.csv`|The valence value of the songs in the dataset|
|energy|*float*|`valence_arousal_dataset.csv`|The energy value of the songs in the dataset|
|label|*str*|`recommend_criteria.csv`|The label of acoustic scenes that we are classifying|
|valence_min|*float*|`recommend_criteria.csv`|The minimum valence value for the label classified|
|valence_max|*float*|`recommend_criteria.csv`|The maximum valence value for the label classified|
|energy_min|*float*|`recommend_criteria.csv`|The minimum energy value for the label classified|
|energy_2nd|*float*|`recommend_criteria.csv`|The energy value in 33th percentile for the label classified|
|energy_3rd|*float*|`recommend_criteria.csv`|The energy value in 66th percentile for the label classified|
|energy_max|*float*|`recommend_criteria.csv`|The maximum energy value for the label classified|

## Overview

## Summary

## Limitation & Future Works 