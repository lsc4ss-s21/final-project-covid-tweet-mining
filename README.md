# Final Project: Covid Tweet Mining

MACS 30123: Large-Scale Computing for the Social Sciences | Spring 2021

**Team member**: Boya Fu, Yile Chen, Fengyi Zheng

## Social science research problem:

2020 is all about Covid-19. This unprecedented global pandemic has changed everyone's daily normal. We have seen that, in the United States, many governors like Andrew Cuomo of New York State published COVID-related content such as policy guidelines on Twitter. In this project, we are going to explore the political communications of state leaders as well as the CDC on Twitter during the pandemic, and how it would be related to the changes in the number of COVID infected cases and deaths. The bulk of the project would be a content analysis of collected tweets.

## Large-scale computing methods:

We will collect tweets from state governors and the CDC over the period of COVID-19 pandemic, and conduct content analysis (e.g., topic modeling) and visualization (e.g., word cloud). The project will benefit from large-scale computing methods from three perspectives. First, parallel solutions of the Twitter scraping process are expected to significantly improve the efficiency of data collection. With large amounts of textual data, we may also parallelize the preprocessing part (e.g. Tokenization, Stemming, and Lemmatization) and thus accelerate the data cleaning process. Finally, the high performance of large-scale methods enables us to further expand the topic with a larger scale of input data and more tuning and tests on model performance.

## Work contains five parts:

- Data Collection: Fengyi
- Data Preprocessing: Boya, Fengyi
- Content Analysis: Boya, Yile
- Visualization: Yile
- Presentation and Report: Fengyi, Boya, Yile

## Data Source

Twitter
- CDC (https://twitter.com/CDCgov)
- Governors' Tweets: from 51 governor's Twitter, stored in data\governor-twitter-handle.csv, some examples: Illinois Governor JB Pritzker (https://twitter.com/GovPritzker), New York Governor Andrew Cuomo (https://twitter.com/NYGovCuomo)

Covid
- JHU COVID MAP (https://coronavirus.jhu.edu/map.html)

## References:

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7188178/#ref1
