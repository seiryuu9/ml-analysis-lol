Goal: Analyze League of Legends match data and build a model to predict match outcomes using in-game statistics.



Dataset used:



Kaggle - League of legends ranked matches

https://www.kaggle.com/datasets/paololol/league-of-legends-ranked-matches?resource=download



This dataset had gathered a few years' worth of data from competitive LoL matches starting in 2014, so the dataset is quite outdated as the game and meta changes quite frequently but for the sake of this project, it is well-suited :)





!!!IMPORTANT!!!

Due to file size constraints of the dataset, raw data is not included in the repository.



Setup

1\. Download the dataset from: [https://www.kaggle.com/datasets/paololol/league-of-legends-ranked-matches?resource=download](https://www.kaggle.com/datasets/paololol/league-of-legends-ranked-matches?resource=download)

2\. Extract the files into: data/raw/

3\. The expected structure is:

ml-analysis-lol/data/raw/matches.csv (7 CSV files in total)



The notebooks will handle processing the data, so a folder data/processed will also appear later on!



1. Introduction



I have decided to create this prediction model as a way to learn more about machine learning, data analysis and practise it on real data.

Raw data can be found in the 'data/raw' folder. I will be using Jupyter notebook to create visualisations which can be found in the 'notebooks' folder.





2\. Notebooks



2.1 Notebook 01\_eda



My first notebook is Exploratory Data Analysis. It aims to help us grow familiar with the dataset, create some visualizations and make the raw data more user-friendly for future endeavours by merging the original CSV files.



For the first part of this notebook we worked with 2 files - 'matches.csv' and 'teamstats.csv'.

To get an idea of what data they contain, see the picture below:



\*insert picture of .head commands\*



Our goal is to have one joint table where 1 match = 1 row, so as a next step we separated the team stats per team - red and blue. Then we merged the blue and red team stats with matches table using the match ID into one big 'matches\_stats' table. We ran some code to get more familiar with the table's data, shape, etc.



The most important information is the column names, which are as follows:



Columns and types:

 id                   int64

gameid               int64

platformid          object

queueid              int64

seasonid             int64

duration             int64

creation             int64

version             object

blue\_teamid          int64

blue\_firstblood      int64

blue\_firsttower      int64

blue\_firstinhib      int64

blue\_firstbaron      int64

blue\_firstdragon     int64

blue\_firstharry      int64

blue\_towerkills      int64

blue\_inhibkills      int64

blue\_baronkills      int64

blue\_dragonkills     int64

blue\_harrykills      int64

red\_teamid           int64

red\_firstblood       int64

red\_firsttower       int64

red\_firstinhib       int64

red\_firstbaron       int64

red\_firstdragon      int64

red\_firstharry       int64

red\_towerkills       int64

red\_inhibkills       int64

red\_baronkills       int64

red\_dragonkills      int64

red\_harrykills       int64



Next we need to get information about wins/losses, as that's what is missing in our table. For this, we merge 'stats1.csv' and 'stats2.csv' into one table 'stats'. However, both of these tables are quite hefty and contain a lot of information, we only extract the columns relevant to us, which are the (match) id and wins (1/0).



\*insert picture of stats\*



* dont forget to add final tables into processed folder, maybe contents
