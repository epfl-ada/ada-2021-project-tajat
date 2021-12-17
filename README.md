# British Bulletin Bias: revealing the hidden agenda of UK’s fourth estate

  

## Abstract

  

While mainstream media has been around for years, the digital age allows media concerns to increase societal impact. Although objectivity is regarded as the mainstay of modern-day reporting, news commercialisation and economic and political interests of media corporations raise questions on how neutral journalists are in fulfilling their job as the fourth estate. In an era where news and opinion making reaches individuals in an increasingly tailor-made fashion, news neutrality has never been less of a luxury. As journalist and media critic Walter Lippmann wrote in his 1920 work ‘Liberty and the News’: 

‘There can be no higher law in journalism than to tell the truth and to shame the devil.’

In this project, data analysis is performed on quotation data of twelve major British news sources, in order to gain insight on their neutrality. 

## Research Questions

The goal is to map papers onto the political spectrum according to their content. As neutrality can be achieved on different fronts and contexts, the main research goal of visualizing paper preferences can be split into multiple sub-analyses:
-	Sentiment analysis of quotes by politicians
-	Frequency of quotes made by politicians
-	Frequency of chosen topics

Searching for patterns, similarities, and differences between the newspapers we would like to answer the question:
- Are newspapers neutral in their quotations?
  

## Methods

The project is built up as a multistage rocket, where three main methods were designed.

- ### Sentiment analysis of matching quotes
As initial data exploration showed, many quotes appear in different newspapers. This could be used to study which news sources publish similar content. To add extra insights, each quote was also given a categorical sentiment value, representing positive, neutral, and negative. One indicator vector with total length equal to the total amount of quotes made by politicians was created for each newspaper. These vectors could then be studied and clustered to reveal similarities in newspaper content.

- ### Frequency analysis of different political speakers

The same vector approach could be used to cluster newspapers based on how often they quote certain speakers. Instead of categorical values, this vector would contain the total number of cited times per speaker and be of the length equal to the total number of speakers. Matching the speaker with its .parquet-file information makes it possible to cluster newspapers based only on political speakers, to gain information on which political party they cite the most.

- ### Frequency of important topics
Quotes was also scanned on the occurrences of specific words that are linked to certain chosen topics. These topics include current subject with dividing opinions between the labour and conservative parties, eg. Climate change, Brexit, the Monarchy. Counting the frequency of each topic per newspapers, the same methods could be used to draw conclusions within certain topics.

Concatenating the vectors for each newspaper, three big feature matrices per year was created. Due to many features compared to objects, we performed PCA on each of the matrices. Using the most important components from the PCA, we could then project the original matrices and try to cluster the projected matrices using K-means.
  

## Proposed timeline

| Period | Milestones |
|--|--|
| Week 9: 13/11 - 19/11 | Finish preliminary data analysis, cluster based on quotation vectors, speaker vectors |
| Week 10: 20/11 - 26/11 | Add sentiment analysis,  look into the specific topics| 
| Week 11: 27/11 - 3/12  | Continue analysis within topics, start on data story |
| Week 12: 4/12 - 10/12 | Continue on data story, add extra analysis where necessary|
| Week 13: 11/12 - 17/12 | Wrap up data story |

## Organization within the team

|  | Tasks |
|--|--|
| Anton | Clustering algorithms, topic analysis |
|  Tove| Speaker and quotation frequency analysis, write the data story  |
| Johanna | Data gathering and storing, topic analysis, start the data story |   
| Arthur | Sentiment analysis, write the data story, extra analysis |
| Everyone | Wrap up | 
## Questions for TAs (optional)

-   We’re struggling with finding the best method to cluster with. Could we get help on that?
