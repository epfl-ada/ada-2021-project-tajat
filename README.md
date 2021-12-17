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
-	Are newspapers neutral in their quotations?
  

## Methods

  

The project is built up as a multistage rocket, where four main methods were designed in increasing order of complexity and implementation workload.

  

-   ### Frequency analysis of matching quotes
    

	-   <b>Exactly matching:</b> As initial data exploration showed, many quotes appear in different newspapers. This could be used to study which news sources publish similar content.  
	 One indicator vector with total length equal to the total amount of interesting quotes would be created for each newspaper. These vectors could then be clustered to reveal similarities in newspaper content.
    
	-   <b>Nearly the same: </b>It is clear that quotations could differ slightly but still hold the same meaning, where the impact on neutrality would be the same. Similar quotes could thus be mapped to one and the same quote value by using naive methods like TF-IDF. More extensive and complex methods like Locality Sensitive Hashing or other NLP-methods could lead to better results.
    

-  ### Frequency analysis of different political speakers
	-   The same vector approach could be used to cluster newspapers based on how often they quote certain speakers. Instead of boolean vectors, this vector would contain the total number of cited times per speaker and be of the length equal to the total number of different speakers. Matching the speaker with its .parquet-file information makes it possible to cluster newspapers on which political party they cite the most, what academic degree these people have, what their occupation is, what their ethnicity is, etc.
    

-  ### Add sentiment analysis
	-   A problem with naive frequency analysis is that only the quantitative measure is used and quote content is not considered. Sentiment analysis on quotes could make it possible to give a score to each speaker of how often it gets positively or negatively quoted. For sentiment analysis the pretrained model ‘Flair’ is used, but could be changed throughout milestone 3.
    

-  ### Look into important topics ###
	-   Quotes could be scanned on the occurence of specific words that are linked to certain topics. That way the same methods could be used to draw conclusions within certain topics.  
      
    

Gained insights will be compared with benchmark research papers on the topic.

  
  

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
