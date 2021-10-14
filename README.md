# DATA 512 - Assignment 2

The goal of this assignment is to explore the concept of bias through data on Wikipedia articles - specifically, articles on political figures from a variety of countries. For this assignment, you will combine a dataset of Wikipedia articles with a dataset of country populations, and use a machine learning service called ORES to estimate the quality of each article.

## Pre-requisites
- python
- Jupyter notebook
- `pandas` python package
- `requests` python package
- `numpy` puython package

## Data gathering
- `Politicians by Country from the English-language Wikipedia` from Figshare: https://figshare.com/articles/dataset/Untitled_Item/5513449
- `World Population Data` was published by the Population Reference Bureau: https://docs.google.com/spreadsheets/d/1CFJO2zna2No5KqNm9rPK5PCACoXKzb-nycJFhV689Iw/edit?usp=sharing
- `ORES` was used to predict the quality of Wikipedia articles: https://ores.wikimedia.org/

API reference: 
- ORES scoring API: https://ores.wikimedia.org/v3/#!/scoring/get_v3_scores_context_revid_model

## Data cleaning
The raw data was processed using `pandas` and is located in the `data_clean` directory after executing the notebook.

The final processed data is in the following schema:
```
column                  value
-------------------------------
country                  string
article_name             string
revision_id              integer
article_quality_est      article_quality
population               integer
```

You can check the Wikipedia content assesment quality documentation here: https://en.wikipedia.org/wiki/Wikipedia:Content_assessment 

## Analysis
The analysis itself is included within the end section of the Jupyter notebook.

## Special considerations
- There was an overlap between the `Pagecounts` and `Pageviews` API around 2014-10 through 2016-10. Hence some visits might have been double counted;
- The page counts might include bots & web crawler and is not necessarily only organic traffic.

## Folder structure
```
./
  ./data_clean # output location for processed data
  ./data       # output location for raw data
  ./src        # jupyter notebook file location
```

## Licensing
This project is under an MIT license.

Data coming from Wikipedia is under Wikipedia's own terms and conditions which can be found here: https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions

