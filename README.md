# Final Project: Covid Tweet Mining

MACS 30123 | Large-Scale Computing for the Social Sciences | Spring 2021

## Team member: Boya Fu, Yile Chen, Fengyi Zheng

## Social science research problem:

### Introduction and research question:
2020 is all about Covid-19. This unprecedented global pandemic has changed everyone's daily normal. We have seen that, in the United States, many governors like Andrew Cuomo of New York State published COVID-related content such as policy guidelines and interacted with the public on Twitter. Evidence shows that, during a health crisis, the public expects immediate and transparent responses from the government (Boin et al., 2016); political leaders play a vital role in communicating critical information to the public and guiding the citizens to combat crisis (Grossman et al., 2020). Meanwhile, social media platforms serve as channels for such engagements between leaders and citizens, and they also offer opportunities for social science researchers to derive insights from large-scale text data. In this project, we will analyze tweets of all US state governors (from Jan 2020 to Feb 2021) and explore 1. how those leaders respond to the pandemic aggregately, and 2. are there any partisan differences between twitter narratives of republic and democratic leaders. The bulk of the project would be a content analysis of collected tweets, with large-scale computing strategies integrated into data-collection, pre-processing, and modeling processes.


## Research design and Large-scale computing methods:

We will collect tweets from state governors and the CDC over the period of COVID-19 pandemic, and conduct content analysis (e.g., topic modeling) and visualization (e.g., word cloud). The project will benefit from large-scale computing methods from three perspectives. First, parallel solutions of the Twitter scraping process are expected to significantly improve the efficiency of data collection. With large amounts of textual data, we may also parallelize the preprocessing part (e.g. Tokenization, Stemming, and Lemmatization) and thus accelerate the data cleaning process. Finally, the high performance of large-scale methods enables us to further expand the topic with a larger scale of input data and more tuning and tests on model performance.

## Results:

## Work contains five parts:

- Data Collection: Fengyi
- Data Preprocessing: Boya, Fengyi, Yile
- Content Analysis: Boya, Yile
- Visualization: Yile
- Presentation and Report: Fengyi, Boya, Yile

## Data Source

Twitter
- CDC (https://twitter.com/CDCgov)
- Governors' Tweets: from 51 governor's Twitter, stored in data\governor-twitter-handle.csv, some examples: Illinois Governor JB Pritzker (https://twitter.com/GovPritzker), New York Governor Andrew Cuomo (https://twitter.com/NYGovCuomo)

Covid
- JHU COVID MAP (https://coronavirus.jhu.edu/map.html)

## Datasets

Large COVID-19 datasets on AWS S3 Bucket 
- COVID-19 case tracking data from Johns Hopkins and The New York Times
- https://registry.opendata.aws/aws-covid19-lake/

## References:

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7188178/#ref1

LDA modeling:
- https://github.com/prrao87/topic-modelling
- https://github.com/alejandronotario/LDA-Topic-Modeling
