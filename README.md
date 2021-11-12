# British Bulletin Bias: revealing the hidden agenda of UK’s fourth estate

  

## Abstract

  

While mainstream media has been around for years, the digital age and technology allow media concerns to increase societal impact. Although objectivity is regarded as the mainstay of modern-day reporting, news commercialisation and economic and political interests of media corporations raise questions on how neutral journalists are in fulfilling their job as the fourth estate. In an era where news and opinion making reaches individuals in an increasingly tailor-made fashion, news neutrality has never been less of a luxury.  
As journalist and media critic <i>Walter Lippmann</i> wrote in his 1920 work <i>‘Liberty and the News’</i>:

  

<i>‘There can be no higher law in journalism than to tell the truth and to shame the devil.’</i>

  

In this project, data analysis is thus performed on quotation data of twelve major British newspapers and -websites, in order to gain insight on their neutrality.  
The choice to dive into the British media landscape instead of analysing media concerns in other English-speaking countries like the US, is done because of their (mainly) two-party political system and the fact that news bias in the US has been abundantly discussed already.

  

## Research Questions

  

As neutrality can be achieved on different fronts and contexts, the main research goal of visualizing paper preferences can be split into multiple sub-questions:

-   Obviously politics is highly prone to opinionated reporting and is therefore chosen as the main section of research. The goal would be to map papers on the political spectrum according to their content.
    

	-   How often do speakers from one side of the political spectrum get quoted in a specific newspaper compared to speakers from the other?
    
	-   Are there any trends in the quotation tone of a specific speaker in a specific news source?
    
	-   Which political speakers are being quoted when it comes to specific topics in a newspaper? What are their affiliated parties, economic ties, academic degrees…
    
	-   How did news sources political views evolve over the time period 2015-2020?
    

-   Similar analysis can be done to a lesser extent on other news rubrics like sports, economics, foreign affairs, if deemed feasible within the scope of the project.
    

	-   Comparing stances between different sections and news sources over time, could show if any topics are more polarized than others and reveal any trends.
    

-   Instead of setting the scope based on news rubric, one could also analyse neutrality within specific topics like climate change, COVID-19 or China.
    

	-   The insights could be compared to the overall political insights gained from the research above, to nuance any conclusions.
    
	-   In research within topics, time series should be especially interesting.  
    For example, what was the stance of the paper in 2015 compared to 2020?  
    How much quotations were done in total on e.g. climate change in 2015 compared to nowadays?  
    Are there trends between government decision-making and stances towards COVID-regulations and how the media covered those?  
    Were the media truly neutral during that time period?
    
	-   Comparing stances between different topics and news sources over time, could show what topics are more polarized compared to others and reveal any upward trends.
    

  

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
