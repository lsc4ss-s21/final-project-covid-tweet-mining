# Final Project: Covid Tweet Mining

MACS 30123 | Large-Scale Computing for the Social Sciences | Spring 2021

Team member: Boya Fu, Yile Chen, Fengyi Zheng

## Work contains five parts:

- Data Collection: Fengyi
- Data Preprocessing: Boya, Fengyi, Yile
- Content Analysis: Boya, Yile
- Visualization: Yile
- Presentation and Report: Fengyi, Boya, Yile

## Social science research problem:

### Introduction and research question:
2020 is all about Covid-19. This unprecedented global pandemic has changed everyone's daily normal. We have seen that, in the United States, many governors like Andrew Cuomo of New York published COVID-related content such as policy guidelines and interacted with the public on Twitter. Evidence shows that, during a health crisis, the public expects immediate and transparent responses from the government (Boin et al., 2016); and political leaders play a vital role in communicating critical information to the public and guiding citizens to combat crisis (Grossman et al., 2020). Meanwhile, social media platforms serve as channels for such engagements between leaders and citizens, and they also offer opportunities for social science researchers to derive insights from large-scale text data.

We therefore believe that it is both timely and important to study online behaviors of governmental leaders during the pandemic. In our previous project for MACS 30122, we analyzed tweets from the CDC and built an interactive dashboard linking COVID-19 infection statistics with tweets. In this project, we will focus specifically on state-level response and scale up by examining tweets of all US state governors (from Jan 2020 to Feb 2021). We attempt to answer two research questions:

1.	How those political leaders tweet about the pandemic aggregately?
2.	Do democratic and republican leaders differ in twitter narratives during the pandemic?

The bulk of the project would be a content analysis of the collected tweets, with large-scale computing strategies integrated into data-collection, pre-processing, and modeling processes.

### Related work:
Various recent research has been leveraging twitter data to study political behaviors during the COVID-19 health crisis. Grossman et al. (2020) investigate the relationship between county governors’ online communication and public mobility patterns. Their finding suggests that governors’ messages of stay-at-home guidance result in significant decrease of resident’s mobility, and the effect is more pronounced in democratic-leaning counties. Applying framing and semantic role analysis, Jing and Ahn (2021) characterize twitter partisan narratives about the pandemic and find that democrats tend to emphasize financial and social support of the government, whereas Republicans focus more on individual citizens and foreign political entities (e.g., China). Rufai and Bunce (2020) perform a content analysis on G7 country leader’s communication behaviors on twitter during the COVID-19 pandemic, and show that the majority of viral tweets are classified as ‘informative’, rather than ‘morale-boosting’ or ‘political’.


## Research design and Large-scale computing methods:

To answer the previous research questions, we collect and analyze US state governors' tweets during the COVID-19 pandemic. We scrape data from Twitter and store the results into JSON files. Then, we conduct a record linkage and merge the text data into one CSV file. The main method of this project is content analysis. In order to better understand the Twitter narratives of governors, we utilize the LDA model to perform topic modeling and cluster the main topics in the Tweets. We are also interested in how political positions factor into the process, so we build separate models on the Tweets from democratic and republican leaders.  
  
Theoretically, the project will benefit from large-scale computing methods from three perspectives. First, parallel solutions of the Twitter scraping process will significantly improve the efficiency of data collection. With large amounts of text data, we may also parallelize the preprocessing part (e.g. Tokenization, Stemming, and Lemmatization) and thus accelerate the data cleaning process. Finally, the high performance of large-scale methods enables us to do more exploratory analysis and deepen our understanding of our data.  
  
Methodologically, we include large-scale computing strategies in three stages of our project. In the process of data collection, we use numba and MPI to accelerate the for-loop and the process of Input/Output. For data pre-processing, we apply Pyspark to read in data. Also, we will build pipelines to facilitate the sequence of stages of pre-processing. Finally, when we build the machine learning model based on LDA, Pyspark is especially helpful for the model training process.  

## Results:


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

Boin, A., Stern, E., Sundelius, B., et al. (2016). The politics of crisis management: Public leadership under pressure. Cambridge: Cambridge University Press.

Grossman, G., Kim, S., Rexer, J.M. and Thirumurthy, H. (2020). Political partisanship influences behavioral responses to governors’ recommendations for COVID-19 prevention in the United States. PNAS, 117(39), pp.24144–24153. doi: www.pnas.org/cgi/doi/10.1073/pnas.2007835117.

Jing, E. and Ahn, Y.Y. (2021). CHARACTERIZING PARTISAN POLITICAL NARRATIVES ABOUT COVID-19 ON TWITTER. Accessed at: https://arxiv.org/abs/2103.06960.

Rufai, S.R. and Bunce, B. (2020). World leaders’ usage of Twitter in response to the COVID-19
pandemic: a content analysis. Journal of Public Health, pp. 1–7. doi: 10.1093/pubmed/fdaa049.

Sha, H., Hasan, M.A., Mohler, G. and Brantingham, P.J. (2020) Dynamic topic modeling of the COVID-19 Twitter narrative among U.S. governors and cabinet executives. Accessed at: https://arxiv.org/abs/2004.11692.

Pyspark LDA modeling:
- https://spark.apache.org/docs/latest/api/python/
- https://towardsdatascience.com/introduction-to-spark-nlp-foundations-and-basic-components-part-i-c83b7629ed59
- https://spark.apache.org/docs/latest/ml-clustering.html
- https://github.com/prrao87/topic-modelling
- https://github.com/alejandronotario/LDA-Topic-Modeling
