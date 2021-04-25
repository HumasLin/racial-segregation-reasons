# The Micro-and-macro Reasons of Segregation in the U.S Metropolitan Areas

In this project, we analyzed how people's opinions on social media can be associated with the phenomenon of social segregation from both the micro-level (individual) and macro-level (city). The following notebooks include the processes and outcome of our analysis.

## Micro-level analysis

- bow_manual.ipynb: This notebook includes initial analysis on data manually picked from Facebook and Roomster, it's simply runable through Jupyter notebook.

- srcape_reddit_personal_attention.ipynb: This notebook includes scripts for scraping data from Reddit with Bigquery, filtering related content, and label the race identity of the comment. It needs a Google Cloud account and a Bigquery project registered with data at https://console.cloud.google.com/bigquery?p=fh-bigquery&page=project to run. And in our analysis, it can only be run on Google colab. The race labeling process is retained in the scraping process to protect privacy of the authors in the database.

- personal_attention.ipynb: This notebook runs analysis collected and preprocessed Reddit data, it can be simply run with Jupyter notebook. The visualizations it generates are based on manually selected results from the IDF and word clustering output of our automated analysis on data. It requires manual modification in the notebook to modify the visualization

## Macro-level analysis

- cities_reddit_colllection.ipynb: This notebook includes scripts for scraping data from 49 subreddits on Reddit with Bigquery. It needs a Google Cloud account and a Bigquery project registered with data at https://console.cloud.google.com/bigquery?p=fh-bigquery&page=project to run. And in our analysis, it can only be run on Google colab. 

- opinion_mining.ipynb: This notebook runs aspect-based opinion mining on 49 city-focused comments we collected from Reddit, it reads data collected from cities_reddit_colllection.ipynb and conducted opinion mining. It outputs file "city_aspects.npy" in the data folder.

- regression_analysis_aspect.ipynb: This notebook runs regression analysis on extracted opinions on 11 categories of city aspects from 34 cities. It can directly run in Jupyter notebook with "aspect_cities.csv" in the data folder.

- regression_analysis_census.ipynb: This notebook runs regression analysis on extracted opinions on features from United Census Bureau. It can directly run in Jupyter notebook with "aspect_cities.csv" in the data folder.

*Contributor: Zhanzhan Zhao, Jongseok Han, Haomin Lin* 


